+ Ansible是一个简单的自动化运维管理工具，基于Python语言实现，由Paramiko和PyYAML两个关键模块构建，可用于自动化部署应用、配置、编排task(持续交付、无宕机更新等)
+ Ansible无需在被控主机部署任何客户端代理，直接通过SSH通道进行远程命令行执行或下发配置，纳管设备只要提供基本的命令行即可实现和Ansible的自动化运维对接。
+ 深信服应用交付产品，数据面提供三至七层的应用流量管理功能，管里面提供完善的命令行和API接口，有效提高运维效率。
+ Sangfor AD命令行简介：
  + sfcli(sangfor command line interface)是用户与设备之间的文本类命令行交互界面，用户可以输入文本类命令，并通过输入回车键提交设备执行相应命令，从而对设备进行配置和管理，并可以通过list 等相关命令查看相应的配置信息。
  + 命令行的构成如下：
[command]  [module ... ]  [component]  (options)  
其中：  
  command：表示此次命令执行的动作，比如create(新建)、modify(编辑)、delete(删除)等； 
  module：表示操作的配置模块，有一些模块下面还有子模块； 
  component：表示具体的操作对象； 
  options：表示操作对象时所使用的一些命令选项，一般为对象的相关属性。
