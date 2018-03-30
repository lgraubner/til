# Synchronize time with NTP

Raspbian Stretch uses `timesyncd` for time management but does not sync it with a NTP server automatically.

Perform the following steps to enable automatic time syncing with a NTP server of your choice.

Edit `/etc/systemd/timesyncd.conf` (choose any NTP server you like):

```bash
[Time]
NTP=0.pool.ntp.org 1.pool.ntp.org 2.pool.ntp.org 3.pool.ntp.org
FallbackNTP=0.debian.pool.ntp.org 1.debian.pool.ntp.org 0.debian.pool.ntp.org
```

Set your timezone:

```bash
sudo timedatectl set-timezone 'Europe/Berlin'
```

Start the `timesyncd` service on boot:

```bash
sudo systemctl enable --now systemd-timesyncd.service
```

Enable NTP syncing:

```bash
sudo timedatectl set-ntp true
```

Review if everything is fine:

```bash
timedatectl
```