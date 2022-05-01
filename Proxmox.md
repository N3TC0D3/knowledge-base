# Proxmox
### Certificate Renewal
If you have to renew manually created SSL certificates in Proxmox while not having direct access to the webinterface you can replace the following files:
1. Replace the content of `/etc/pve/local/pveproxy-ssl.pem` with the contents of your `fullchain.pem`
2. Replace the content of `/etc/pve/local/pveprocy-ssl.key` with the contents of your `privkey.pem`
3. You may need to restart pveproxy using `service pveproxy restart` (run as root or using sudo)

> Remember to create backups before you do this in case you mess something up!

### Resize boot disk
If your VM runs out of space you can easily increase the disk size by visiting the `Hardware`-tab of the VM, click on the Harddisk that has gotten too small and press `resize disk` in the menu above. Enter the amount of space you want to add and confirm. Afterwards reboot the VM

> In case your VM doesn't boot anymore check the console. If it says `no bootable device found` or a similar message go to the `options`-tab of the VM and check the option `Boot Order`. Sometimes the check for the disk you edited gets removed and you have to recheck it.

Afterwards you will have to resize the partition from inside the OS. You can use builtin tools like `gparted`.

> On Windows you may have to move the Recovery partition to the end of the disk so that the free space is located right after the old partition
