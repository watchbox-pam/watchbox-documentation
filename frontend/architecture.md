#

L'architecture du frontend de l'application Watchbox se présente de la façon suivante : 

```
📦src
 ┣ 📂app
 ┃ ┣ 📂(app)
 ┃ ┃ ┣ 📂(tabs)
 ┃ ┃ ┃ ┣ 📜_layout.tsx
 ┃ ┃ ┃ ┗ 📜xxx.tsx
 ┃ ┃ ┣ 📂movie
 ┃ ┃ ┃ ┣ 📂[id]
 ┃ ┃ ┃ ┃ ┗ 📜review.tsx
 ┃ ┃ ┃ ┗ 📜[id].tsx
 ┃ ┃ ┣ 📂person
 ┃ ┃ ┃ ┗ 📜[id].tsx
 ┃ ┃ ┗ 📂watchList
 ┃ ┃ ┃ ┗ 📜[id].tsx
 ┃ ┣ 📜_layout.tsx
 ┃ ┣ 📜base.tsx
 ┃ ┣ 📜login.tsx
 ┃ ┗ 📜signup.tsx
 ┣ 📂assets
 ┃ ┣ 📂fonts
 ┃ ┃ ┗ 📜Oswald-VariableFont_wght.ttf
 ┃ ┣ 📂images
 ┃ ┃ ┗ 📜image.png
 ┣ 📂components
 ┃ ┗ 📜Component.tsx
 ┣ 📂models
 ┃ ┗ 📜Model.ts
 ┣ 📂screens
 ┃ ┗ 📜xxxScreen.tsx
 ┣ 📂services
 ┃ ┗ 📜xxxService.ts
 ┣ 📂styles
 ┃ ┗ 📜xxxStyle.ts
 ┣ 📂utils
 ┃ ┣ 📜axios.ts
 ┃ ┗ 📜encryption.ts
 ┗ 📂zustand
   ┗ 📜xxxStore.ts
```

```
📦watchbox-app
 ┣ 📂.expo
 ┣ 📂.github
 ┃ ┗ 📂workflows
 ┃ ┃ ┗ 📜test.yml
 ┣ 📂.husky
 ┃ ┗ 📜pre-commit
 ┣ 📂android
 ┣ 📂ios
 ┣ 📂src
 ┃ ┣ 📂app
 ┃ ┃ ┣ 📂(app)
 ┃ ┃ ┃ ┣ 📂(tabs)
 ┃ ┃ ┃ ┃ ┣ 📜_layout.tsx
 ┃ ┃ ┃ ┃ ┗ 📜xxx.tsx
 ┃ ┃ ┃ ┣ 📂movie
 ┃ ┃ ┃ ┃ ┣ 📂[id]
 ┃ ┃ ┃ ┃ ┃ ┗ 📜review.tsx
 ┃ ┃ ┃ ┃ ┗ 📜[id].tsx
 ┃ ┃ ┃ ┣ 📂person
 ┃ ┃ ┃ ┃ ┗ 📜[id].tsx
 ┃ ┃ ┃ ┗ 📂watchList
 ┃ ┃ ┃ ┃ ┗ 📜[id].tsx
 ┃ ┃ ┣ 📜_layout.tsx
 ┃ ┃ ┣ 📜base.tsx
 ┃ ┃ ┣ 📜login.tsx
 ┃ ┃ ┗ 📜signup.tsx
 ┃ ┣ 📂assets
 ┃ ┃ ┣ 📂fonts
 ┃ ┃ ┃ ┗ 📜Oswald-VariableFont_wght.ttf
 ┃ ┃ ┣ 📂images
 ┃ ┃ ┃ ┗ 📜image.png
 ┃ ┣ 📂components
 ┃ ┃ ┗ 📜Component.tsx
 ┃ ┣ 📂models
 ┃ ┃ ┗ 📜Model.ts
 ┃ ┣ 📂screens
 ┃ ┃ ┗ 📜xxxScreen.tsx
 ┃ ┣ 📂services
 ┃ ┃ ┗ 📜xxxService.ts
 ┃ ┣ 📂styles
 ┃ ┃ ┗ 📜xxxStyle.ts
 ┃ ┣ 📂utils
 ┃ ┃ ┣ 📜axios.ts
 ┃ ┃ ┗ 📜encryption.ts
 ┃ ┗ 📂zustand
 ┃   ┗ 📜xxxStore.ts
 ┣ 📜.env
 ┣ 📜.env.example
 ┣ 📜.eslintrc.js
 ┣ 📜.gitignore
 ┣ 📜.prettierrc
 ┣ 📜.watchmanconfig
 ┣ 📜README.md
 ┣ 📜app.json
 ┣ 📜bun.lockb
 ┣ 📜eas.json
 ┣ 📜expo-env.d.ts
 ┣ 📜package.json
 ┗ 📜tsconfig.json
```

## .github/workflows

Dossier qui contient les [workflows github](https://docs.github.com/fr/actions/writing-workflows), pour pouvoir
- lancer différents checks (builds, tests) avant la validation d'une pull request
- lancer un script de dépliement automatique après la validation d'une pr
- etc...

## husky

Dans le fichier pre-commit, on met des commandes qui seront lancées au moment de chaque commit git. Exemple : un linter, des tests...

## src

### app

Les différents écrans de l'application. Les fichiers de ce dossier ne contiennent pas de code mais appellent uniquement les composants exportés du dossier screens.

Comme nous utilisons Expo, le routage de l'application se fait par rapport à l'arborescence de ce dossier.

### assets

Les assets inclus dans l'application (fonts, images...).

### components

Les composants React qui sont réutilisés à travers l'application.

### models

Les définitions des modèles de données utilisés comme type à travers le frontend de l'application. Utilisés pour structurer et valider les données reçues et envoyées.

### screens

Les définitions des écrans de l'application. Contient l'import de tous les composants nécessaires à l'affichage de la page ainsi que la gestion du state.

### services

Le code qui va faire le lien entre l'interface utilisateur définie dans les screens, et le backend de l'application.

Cela comprend l'envoi de toutes les requêtes vers le backend, pour faire de la récupération de données, l'envoi de commandes...

Chaque screen a son service particulier qui lui est associé.

### styles

Les fichiers de style qui seront appelés par les screens.

### utils

Les services qui seront réutilisés à plusieurs endroits à travers l'application

### zustand

Le dossier qui contient les différents stores Zustand. Cela permet d'avoir un state commun à travers toute l'application.