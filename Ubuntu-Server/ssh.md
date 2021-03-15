# SSH Configuration

![SSH](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/symmetric-encryption-ssh-tutorial.jpg)

### Server

Install SSH server
```
sudo apt install openssh-server
```

Manage SSH service
```
sudo systemctl status sshd
sudo systemctl enable sshd
sudo systemctl disable sshd
```

Allow SSH through firewall
```
sudo ufw allow ssh  # for default port
sudo ufw allow 2222 # for custom port
```

Configuration is in `/etc/ssh/sshd_config`
```
Port 2222 # Default port is 22
PasswordAuthentication no
```

**Host keys** are in the directory`/etc/ssh/`

**Authorized keys** are in the file `~/.ssh/authorized_keys`

See key randomart
```
ssh-keygen -lvf <key_location>
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

Generate new RSA key
```
ssh-keygen
```

Upload key on server
```
ssh-copy-id [-i <key_location>] [-p <port>] <username>@<hostname/ip>
```

Connect to instance
```
ssh [-i <key_location>] [-p <port>] [-o VisualHostKey=yes] <username>@<hostname/ip>
```

**Generated keys** are (by default) in the directory `~/.ssh/`

**Known hosts** are in the file `~/.ssh/known_hosts`
