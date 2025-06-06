# Architecture Backend

Le backend de l'application Watchbox utilise une implémentation de la Clean Architecture. Les différentes couches de l'application sont séparées afin de garantir une meilleure lisibilité, maintenabilité et évolutivité du code.


```
📦watchbox-back
 ┣ 📂.github
 ┃ ┗ 📂workflows
 ┣ 📂.venv
 ┣ 📂api
 ┃ ┣ 📂auth
 ┃ ┣ 📜server.py
 ┃ ┗ 📜xxx_router.py
 ┣ 📂assets
 ┃ ┗ 📂images
 ┣ 📂domain
 ┃ ┣ 📂interfaces
 ┃ ┃ ┣ 📂repositories
 ┃ ┃ ┃ ┗ 📜i_xxx_repository.py
 ┃ ┃ ┗ 📂services
 ┃ ┃   ┗ 📜i_xxx_service.py
 ┃ ┗ 📂models
 ┃   ┗ 📜model.py
 ┣ 📂repository
 ┃  ┗ 📜xxx_repository.py
 ┣ 📂service
 ┃  ┗ 📜xxx_service.py
 ┣ 📂tests
 ┃ ┣ 📂api
 ┃ ┃ ┗ 📜test_xxx_router.py
 ┃ ┣ 📂repository
 ┃ ┃ ┗ 📜test_xxx_repository.py
 ┃ ┣ 📂service
 ┃ ┃ ┗ 📜test_xxx_service.py
 ┃ ┗ 📂utils
 ┣ 📂utils
 ┣ 📜.env
 ┣ 📜.env.example
 ┣ 📜.gitignore
 ┣ 📜Deploy-Back.md
 ┣ 📜Deploy-Database.md
 ┣ 📜Dockerfile
 ┣ 📜README.md
 ┣ 📜db_config.py
 ┣ 📜main.py
 ┣ 📜pytest.ini
 ┣ 📜requirements.txt
 ┣ 📜runtime.txt
 ┣ 📜setup.py
 ┗ 📜startup.txt
 ```

## .github/workflows

Dossier qui contient les [workflows github](https://docs.github.com/fr/actions/writing-workflows), pour pouvoir
- lancer différents checks (builds, tests) avant la validation d'une pull request
- lancer un script de dépliement automatique après la validation d'une pr
- etc...

## api

Dossier qui contient les controllers du backend, c'est à dire la définition des endpoints du backend de l'application.

### auth

Contient le système d'authentification de l'application, qui sera ajouté comme middleware sur les routes à sécuriser.

## assets

Les assets inclus dans l'application (images...)

## domain

### interfaces

#### repositories

La définition des interfaces pour les repositories.

#### services

La définition des interfaces pour les services.

### models

Les définitions des modèles de données utilisés comme classe à travers le backend de l'application. Utilisés pour structurer et valider les données reçues et envoyées.

## repositories

La couche de l'application qui permet l'accès aux données peut importe leur source. Dans ce cas : base de données PostgreSQL ou api TMDB.
    
## services

La couche de l'application qui contient toute la logique métier.

## tests

Les tests unitaires de l'application qui servent à assurer la fiabilité du code.

## utils

Des fichiers contenant des fonctions qui peuvent être réutilisées à travers l'application.
