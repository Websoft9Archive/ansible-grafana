# Initial Installation

If you have completed the Grafana deployment on Cloud Platform, the following steps is for you to start use it quikly

## Preparation

1. Get the **Internet IP** on your Cloud Platform
2. Check you **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the TCP:80 is allowed
3. Make a domain resolution on your DNS Console if you want to use domain for Grafana

## Grafana Installation Wizard

1. Using local Chrome or Firefox to visit the URL *http://domain name* or *http://Internet IP*, you will enter the register interface of Grafana
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

> More useful Grafana guide, please refer to [Grafana Documentation](https://grafana.com/docs)

## Q&A

#### I can't visit the start page of Grafana?

Your TCP:80 of Security Group Rules is not allowed so there no response from Chrome or Firefox

#### Which database does this Grafana use?

SQLite
