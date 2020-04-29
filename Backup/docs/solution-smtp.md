# SMTP

Sending mail is a common feature for Grafana. After a large number of user practice feedback, only one way is recommended, that is, using the **third-party STMP service** to send the email.

> Do not try to install **Sendmail** or other Mail server software on your Cloud Server for sending mail, because it is very difficulty in maintenance.

Follow is the sample using **SendGrid's SMTP Service** to configure sending mail for Grafana:

1. Log in SendGrid console, prepare your SMTP settings like the follow sample
   ```
   SMTP host: smtp.sendgrid.net
   SMTP port: 25 or 587 for unencrypted/TLS email, 465 for SSL-encrypted email
   SMTP Authentication: must be checked
   SMTP Encryption: must SSL
   SMTP username: websoft9smpt
   SMTP password: #fdfwwBJ8f    
   ```
3. Edit the SMTP segment part in [Grafana configuration file](/stack-components.md#grafana) and fill in your SMTP items
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
5.  Log in Grafana Console, Open: **Alerting** > **Alert Rules**, create new Notification Channel and select the type with **Email**
   ![Grafana SMTP](https://libs.websoft9.com/Websoft9/DocsPicture/en/grafana/grafana-sendmails-websoft9.png)
6. Click the **Test Connection**, you can get the feedback *"no errors were..."* if SMTP is useful

More SMTP Service(Gmail, Hotmail, QQ mail, Yahoo mail, SendGrid and so on)  settings or Issues with SMTP, please refer to Websoft9's *[SMTP Guide](https://support.websoft9.com/docs/faq/tech-smtp.html)*