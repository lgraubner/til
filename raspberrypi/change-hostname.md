# Change hostname

To change the hostname of a Raspberry Pi (Raspbian) edit the `/etc/hostname` file.

```bash
# set new hostname, reboot required
echo "raspberrypi" > /etc/hostname
```

Also edit the `/etc/hosts` file and edit the entry `127.0.0.1`.

```bash
127.0.0.1   raspberrypi # localhost by default
```