### create ssh key
```
ssh-keygen -t rsa -b 4096 -C "YOUR@EMAIL.com" -f "your file"
```

### create file ~/.ssh/config

```
# Personal account, - the default config
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa

# Work account-1
Host github.com-work_user1
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_work_user1
```

```
ssh-add -D            //removes all ssh entries from the ssh-agent
```

if you see a message
Could not open a connection to your authentication agent

```
eval `ssh-agent -s`
```

```
ssh-add ~/.ssh/id_rsa
```
