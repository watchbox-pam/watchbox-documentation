# Lancement du projet

## Récupération du projet

Pour récupérer le projet, cloner le repository git
```bash
git clone https://github.com/watchbox-pam/watchbox-app.git
```

## Où lancer le projet

Pour lancer le frontend de l'application, vous aurez besoin
- soit d'un téléphone avec l'application [Expo Go](https://expo.dev/go)
- soit d'un émulateur sur votre machine pour tester le projet
    - ### Émulateur Android
        Un émulateur Android peut être utilisé sur n'importe quel OS majeur : suivre la [documentation d'Expo](https://docs.expo.dev/workflow/android-studio-emulator/).
    - ### Simulateur IOS
        Le simulateur IOS ne peut être utiliser que sur MacOS : suivre la [documentation d'Expo](https://docs.expo.dev/workflow/ios-simulator/)

## Lancement du projet

Ouvrir le projet dans un éditeur de code comme VsCode ou un IDE comme WebStorm.

Ajouter les variables d'environnement au fichier .env.

Installer les packages nécessaires au fonctionnement du projet avec la commande `npm / yarn / bun install`.

Lancer la commande `npm / yarn / bun expo start` pour lancer le projet.