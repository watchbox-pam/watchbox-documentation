# Packages backend

Le backend de l'application Watchbox utilise un certain nombre de packages pour fonctionner.

Ces packages sont répertoriés dans le fichier requirements.txt et doivent être installés avec pip : 
```bash
pip install -r requirements.txt
```

Voici les principaux plugins utilisés :

## [fastapi](https://fastapi.tiangolo.com/)

Le backend de l'application Watchbox, construit en python, utilise le framework FastAPI pour concevoir des API REST performantes, bénéficier d’une documentation automatique et faciliter la maintenance du code.

FastAPI permet de créer des endpoints qui seront exposés pour que le frontend puisse y accéder.

Ces endpoints sont répertoriés à l'aide d'une documentation [Swagger](https://swagger.io/) ou [ReDoc](https://redocly.com/), respectivement aux endpoints /docs et /redoc du serveur backend.

## [pytest](https://docs.pytest.org/en/stable/)

Nous utilisons également pytest pour écrire des tests et garantir la stabilité du code tout au long du développement.

Au moment des pull requests sur les branches majeures du répertoire git, les tests sont lancés, et s'ils échouent, la pr ne peut pas être validé, et la personne qui a fait la pr doit faire fonctionner les tests avant de pouvoir déployer son code.

## [psycopg](https://www.psycopg.org/)

Les données de l'application Watchbox sont stockées dans une base de données PostgreSQL. Pour accéder à ces données depuis le backend python, nous utilisons psycopg pour assurer une communication fiable et performante avec la base de données PostgreSQL.