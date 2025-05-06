# Cloner un répertoire Git dans la machine virtuelle distante
## Préparation (optionnel)
### Créé un dossier dans la machine virtuelle distante pour les répertoires clonés.
Tout en étant connecté à une machine virtuelle distante, dans la fenêtre de terminal, entrer cette commande.<br>
```bash
# Changer 'NOM_DU_REPERTOIRE' pour le nom souhêté
$ mkdir ~/NOM_DU_REPERTOIRE
```
***Astuce*** Créer un dossier pour chaque hébergeur de code évite les conflits en cas de doublons de nom. <br> Example: "~/repos/github" ou "~/repos/azure-devops"

## Cloner un projet
Tout en étant connecté à une machine virtuelle distante, dans l'explorateur, cliquer sur "Clone Repository". <br>
![](./images/VSCode%20-%20Clone%20repo%20button.png)
<br><br>

---

<details>
<summary>Si Projet hébergé sur GitHub</summary>

Dans la barre de menu en haut, cliquer sur "Clone from GitHub".<br>
![](./images/VSCode%20-%20Clone%20from%20GitHub.png)

Dans la nouvelle fenêtre permettre l'extension "GitHub" de se connecté à votre compte GitHub.<br>
![](./images/VSCode%20-%20Allow%20GitHub%20extension.png)

Dans la nouvelle fenêtre de navigateur web, authentifiez-vous ou cliquer sur "Continuer".<br>
![](./images/VSCode%20-%20GitHub%20Authentication.png)

Dans la fenêtre de VS Code, sélectionner le répertoire à cloner.<br>
![](./images/VSCode%20-%20Select%20repo%20to%20clone.png)
</details>
<br>
<details>
<summary>Si l'URL du projet</summary>

Dans la barre de menu en haut, entrer l'URL du répertoire.<br>
![](./images/VSCode%20-%20Git%20repo%20url.png)

</details>

---
<br>

Sélectionner le chemin dans laquelle le projet sera cloné. <br>
![](./images/VSCode%20-%20Select%20clone%20path%201.png)<br>
![](./images/VSCode%20-%20Select%20clone%20path%202.png)

Cliquer sur "Open" pour ouvrir le dossier du projet dans la fenêtre de VS Code en cours.<br>
![](./images/VSCode%20-%20Open%20cloned%20repository.png)

Le projet est maintenant ouvert. <br>
![](./images/VSCode%20-%20Projet%20open.png)

## Ouvrir un projet déjà cloné
Tout en étant connecté à une machine virtuelle distante, dans l'explorateur, cliquer sur "Open Folder".<br>
![](./images/VSCode%20-%20Open%20folder.png)

Sélectionner le chemin dans laquelle le projet a été' cloné et cliquer "OK". <br>
![](./images/VScode%20-%20Select%20projet%20folder%201.png)<br>
![](./images/VScode%20-%20Select%20projet%20folder%202.png)

Le projet est maintenant ouvert. <br>
![](./images/VSCode%20-%20Projet%20open.png)