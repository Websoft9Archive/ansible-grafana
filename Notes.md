# Grafana Notes

组件名称：Grafana 
安装文档：https://grafana.com/docs/grafana/latest/installation/rpm/ 
配置文档：https://grafana.com/docs/grafana/latest/installation/configuration/#linux
支持平台： Debian家族 | RHEL家族 | Windows | macOS |Docker  

责任人：zxc

## 概要

Grafana是一款用Go语言开发的开源数据可视化工具，可以做数据监控和数据统计，带有告警功能。

## 环境要求

* 程序语言：Go
* 应用服务器：自带
* 数据库：sqlite3
* 依赖组件：无
* 其他：

## 安装说明

官方有三种安装方法,这里使用官方grafana仓库自动安装。

下面基于不同的安装平台，分别进行安装说明。

### CentOS

```shell
# 配置grafana仓库
vim /etc/yum.repos.d/grafana.repo
[grafana]
name=grafana
baseurl=https://packages.grafana.com/oss/rpm
repo_gpgcheck=1
enabled=1
gpgcheck=1
gpgkey=https://packages.grafana.com/gpg.key
sslverify=1
sslcacert=/etc/pki/tls/certs/ca-bundle.crt

# 安装
sudo yum install grafana-enterprise
```

## 路径

* 程序路径：/usr/sbin/grafana-server
* 日志路径：/var/log/grafana
* 配置文件路径：/etc/grafana/grafana.ini
* 其他...

## 配置

安装完成后，可按需完成如下配置

```shell
#/etc/grafana/grafana.ini
[server]:设置协议(http,https访问)，http_addr(监听哪些地址，默认是所有)，http_port(监听的端口，默认3000)
[security]：设置管理员的账号密码
[users]:设置普通是否可以登录和操作权限
[auth.anonymous]：设置是否匿名用户可以访问
[smtp] [emails]:发送邮件的设置
[log.console] [log.file]：日志输出的级别和轮询的设置

```

## 服务

本项目安装后自动生成：grafana-server 服务


## 环境变量

列出需要增加的环境变量以及增加环境变量的命令

## 版本号

通过如下的命令获取主要组件的版本号: 

```
# Check Grafana version
rpm -qa |grep grafana

```

## 常见问题

#### 有没有管理控制台？

*http:// 公网 IP:3000* 即可访问控制台，默认使用sqlit3数据库，初始账号和密码都为admin。

#### 本项目需要开启哪些端口？

| item      | port  |
| --------- | ----- |
| http_port | 3000 |


#### 有没有CLI工具？

有，通过 `grafana-cli` 查看工具的说明

## 日志

* 2020-04-17完成CentOS安装研究
