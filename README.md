# MNIST Digit Classifier

Projet de classification de chiffres manuscrits utilisant la base de données MNIST.

Ce projet est réalisé dans le cadre du Master IA et a pour objectif de comparer différentes approches de classification :

- Baseline classique avec Scikit-Learn
- Réseau de neurones dense (MLP)
- Réseau de neurones convolutif (CNN)
- Déploiement du meilleur modèle via une application Flask

---

# Membres du projet

- Bastoini Rifka
- Mazard Pierre

---

# Contexte

La base de données MNIST (Modified National Institute of Standards and Technology) est un jeu de données de référence pour la classification d'images.

Elle contient :

- 60 000 images d'entraînement
- 10 000 images de test
- Images en niveaux de gris
- Taille : 28 × 28 pixels
- 10 classes (chiffres de 0 à 9)

L'objectif est d'analyser différents modèles de Machine Learning et Deep Learning afin de comprendre leurs performances, leurs limites et leur comportement.

---

# Objectifs du projet

## Palier 1 : Baseline classique

- Chargement et exploration de MNIST
- Analyse de la répartition des classes
- Prétraitement des données
- Régression logistique ou forêt aléatoire
- Matrice de confusion
- Analyse des erreurs

---

## Palier 2 : Réseau dense (MLP)

Étude de plusieurs configurations :

- profondeur du réseau
- largeur des couches
- learning rate
- optimiseur
- batch size

Analyse :

- loss d'entraînement
- loss de validation
- overfitting
- Early Stopping
- Dropout
- Batch Normalization

Objectif :

```text
Erreur < 2 % sur le jeu de test
```

---

## Palier 3 : Réseau convolutif (CNN)

Étude :

- architecture CNN
- pooling
- nombre de filtres
- augmentation de données
- visualisation des couches convolutives
- analyse des erreurs

Objectif :

```text
Erreur < 1 % sur le jeu de test
```

---

## Palier 4 : Application Flask

Déploiement du meilleur modèle :

- chargement du modèle sauvegardé
- prédiction d'images
- affichage des probabilités
- gestion des erreurs
- tests automatisés

---

# Technologies utilisées

## Langage principal

- Python

## Machine Learning

- Scikit-Learn
- TensorFlow
- Keras

## Visualisation

- Matplotlib
- Seaborn

## Application Web

- Flask

## Tests

- Pytest

## Qualité de code

- Ruff
- Pre-commit

## Gestion des dépendances

- UV

---

# Structure du projet

```text
mnist-digit-classifier/

├── .github/
│   └── workflows/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── models/
│
├── docs/
│
├── notebooks/
│
├── reports/
│   ├── experiments/
│   └── figures/
│
├── src/
│   ├── data/
│   ├── evaluation/
│   ├── models/
│   ├── training/
│   └── utils/
│
├── flask_app/
│
├── tests/
│
├── README.md
├── CONTRIBUTING.md
├── pyproject.toml
└── LICENSE
```

---

# Installation

## Cloner le dépôt

```bash
git clone https://github.com/organisation/mnist-digit-classifier.git
```

```bash
cd mnist-digit-classifier
```

## Créer l'environnement virtuel

```bash
uv venv
```

### Linux / Mac

```bash
source .venv/bin/activate
```

### Windows

```bash
.venv\Scripts\activate
```

## Installer les dépendances

```bash
uv sync
```

---

# Qualité de code

Analyse statique :

```bash
ruff check .
```

Formatage :

```bash
ruff format .
```

Tests :

```bash
pytest
```

---

# Reproductibilité

Afin de garantir la reproductibilité des expériences :

- les dépendances sont figées dans le projet ;
- les graines aléatoires sont fixées ;
- les expériences sont documentées ;
- les résultats sont enregistrés dans le dossier `reports/`.

Exemple :

```python
SEED = 42
```

```python
random.seed(SEED)
numpy.random.seed(SEED)
tensorflow.random.set_seed(SEED)
```

---

# Résultats

## Baseline Scikit-Learn

À compléter.

---

## Meilleur MLP

À compléter.

---

## Meilleur CNN

À compléter.

---

# Documentation

La documentation détaillée du projet est disponible dans :

```text
docs/
```

et

```text
reports/
```

---

# Workflow Git

Le projet utilise :

```text
main
develop
feature/*
fix/*
docs/*
release/*
```

Les règles de contribution sont décrites dans :

```text
CONTRIBUTING.md
```

---

# Licence

Ce projet est distribué sous licence MIT.

Voir :

```text
LICENSE
```