# Mettre en place un apprentissage semi-supervisé

L'objectif ici est d'explorer la possibilité d'automatiser la détection de tumeurs au cerveau. Un ensemble conséquent de radios a été collecté : la majorité de ces images ne dispose d’aucun étiquetage, tandis qu’un sous-ensemble limité a été annoté par des radiologues experts.

## Problématique 

La mission est :
- d'explorer les images et extraire des caractéristiques visuelles via un modèle pré-entraîné
- d'appliquer des méthodes de clustering pour identifier des structures ou regroupements dans les données
- de mettre en œuvre une méthode d’apprentissage semi-supervisé à partir des quelques étiquettes disponibles
- de synthétiser vos résultats, formuler des recommandations

## Données utilisées

Nous avons à disposition plusieurs dossiers :
- Un dossier contenant 50 images médicales avec le label "normal".
- Un dossier contenant 50 images médicales avec le label "cancer".
- Un dossier contenant 1406 images médicales sans label.

## Organisation du projet
```
├── Data
│   ├── Raw/          # Données brutes mais pas affiché sur GitHub car trop volumineux
│   └── Processed/    # Données nettoyées et préparées
│
├── notebooks/        # Étapes du projet sous forme de notebooks
│   ├── notebook_1_analyse_exploratoire.ipynb
│   ├── notebook_2_pretraitement_donnees.ipynb
│
├── README.md         # Documentation du projet
└── pyproject.toml    # Dépendances et configuration
```

### Installation et utilisation
1. Cloner le projet :
``` 
git clone https://github.com/SCFlorian/Apprentissage_semi_supervise.git
cd Apprentissage_semi_supervise
```
2. Installer les dépendances :
Le projet utilise pyproject.toml pour la gestion des dépendances.
```
poetry install
```
3. Ouvrir le projet dans VS Code
```
code .
```
4. Configurer l’environnement Python dans VS Code
	1.	Installez l’extension Python (si ce n’est pas déjà fait).
	2.	Appuyez sur Ctrl+Shift+P (Windows/Linux) ou Cmd+Shift+P (Mac).
	4.	Recherchez “Python: Select Interpreter”.
	5.	Sélectionnez l’environnement créé par Poetry ou celui dans lequel tu as installé le projet.

5. Travailler avec les notebooks
- Les notebooks se trouvent dans le dossier :
```
notebooks/
```

- Ouvrez n’importe quel fichier .ipynb (ex. notebook_1_analyse_exploratoire.ipynb).
- VS Code activera automatiquement l’éditeur interactif Jupyter.
- Vous pouvez exécuter les cellules avec Shift+Enter.