# ubuntu web server

config file located at: `/etc/netplan/00-installer-config.yaml`

```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    eno2:
      dhcp4: true
```

apply config using `sudo netplan apply`

verify config using `ip a` or `ip link`