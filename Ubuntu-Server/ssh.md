# SSH Configuration

![SSH](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/symmetric-encryption-ssh-tutorial.jpg)

### Server

Install SSH server
```
sudo apt install openssh-server
```

Enable SSH service
```
sudo systemctl enable ssh
```

(Optional) Allow SSH through firewall
```
sudo ufw allow ssh
```

Change configuration in `/etc/ssh/sshd_config`
```
Port 2222
PasswordAuthentication no
```

Check authorized keys in `~/.ssh/authorized_keys`

See key randomart
```
ssh-keygen -lvf ~/.ssh/<key_location>
```

Check IP address
```
ip a
```

### Client

Install SSH client
```
sudo apt install openssh-client
```

Connect to the instance
```
ssh -i <key_location> -p <port> <username>@<hostname/ip> -o VisualHostKey=yes
```
