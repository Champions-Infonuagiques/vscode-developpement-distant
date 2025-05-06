# Installation de Git
1. Dans la console, mettre à jour le registre de paquet.<br>
```bash
$ sudo apt update
```
Résultat:
```bash
...
Get:54 http://security.ubuntu.com/ubuntu noble-security/multiverse Translation-en [3792 B]                                      
Get:55 http://security.ubuntu.com/ubuntu noble-security/multiverse amd64 Components [208 B]                                     
Get:56 http://security.ubuntu.com/ubuntu noble-security/multiverse amd64 c-n-f Metadata [380 B]                                 
Fetched 33.5 MB in 8s (4426 kB/s)                                                                                               
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
63 packages can be upgraded. Run 'apt list --upgradable' to see them.
```

2. Configurer le répertoire apt de Docker.
```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
Résultat:
```bash
...
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
ca-certificates is already the newest version (20240203).
ca-certificates set to manually installed.
curl is already the newest version (8.5.0-2ubuntu10.6).
curl set to manually installed.
0 upgraded, 0 newly installed, 0 to remove and 63 not upgraded.
Hit:1 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble InRelease
Hit:2 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates InRelease                                                
Hit:3 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-backports InRelease                                              
Hit:4 http://security.ubuntu.com/ubuntu noble-security InRelease                                                            
Get:5 https://download.docker.com/linux/ubuntu noble InRelease [48.8 kB] 
Get:6 https://download.docker.com/linux/ubuntu noble/stable amd64 Packages [23.2 kB]
Fetched 72.0 kB in 0s (145 kB/s)      
Reading package lists... Done
```

3. Installer Docker.
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
Résultat:
```bash
...
The following NEW packages will be installed:
  containerd.io docker-buildx-plugin docker-ce docker-ce-cli docker-ce-rootless-extras docker-compose-plugin libltdl7 libslirp0
  pigz slirp4netns
0 upgraded, 10 newly installed, 0 to remove and 63 not upgraded.
Need to get 121 MB of archives.
After this operation, 441 MB of additional disk space will be used.
Do you want to continue? [Y/n] (Enter)

...
Processing triggers for man-db (2.12.0-4build2) ...
Processing triggers for libc-bin (2.39-0ubuntu8.4) ...
Scanning processes...                                                                                                            
Scanning linux images...                                                                                                         

Running kernel seems to be up-to-date.

No services need to be restarted.

No containers need to be restarted.

No user sessions are running outdated binaries.

No VM guests are running outdated hypervisor (qemu) binaries on this host.
```

4. Valider l'installation.
```bash
sudo docker run hello-world
```
Résultat:
```bash
$ sudo docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
e6590344b1a5: Pull complete 
Digest: sha256:424f1f86cdf501deb591ace8d14d2f40272617b51b374915a87a2886b2025ece
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```

5. Se donner accès à l'API Docker.

Pour avoir le droit de lancer des conteneurs, vous devez vous ajouter au groupe d'utilisateurs "docker".

```bash
# Créer le group
$ sudo groupadd docker

# Remplacer 'username' par votre non d'utilisateur
$ sudo usermod -a -G docker userName
```

> ***Astuce:*** Afin de rafraichir les permissions, fermez la connexion distante et reconnectez-vous.

# Références
- [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/)
- [Linux post-installation steps for Docker Engine](https://docs.docker.com/engine/install/linux-postinstall/)