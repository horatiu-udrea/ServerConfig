# SSH Configuration

Useful configuration [here](https://help.ubuntu.com/community/SSH/OpenSSH/Configuring)

Install SSH server
```sudo apt install openssh-server```

Enable SSH service
```sudo systemctl enable ssh```

(Optional) Allow SSH through firewall
```sudo ufw allow ssh```

Check IP address
```ip a```

Connect to the instance
```ssh <username>@<ip>```
