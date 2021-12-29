# Parameters

The Grafana deployment package contains a sequence software (referred to as "components") required for Grafana to run. The important information such as the component name, installation directory path, configuration file path, port, version, etc. are listed below.

## Path

Grafana installation directory: */usr/share/grafana*  
Grafana configuration file: */usr/share/grafana/conf/defaults.ini*  
Grafana log file: */var/log/grafana/grafana.log*  
Grafana data directory:*/usr/share/grafana/data*   
Grafana data log directory:*/usr/share/grafana/data/log*

> **defaults.ini** includes important configs, e.g. database connection strings, SMTP, Cache and so on

### Go

Grafana is development with Go

### Node.js

The Grafana web is developed with Node.js. This pre-packaged package is based on apt installation. No need to install Node.js on the Server.

### Nginx

Nginx vhost configuration file: */etc/nginx/sites-available/default.conf*  
Nginx main configuration file: */etc/nginx/nginx.conf*  
Nginx logs file: */var/log/nginx/*

### SQLite

The default configuration specifies a sqlite3 database located at */var/lib/grafana/grafana.db*

## Ports

These Ports is need when use Grafana, refer to [Safe Group Setting on Cloud Console](https://support.websoft9.com/docs/faq/tech-instance.html)

| Name | Number | Use |  Necessity |
| --- | --- | --- | --- |
| HTTP | 80 | HTTP requests for Grafana by Nginx proxy | Required |
| HTTPS | 443 | HTTPS requests Grafana by Nginx proxy| Optional |
| Grafana | 3000 | Web managment GUI for Grafana | Optional |

## Version

You can see the version from product page of Marketplace. However, after being deployed to your server, the components will be automatically updated, resulting in a certain change in the version number. Therefore, the exact version number should be viewed by running the command on the server:

```shell
# Nginx version:
nginx -v
```
