# SMTP

大量用户实践反馈，使用**第三方 SMTP 服务发送邮件**是一种最稳定可靠的方式。  

请勿尝试在服务器上安装sendmail等发邮件方案，因为邮件系统的路由配置受制与域名、防火墙、路由等多种因素制约，导致不稳定、不易维护、诊断故障困难。

下面以**网易邮箱**为例，提供设置 Grafana 发邮件的步骤：

1. 在网易邮箱管理控制台获取 SMTP 相关参数
   ```
   SMTP host: smtp.163.com
   SMTP port: 465 or 994 for SSL-encrypted email
   SMTP Authentication: must be checked
   SMTP Encryption: must SSL
   SMTP username: websoft9@163.com
   SMTP password: #wwBJ8    //此密码不是邮箱密码，是需要通过163邮箱后台设置去获取的授权码
   ```
3. 编辑 [Grafana 配置文件](/zh/stack-components.md#grafana) 中的 SMTP选项，填写自己的 SMTP 项
   ```
   #################################### SMTP / Emailing #####################
   [smtp]
   enabled = false
   host = localhost:25
   user =
   # If the password contains # or ; you have to wrap it with triple quotes. Ex """#password;"""
   password =
   cert_file =
   key_file =
   skip_verify = false
   from_address = admin@grafana.localhost
   from_name = Grafana
   ehlo_identity =

   [emails]
   welcome_email_on_sign_up = false
   templates_pattern = emails/*.html
   ```
4. Restart Service
   ```
   sudo systemctl restart grafana-server
   ```
5. 登录 Grafana控制台，打开：【Alerting】>【Alert Rules】，新建一个【Email】通知渠道
   ![Grafana SMTP](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-sendmails-websoft9.png)
6. 点击【Send Test】

更多邮箱设置（QQ邮箱，阿里云邮箱，Gmail，Hotmail等）以及无法发送邮件等故障之诊断，请参考由Websoft9提供的 [SMTP 专题指南](https://support.websoft9.com/docs/faq/zh/tech-smtp.html)