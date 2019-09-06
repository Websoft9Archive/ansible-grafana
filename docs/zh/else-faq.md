# FAQ

#### Grafana支持哪些数据源？

官方支持以下数据源:Graphite，InfluxDB，OpenTSDB，Prometheus，Elasticsearch，CloudWatch 和 KairosDB。

#### Grafana数据库连接配置信息在哪里？

数据库配置信息在Grafana安装目录下的 *defaults.ini* 中，[查阅安装目录路径](/zh/stack-components.md#grafana)

#### 如果没有域名是否可以部署 Grafana？

可以，访问`http://服务器公网IP` 即可

#### 是否可以修改 Grafana 的访问端口？

可以，通过修改 [Nginx 虚拟主机配置文件](/zh/stack-components.md)中相关参数

#### 部署和安装有什么区别？

部署是将一序列软件按照不同顺序，先后安装并配置到服务器的过程，是一个复杂的系统工程。  
安装是将单一的软件拷贝到服务器之后，启动安装向导完成初始化配置的过程。  
安装相对于部署来说更简单一些。 

#### 云平台是什么意思？

云平台指提供云计算服务的平台厂家，例如：Azure,AWS,阿里云,华为云,腾讯云等

#### 实例，云服务器，虚拟机，ECS，EC2，CVM，VM有什么区别？

没有区别，只是不同厂家所采用的专业术语，实际上都是云服务器