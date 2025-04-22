# Configurer VS Code pour la connexion distante
## Ajouter un nouvel hôte
1. Dans VS Code, cliquer sur le bouton "Fenêtre distante". Dans le menu en haut, cliquer sur "Connecter la fenêtre courante à un hôte". <br>
<img src="./images/VSCode - Remote window button.png"> <br>
<img src="./images/VSCode - Connect Current Window to Host.png">

1. Sélectionner "Ajouter un nouvel hôte SSH". <br>
<img src="./images/VSCode - Add new SSH host.png">

1. Entrer l'adresse IP publique de la machine virtuelle de développement et fait "Entrée". <br>
<img src="./images/VSCode - Host ip address.png">

1. Sélectionner le fichier de configuration SSH. <br>
<img src="./images/VSCode - SSH Configuration file.png">

## Configurer l'hôte
1. Dans VS Code, cliquer sur le bouton "Fenêtre distante". Dans le menu en haut, cliquer sur "Connecter la fenêtre courent à un hôte".  <br>
<img src="./images/VSCode - Remote window button.png"> <br>
<img src="./images/VSCode - Connect Current Window to Host.png">

1. Sélectionner "Configurer l'hôte SSH". <br>
<img src="./images/VSCode - Open SSH Configuration file.png">

1. Sélectionner votre fichier de configuration SSH. <br>
<img src="./images/VSCode - SSH Configuration file.png">

1. Vous devriez y retrouver l'hôte précédemment ajouté.
```ssh_config
Host 130.107.48.90
  HostName 130.107.48.90
```

5. Ajouter le chemin vers votre clé publique SSH et le nom d'utilisateur. Puis sauvegarder. <br>
```
Host 130.107.48.90   # Nom de l'hôte affichié dans le menu
  HostName 130.107.48.90
  IdentityFile ~/.ssh/dev01.pem
  User dev
```

