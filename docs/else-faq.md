# FAQ

#### Grafana support which data source?

Graphite, InfluxDB, OpenTSDB, Prometheus, Elasticsearch, CloudWatch, KairosDB。

#### Where is the database connection configuration of Grafana?

Database configuration information in *defaults.ini* in the Grafana installation directory, [refer to the installation directory](/stack-components.md#grafana)

#### If there is no domain name, can I deploy Grafana?

Yes, visit Grafana by *http://Internet IP*

#### Can I modify the port for visiting Grafana?

Yes, modify it by [Nginx vhost configuration file](/stack-components.md)

#### What's the difference between Deployment and Installation?

- Deployment is a process of installing and configuring a sequence of software in sequence in a different order, which is a complex system engineering.  
- Installation is the process of starting the initial wizard after the application is prepared.  
- Installation is simpler than deployment. 

#### What's Cloud Platform?

Cloud platform refers to platform manufacturers that provide cloud computing services, such as: **Azure, AWS, Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud**, etc.

#### What is the difference between Instance, Cloud Server, Virtual Machine, ECS, EC2, CVM, and VM?

No difference, just the terminology used by different manufacturers, actually cloud servers