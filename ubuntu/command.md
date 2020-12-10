### create new user ubuntu
sudo adduser <user-name>

--------------------------------------

### Enable ssh password authentication
```
/etc/ssh/sshd_config
```
then, change the line

```
PasswordAuthentication no
```
to
```
PasswordAuthentication yes
```

restart the SSH service

```
sudo service ssh restart
```

### Enable Logging in as root
```
sudo -i
```

```
/etc/ssh/sshd_config
```

change the line
```
PermitRootLogin no
```

to
```
PermitRootLogin yes
```

restart the SSH service
```
sudo service ssh restart
```

```
sudo passwd root
```
------------------
** Lệnh thêm public key cho apt
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys <public-key>

- sửa lỗi ssh too many authentication failures
```
ssh -o IdentitiesOnly=yes -i "pem.pem" ip
```
