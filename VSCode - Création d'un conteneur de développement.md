# Création d'un conteneur de développement
Tout en étant connecté à une machine virtuelle distante et ayant un dossier de projet ouvert, cliquer sur le menu de gestion distante et "Ajouter un fichier de configuration 'Conteneur de développement'"<br>
![](./images/VSCode%20-%20Add%20dev%20container.png)

Sélectionner le conteneur qui correspond le mieux à votre projet.<br>
![](./images/VSCode%20-%20Dev%20container%20-%20Select%20container.png)

***Astuce*** Consulter la liste des conteneurs de développement disponible: [Available Dev Container Templates](https://containers.dev/templates)<br>
Porter attention au responsable du maintien du conteneur. Des conteneurs officiels et de la communauté y sont dans la liste.

Si proposé, sélectionnez la version du conteneur de développement.<br>
![](./images/VSCode%20-%20Dev%20container%20version.png)

Cocher les fonctionnalités à intégrer au conteneur de développement.<br>
![](./images/VSCode%20-%20Dev%20container%20features.png)

***Astuce*** Consulter la liste des fonctionnalités disponibles: [Available Dev Container Features](https://containers.dev/features)
Porter attention au responsable du maintien de la fonctionnalité. Des fonctionnalités officielles et de la communauté y sont dans la liste.

Activer au besoin Dependabot.<br>
![](./images/VSCode%20-%20Dev%20container%20dependabot.png)

***Pour plus d'information*** [General Availability of Dependabot Integration](https://containers.dev/guide/dependabot)

Vous devriez avoir obtenu un nouveau fichier `./.devcontainer/devcontainer.json`:
```json
// For format details, see https://aka.ms/devcontainer.json. For config options, see the
// README at: https://github.com/devcontainers/templates/tree/main/src/typescript-node
{
	"name": "Node.js & TypeScript",
	// Or use a Dockerfile or Docker Compose file. More info: https://containers.dev/guide/dockerfile
	"image": "mcr.microsoft.com/devcontainers/typescript-node:1-22-bookworm",
	"features": {
		"ghcr.io/devcontainers-extra/features/angular-cli:2": {}
	}

	// Features to add to the dev container. More info: https://containers.dev/features.
	// "features": {},

	// Use 'forwardPorts' to make a list of ports inside the container available locally.
	// "forwardPorts": [],

	// Use 'postCreateCommand' to run commands after the container is created.
	// "postCreateCommand": "yarn install",

	// Configure tool-specific properties.
	// "customizations": {},

	// Uncomment to connect as root instead. More info: https://aka.ms/dev-containers-non-root.
	// "remoteUser": "root"
}

```

VS Code devrait détecter le fichier de configuration et proposer d'ouvrir le projet dans le conteneur. Cliquer sur "Ouvrir dans le conteneur".<br>
![](./images/VSCode%20-%20Reopen%20in%20Container.png)

***Astuce*** L'ouverture du projet dans un conteneur est aussi disponible dans le menu de gestion distante et "Ouvrir dans le conteneur".<br>
![](./images/VSCode%20-%20Reopen%20in%20Container%20from%20menu.png)

Durant l'ouverture du conteneur, si vous cliquez sur "montrer le log", vous pouvez suivre l'évolution du déploiement.<br>
![](./images/VSCode%20-%20Reopen%20in%20Container%20-%20logs.png)

Le projet est maintenant ouvert dans le conteneur.<br>
![](./images/VSCode%20-%20open%20in%20container.png)






















# Références
[Development Containers](https://containers.dev/)
