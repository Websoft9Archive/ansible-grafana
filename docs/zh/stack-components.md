# 参数

Grafana 预装包包含 Grafana 运行所需一序列支撑软件（简称为“组件”），下面列出主要组件名称、安装路径、配置文件地址、端口、版本等重要的信息。

## 路径

### Grafana


Grafana 安装目录： */usr/share/grafana*  
Grafana 配置文件： */usr/share/grafana/conf/defaults.ini*  
Grafana 日志文件： */var/log/grafana/grafana.log*  
Grafana 数据存储路径：*/usr/share/grafana/data*   
Grafana 数据日志路径：*/usr/share/grafana/data/log*

> Grafana 配置文件中包含数据库连接信息，数据存储路径、日志存储路径、STMP等重要配置

### Go

Grafana 基于 Go 语言开发

### Node.js

Grafana 前端采用 Node.js 开发，本预装包基于 apt/yum 安装，前端已经构建好，服务器上无需安装 Node.js

### Nginx

Nginx 虚拟主机配置文件：*/etc/nginx/conf.d/default.conf*  
Nginx 主配置文件： */etc/nginx/nginx.conf*  
Nginx 日志文件： */var/log/nginx/*

### SQLite

The default configuration specifies a sqlite3 database located at /var/lib/grafana/grafana.db. Please backup this database before upgrades. 

## 端口号

下面是您在使用本镜像过程中，需要用到的端口号，请通过 [云控制台安全组](https：//support.websoft9.com/docs/faq/zh/tech-instance.html)进行设置

| 名称 | 端口号 | 用途 |  必要性 |
| --- | --- | --- | --- |
| HTTP | 80 | 通过 http 访问Grafana by Nginx proxy| 必须 |
| HTTPS | 443 | 通过 https 访问 Grafana by Nginx proxy | 可选 |
| Grafana | 3000 | Grafana 端口 | 可选 |

## 版本号

组件版本号可以通过云市场商品页面查看。但部署到您的服务器之后，组件会自动进行更新导致版本号有一定的变化，故精准的版本号请通过在服务器上运行命令查看：

```shell
# Nginx version：
nginx -v
```