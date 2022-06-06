# sangfor_devops
hosts: ad-test remote_user: admin tasks:

name: create-link
command: 'sfcli create net link wan DianXin state enable interface { interface NET5 type physical } addresses [ '202.1.1.11/24' '240e::abcd/96' ] gateway '202.1.1.254' gateway_ipv6 '240e::1234' auto_snat enable upstream_bandwidth_mbps 1000 upstream_busy_percent 80 downstream_bandwidth_mbps 1000 downstream_busy_percent 80 dns_servers [ '114.114.114.144' '8.8.8.8'] monitors [ { monitor http target_host 'www.baidu.com' } ] cable_plugin_detect enable gateway_arp_detect { state disable }'
name: create-pool
command: 'sfcli create slb pool pool1 description 描述信息 method round-robin priority_level_available_node 1 nodes add [ { type domain address www.test.com cookie 12312312 port 90 state offline priority_level 10 weight 10 } {type address address 3.3.3.3 port 80 }] persist sourceip service_monitors [ ping http ] '
name: create-vs
command: 'sfcli create slb virtual-service MyVS vips [1.1.1.1 2.2.2.2] vports [80 90-91] pool pool1 service http '
