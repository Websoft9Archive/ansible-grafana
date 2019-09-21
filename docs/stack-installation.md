# Initial Installation

If you have completed the Grafana deployment on Cloud Platform, the following steps is for you to start use it quikly

## Preparation

1. Get the **Internet IP** on your Cloud Platform
2. Check you **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the TCP:80 is allowed
3. Make a domain resolution on your DNS Console if you want to use domain for Grafana

## Grafana Installation Wizard

1. Using local Chrome or Firefox to visit the URL *http://domain name* or *http://Internet IP*, you will enter the register interface of Grafana
![Grafana login page](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-login-websoft9.png)

2. Input the [default username and password](/stack-accounts.md#grafana), then system will force you to change your password
![Grafana change password](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-forcechangepw-websoft9.png)

3. Log in to the Grafana Console  
![Grafana console](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-dashboard-websoft9.png)

4. Open **Configuration** > **Plugins** to add plugins for function extension 
![Grafana add plugin](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-plugins-websoft9.png)

5. Open **Configuration** > **Data Sources** to add data source for analysis  
![Grafana add data source](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-datasource-websoft9.png)

6. Open **Configuration** > **Users** to add user  
![Grafana add user](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-users-websoft9.png)

> More useful Grafana guide, please refer to [Grafana Documentation](https://grafana.com/docs)

## Q&A

#### I can't visit the start page of Grafana?

Your TCP:80 of Security Group Rules is not allowed so there no response from Chrome or Firefox

#### Which database does this Grafana use?

SQLite
