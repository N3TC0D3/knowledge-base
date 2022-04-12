# Proxmox
### Certificate Renewal
If you have to renew manually created SSL certificates in Proxmox while not having direct access to the webinterface you can replace the following files:
1. Replace the content of `/etc/pve/local/pveproxy-ssl.pem` with the contents of your `fullchain.pem`
2. Replace the content of `/etc/pve/local/pveprocy-ssl.key` with the contents of your `privkey.pem`
3. You may need to restart pveproxy using `service pveproxy restart` (run as root or using sudo)

> Remember to create backups before you do this in case you mess something up!