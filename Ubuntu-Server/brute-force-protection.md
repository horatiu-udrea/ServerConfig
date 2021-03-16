![Hacking](https://www.axigen.com/usr/files/articles/x82.png.pagespeed.ic.UN0bP5_iVK.png)

Install fail2ban
```
apt install fail2ban
systemctl enable fail2ban
```

Ban ip: `fail2ban-client set sshd banip <ip>`

Ban ip: `fail2ban-client set sshd unbanip <ip>`

See status: `fail2ban-client status sshd`

See logs in real time: `tail -F /var/log/fail2ban.log`

Change configuration in `/etc/fail2ban/jail.local`
```
[DEFAULT]
# Ban hosts for one day if they get 3 passwords wrong in 10 minutes:
bantime = 1d
maxretry = 3
findtime  = 10m

[sshd]
enabled = true
port = 22
```
