# Packages frontend

Le backend de l'application Watchbox utilise un certain nombre de packages pour fonctionner.

Ces packages sont répertoriés dans le fichier requirements.txt et doivent être installés avec votre manager de package (npm, yarn, bun...) : 
```bash
npm / yarn / bun install
```

Voici les principaux packages utilisés :

## packages [react](https://fr.react.dev/)

Le frontend de l’application Watchbox est construit avec React, pour créer des interfaces utilisateur dynamiques et réactives. L'utilisation de React permet de structurer l'application en composants réutilisables, facilitant la maintenance, l’évolutivité et la cohérence du design.

## packages react-native

Nous utilisons React Native, ce qui nous permet de faire en sorte que l'application Watchbox soit disponible à la fois pour iOS et Android à partir d’un code JavaScript unifié. Grâce à React Native, nous pouvons mutualiser une grande partie du code entre les deux plateformes, tout en conservant des performances proches du natif et une expérience utilisateur fluide.

En plus de React Native, nous pouvons également utiliser des packages complémentaires comme par exemple : 

- react-native-webview : pour afficher du contenu web dans l'application de manière encapsulée.

- react-native-svg : pour manipuler facilement des graphiques vectoriels (par exemple pour les icônes ou des graphiques de données).

## packages [expo](https://expo.dev/)

En plus de React Native, nous utilisons Expo, un framework et une plateforme qui simplifie considérablement le développement, le déploiement et les tests d’applications mobiles. Grâce à Expo, nous bénéficions d’un ensemble d’outils et de services intégrés qui accélèrent le cycle de développement tout en réduisant la complexité technique liée à la configuration native (Xcode, Android Studio, etc.).

En plus d'Expo, nous pouvons également utiliser des packages complémentaires comme par exemple : 
- expo-router : gestion de navigation basée sur le filesystem, facilitant l’organisation des écrans et la structuration du code.

- expo-crypto : permet d’accéder aux fonctions cryptographiques pour le hachage sécurisé (utile pour la validation de données, signature, etc.).

## [axios](https://axios-http.com/fr/docs/intro)

Nous utilisons axios pour lancer des requêtes http et accéder au backend de l'application.

## [husky](https://typicode.github.io/husky/)

Nous utilisons husky et son système de pre-commit pour lancer des scripts au moment de chaque commit git. Exemple : un linter, des tests...

## [zustand](https://zustand-demo.pmnd.rs/)

Nous utilisons zustand pour avoir accès à un state commun à travers toute l'application à l'aide de son système de store.

## [jest](https://jestjs.io/fr/)

Nous utilisons jest pour écrire les tests des composants, garantir la stabilité de l’interface utilisateur et détecter rapidement les régressions.

Au moment des pull requests sur les branches majeures du répertoire git, les tests sont lancés, et s'ils échouent, la PR ne peut pas être validé, et la personne qui a fait la PR doit faire fonctionner les tests avant de pouvoir déployer son code.