# Install deepseek with web-ui

### prerequisites

You need an Ubuntu > 22 host and root access.


### Installation

just run (change to your IP number)

```
ansible-playbook -i 172.233.28.12, install.yml 
```

afterwards, you can connect to http://IP-NUMBER using a webbrowser


### Cloudflare

If you want to use Cloudflare and restrict the access on Port 80 to the cloudflare source, just create a DNS + proxy entry for this IP NUmmer and set the variable in install.yml to 

```
cloudflare: true 

```
