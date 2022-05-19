copy this in `/etc/logrotate.conf`
```
/var/lib/docker/containers/*/*.log {
    rotate 5
    copytruncate
    missingok
    notifempty
    compress
    maxsize 200M
    daily
}
```

Run command
```
logrotate -v -f /etc/logrotate.conf
```
