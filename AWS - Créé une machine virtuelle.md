# Créé une machine virtuelle dans AWS
1. Dans la console AWS, chercher pour le service "EC2" et sélectionner ce service dans le menu. <br>
<img src="./images/AWS - Console menu EC2.png">

1. Dans le menu "Instances", cliquer sur "Lancer des instances". <br>
<img src="./images/AWS - Launch new EC2.png">

1. Donné un nom à la machine, selectionner l'image "Ubuntu"
<img src="./images/AWS - New EC2 select image.png">

1. Selection une instance de type "t2.medium". <br>
<img src="./images/AWS - New EC2 select size.png">

1. Cliquer sur "Créer une paire de clés". <br>
<img src="./images/AWS - New EC2 select new ssh key.png">

1. Donner un nom à la nouvelle clé et cliquer sur "Créer une paire de clés". <br>
<img src="./images/AWS - New EC2 create new ssh key.png">

1. Sauvegarder la clé privé dans le dossier "C:\Users\user\\.ssh". <br>
<img src="./images/AWS - Save ssh key.png">

1. Changer la taile de la configuration de stockage pour 30Gio
<img src="./images/AWS - New EC2 select storage size.png">

1. Cliquer sur le boutton "Lancer l'instance" en bas à droite. <br>
<img src="./images/AWS - Launch EC2.png">

1. Une fois l'instance créé, retourner à la liste des instances et selectionner la nouvelle instance. <br>
1. Copier l'adresse DNS public, vous en aurai besoin pour la procédure [Configuration d'une connection distante](./VSCode%20-%20Configuration%20d'une%20connection%20distante.md)
<img src="./images/AWS - EC2 IP Public.png">