# ubuntu web server

have to set static ip using `netplan`

config file located at: `/etc/netplan/00-installer-config.yaml`

```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    eno2:
      addresses:
        - <ip>/<cidr>
      nameservers:
        search: []
        addresses: []
      routes:
        - to: default
          via: <gateway_ip>
```

apply config using `sudo netplan apply`

verify config using `ip a` or `ip link`