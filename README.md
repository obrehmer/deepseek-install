# Install deepseek with web-ui

### prerequisites

You need an Ubuntu > 22 host and root access.


### id_rsa.pu into vault

Create the ansible vault file from your ssh pubkey. 

```
ansible-vault encrypt ~/.ssh/id_rsa.pub --output authorized_keys.vault

```

You will now be asked for a Vault password. You will need this password later for decryption or for the playbook run.
You can also put the password in a file outside of the git repo and set this in the ansible.cfg, e.g.

```
vault_password_file = ~/.vaultpass_ai
```




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
