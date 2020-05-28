## Change the mirroring location in ubuntu
nano /etc/apt/sources.list

### Change IP address (to static)

sudo nano /etc/netplan/50-cloud-init.yaml or 01-netcfg.yaml
```bash 
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s3:
     dhcp4: no
     addresses: [192.168.1.222/24]
     gateway4: 192.168.1.1
     nameservers:
       addresses: [8.8.8.8,8.8.4.4]

```
### ssh keys
https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-linux-server