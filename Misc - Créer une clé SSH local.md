### Créer une paire de clé SSH
Ouvrir une invite de commande et aller au répertoire `.ssh` de votre dossier de profile:
``` powershell
C:\Users\dev> cd ~/.ssh
C:\Users\user\.ssh>
```

Lancer la commande de création de clé SSH: `ssh-keygen -b 2048 -t rsa -f dev`
``` powershell
C:\Users\user\.ssh> ssh-keygen -b 2048 -t rsa -f dev
Generating public/private rsa key pair.
Enter passphrase (empty for no passphrase): [Enter]
Enter same passphrase again: [Enter]
Your identification has been saved in dev
Your public key has been saved in dev.pub
The key fingerprint is:
SHA256:95AqMZCYcYkm4yEEY6QszxvCAfoOktEDVz2ZYdyuQBA monorganisation\dev@MONLAPTOP
The key's randomart image is:
+---[RSA 2048]----+
|O+ooE=o=         |
|X*o=+o* .        |
|A**oo  o         |
|oB....  .  .     |
|=.=  .o.S +      |
|.+ o  .o o o     |
|  o   . .   .    |
|       .         |
|                 |
+----[SHA256]-----+

```

Deux nouveaux fichiers devrais avoir été créé:
``` powershell
C:\Users\user\.ssh> ls


    Répertoire : C:\Users\user\.ssh


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        2025-04-15     14:27           1831 dev
-a----        2025-04-15     14:27            408 dev.pub
```

