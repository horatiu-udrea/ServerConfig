# Pi-hole

![Pi-hole](https://brianchristner.io/content/images/2019/03/pihole-traditional-dns-1024x630.png)

Installation [instructions](https://docs.pi-hole.net/main/basic-install/)

Configure firewall
``` 
ufw allow http
ufw allow 53
```

Flush DNS (Manjaro): `nscd -i hosts`

Web interface: `http://pi.hole/admin`

Change admin password: `pihole -a -p`
