# Lancement du projet

## Récupération du projet

Pour récupérer le projet, cloner le repository git
```bash
git clone https://github.com/watchbox-pam/watchbox-back.git
```

## Préparation du projet

Ajouter un environnement virtuel au projet avec la commande
```bash
python -m venv /path/to/new/virtual/environment
```

Puis l'activer avec `source .venv/bin/activate` pour MacOS / Linux ou `.venv\Scripts\activate` pour Windows.

## Lancement du projet

Ouvrir le projet dans un éditeur de code comme VsCode ou un IDE comme PyCharm.

Ajouter les variables d'environnement au fichier .env.

Installer les packages pip nécessaires au lancement du projet avec la commande
```bash
pip install -r requirements.txt
```

Lancer la commande `fastapi dev main.py` pour lancer le projet. 