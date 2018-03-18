# Set static IP

Add the following to `/etc/dhcpcd.conf` and reboot:

```bash
interface eth0
static ip_address=192.168.1.100/24
static routers=192.168.1.1
static domain_name_servers=192.168.1.1
```

The first part (192.168.1) might vary. Check your routers IP and change accordingly.