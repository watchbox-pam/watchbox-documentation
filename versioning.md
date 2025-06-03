# Versioning de l'application

Pour gérer le code de l'application, nous utilisons Git, et publions le code sur Github.

Nous avons créé [une organisation](https://github.com/watchbox-pam) sur Github, ou nos repositories sont publiés.

Le code est séparé en 2 repositories : 
- [watchbox-app](https://github.com/watchbox-pam/watchbox-app), pour le frontend de l'application en React Native
- [watchbox-back](https://github.com/watchbox-pam/watchbox-back), pour le backend de l'application en Python

## Branches

Il y a deux branches principales dans les répertoires de l'application.
- main, la branche de base qui sert de branche de production
- develop, la branche qui sert à fusionner le code des différents développeurs afin de faire des tests avant les passages en production

### Nommage des branches

Jira, notre outil de suivi de projet, peut être relié à Github afin de lier des tickets à des branches particulières. <br/>
Pour cela, les branches doivent être nommées de la façon suivante : 'WBX-(numéro de ticket)-(description courte)'. Exemple : `git checkout -b WBX-47-profile`

## Commits

Pour nommer les commits, nous utilisons des [Gitmojis](https://gitmoji.dev/). Le principe consiste simplement à rajouter un émoji au début du nom d'un commit afin que tout le monde puisse rapidement comprendre ce qu'un développeur a fait dans un commit particulier. Exemple : `git commit -m "📝 Added documentation about versioning"`

## Pull requests

Une fois qu'un développeur estime que ses modifications sont satisfaisantes, il pourra envoyer son code sur la branche develop pour faire des tests avant un passage en production.

Pour cela, il devra : 
- mettre sa branche à jour avec la branche develop, en faisant un `git merge` ou un `git rebase`
- créer une pull request de sa branche vers la branche develop dans Github

Pour que la pr puisse être acceptée, il faudra que : 
- les différents checks (tests unitaires, builds...) soit passés
- un autre développeur approuve les modifications effectuées, et valide la pr

Une fois que la pr a été mergée, la branche est supprimée.

Pour faire des pull requests sur la branche main et passer du code en production, le système sera le même : 
- la pull request est effectuée depuis la branche develop vers la branche main
- cette fois-ci, le code devra être approuvé par 2 développeurs avant que la pull request puisse être validée