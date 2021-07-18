# Install docker

1. Update the apt package index and install packages to allow apt to use a repository over HTTPS:
```bash
sudo apt-get update
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common -y
```

2. Add Docker’s official GPG key:
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

3. Use the following command to set up the stable repository
```bash
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

4. INSTALL DOCKER ENGINE
```bash
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io -y
```

5. Add your user to docker group
```bash
sudo usermod -aG docker ${USER}
```

6. Command logout and login again
```bash
newgrp docker
```
