# Troubleshooting

We collect the most common troubleshooting of using Grafana for your reference:

## Database related

#### Database service could not be started?

Insufficient disk space, insufficient memory, and configuration file errors can make database service could not be started  

It is recommended to first check through the command.

```shell
# view disk space
df -lh

# view memory rate
free -lh
```

## Instance related

Instance troubleshooting is closely related to the Instance provider that is Cloud Platform   
Please refer to [Cloud Platform Documentation](https://support.websoft9.com/docs/faq/tech-instance.html)

## Network related

## Other