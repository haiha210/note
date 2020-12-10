# Config new server
- Create new user deploy
```
sudo adduser deploy
```

- Add deploy in group sudo
```
sudo usermod -aG sudo deploy
```

- Connect user by ssh
```
touch ~/.ssh/authorized_keys
chmod 0700 $HOME/.ssh
# add ssh-key to file authorized_keys
```
