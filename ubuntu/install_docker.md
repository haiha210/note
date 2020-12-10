# Install docker

1. Update the apt package index and install packages to allow apt to use a repository over HTTPS:
```
sudo apt-get Update
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```

2. Add Docker’s official GPG key:
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

3. Use the following command to set up the stable repository
```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

4. INSTALL DOCKER ENGINE
```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

5. Add your user to docker group
```
sudo usermod -aG docker ${USER}
```