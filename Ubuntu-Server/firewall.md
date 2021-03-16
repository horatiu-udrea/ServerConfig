![Firewall](https://images.idgesg.net/images/article/2019/05/cso_security_lock_firewall_fires_threats_exploits_by_matejmo_gettyimages-879868000_2400x1600-100798015-large.jpg)

Installation
```
apt install ufw
ufw enable
ufw default deny incoming
ufw default allow outgoing
```


Open ports
```
ufw allow 22
ufw allow 22/tcp
ufw allow 1000:2000/tcp
ufw insert 1 allow 80
ufw allow ssh
```

Close ports
```
ufw deny 22
ufw deny ssh
```

Remove a rule
```
ufw delete deny 22
ufw delete 1
```

Specific
```
ufw allow proto tcp from 192.168.0.2 to any port 22
```

Check status
```
ufw status numbered
```

App integration
```
ufw app list
ufw allow Samba
```

Disable
```
ufw disable
```
