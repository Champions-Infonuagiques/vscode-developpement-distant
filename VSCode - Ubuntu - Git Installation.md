# Installation de Git
1. Dans la console, mettre à jour le registre de paquet.<br>
```bash
$ sudo apt update
```
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

2. Installer Git. <br>
```bash
$ sudo apt install git
```
```bash
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
git is already the newest version (1:2.43.0-1ubuntu7.2).
git set to manually installed.
0 upgraded, 0 newly installed, 0 to remove and 63 not upgraded
```
***À savoir: Git est souvent déjà installé dans Ubuntu par défaut.***

3. Valider l'installation:
```bash
$ git --version
git version 2.43.0
```
