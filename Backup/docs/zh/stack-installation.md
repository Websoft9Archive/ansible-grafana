# 初始化安装

在云服务器上部署 Grafana 预装包之后，请参考下面的步骤快速入门。

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:80** 端口是否开启
3. 若想用域名访问 Grafana，请先到 **域名控制台** 完成一个域名解析

## Grafana 安装向导

1. 使用本地电脑的 Chrome 或 Firefox 浏览器访问网址：*http://域名* 或 *http://Internet IP*, 就进入登录页面
![Grafana 登录](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-login-websoft9.png)

2. 输入默认的用户名和密码（[查看](/zh/stack-accounts.md#grafana)），系统会提示修改密码
![Grafana 强提示修改密码](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-forcechangepw-websoft9.png)

3. 登录到 Grafana 控制台页面  
![Grafana 控制台](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-dashboard-websoft9.png)

4. 通过【Configuration】>【Plugins】添加插件  
![Grafana 添加插件](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-plugins-websoft9.png)

5. 通过【Configuration】>【Data Sources】添加数据源（分析对象）  
![Grafana 添加数据源](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-datasource-websoft9.png)

6. 通过【Configuration】>【Users】增加用户    
![Grafana 添加用户](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-users-websoft9.png)

> 需要了解更多 Grafana 的使用，请参考官方文档：[Grafana Documentation](https://grafana.com/docs)

## 常见问题

#### 浏览器打开IP地址，无法访问 Grafana（白屏没有结果）？

您的服务器对应的安全组80端口没有开启（入规则），导致浏览器无法访问到服务器的任何内容

#### 本部署包采用的哪个数据库来存储 Grafana 数据？

SQlite
