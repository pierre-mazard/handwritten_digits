# Planification des sprints

## Sprint 0 — Initialisation du projet

Objectif :

Mettre en place l'infrastructure de développement.

### Tâches

- Création du dépôt GitHub
- Création de l'arborescence
- Configuration UV
- Configuration Ruff
- Configuration Pre-Commit
- Mise en place de la documentation
- Mise en place du workflow Git

---

## Sprint 1 — Exploration et Baseline

Objectif :

Découvrir les données et établir un point de référence.

### Tâches

- Chargement de MNIST
- Analyse exploratoire
- Vérification de la répartition des classes
- Prétraitement des données
- Création du découpage train / validation / test
- Régression logistique ou forêt aléatoire
- Matrice de confusion
- Analyse des erreurs

### Validation

- Notebook reproductible
- Matrice de confusion
- Erreur de validation calculée

---

## Sprint 2 — MLP

Objectif :

Construire un réseau dense performant.

### Tâches

- Premier modèle MLP
- Étude du learning rate
- Étude du batch size
- Étude des optimiseurs
- Étude du surapprentissage
- Early Stopping
- Dropout
- Batch Normalization

### Validation

- Comparaison d'au moins 4 configurations
- Courbes d'entraînement
- Tableau comparatif
- Évaluation sur le test

---

## Sprint 3 — CNN

Objectif :

Construire un réseau convolutif performant.

### Tâches

- Première architecture CNN
- Comparaison avec le MLP
- Ablation pooling
- Ablation filtres
- Data augmentation
- Visualisation des convolutions
- Analyse des erreurs

### Validation

- Erreur inférieure à 1 %
- Analyse des performances

---

## Sprint 4 — Flask

Objectif :

Déployer le meilleur modèle.

### Tâches

- Chargement du modèle au démarrage
- Upload d'image
- Prédiction
- Affichage des probabilités
- Gestion des erreurs

### Validation

- Interface fonctionnelle
- Prédictions correctes

---

## Sprint 5 — Tests et finalisation

Objectif :

Préparer le rendu final.

### Tâches

- Pytest
- Validation de l'application
- Vérifications de reproductibilité
- Nettoyage du dépôt
- Finalisation de la documentation

### Validation

- Tous les tests passent
- Documentation complète