# Technologies

## Langage de programmation 

Le frontend de l'application Watchbox est construit en [React Native](https://reactnative.dev/), et utilise également le framework [Expo](https://expo.dev)

## Téléchargement de Node

Pour télécharger Node, il est recommandé d'utiliser nvm (Node Version Manager) pour pouvoir gérer les différentes versions de Node sur sa machine

### Pour Windows

Suivre la [documentation Microsoft](https://learn.microsoft.com/fr-fr/windows/dev-environment/javascript/nodejs-on-windows#install-nvm-windows-nodejs-and-npm) pour installer [nvm-windows](https://github.com/coreybutler/nvm-windows)


### Pour MacOS

- Soit installer nvm via une commande curl
    ```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
    ```
    Puis l'ajouter au PATH
    ```bash
    export NVM_DIR="$HOME/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
    ```
    
- Soit installer nvm via [Homebrew](https://brew.sh/fr/)
    - Installer Homebrew
    - Lancer la commande
        ```bash
        brew install nvm
        ```
    - Puis ajouter nvm au PATH
        ```bash
        export NVM_DIR="$HOME/.nvm"
        source "$(brew --prefix nvm)/nvm.sh"
        ```

Vous pouvez ensuite gérer la version de Node actuellement utilisée par votre machine