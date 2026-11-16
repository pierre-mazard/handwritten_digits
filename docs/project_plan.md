# Plan de projet

## Présentation

L'objectif du projet est de développer une solution complète de classification de chiffres manuscrits à partir de la base de données MNIST.

Le projet suit une démarche scientifique reposant sur :

- une baseline classique avec Scikit-Learn ;
- l'étude d'un perceptron multicouche (MLP) ;
- l'étude d'un réseau convolutif (CNN) ;
- le déploiement du meilleur modèle dans une application Flask.

---

# Objectifs

## Objectif principal

Construire un classifieur de chiffres manuscrits performant et reproductible.

---

## Objectifs de performance

### Baseline

Obtenir une référence de performance à l'aide d'un modèle classique.

---

### MLP

Objectif :

```text
Erreur < 2 %
```

sur le jeu de test.

---

### CNN

Objectif :

```text
Erreur < 1 %
```

sur le jeu de test.

---

### Flask

Permettre à un utilisateur :

- d'envoyer une image ;
- d'obtenir une prédiction ;
- d'obtenir les probabilités associées aux 10 classes.

---

# Contraintes du sujet

- séparation stricte entraînement / validation / test ;
- reproductibilité des résultats ;
- comparaison scientifique des expériences ;
- utilisation de Python ;
- utilisation de Scikit-Learn ;
- utilisation de TensorFlow / Keras ;
- utilisation de Flask.

---

# Répartition prévisionnelle

## Membre 1

- Infrastructure du projet
- CI/CD
- Baseline
- Expérimentations MLP

## Membre 2

- CNN
- Flask
- Tests
- Documentation

---

# Livrables

- Documentation complète
- Notebooks reproductibles
- Modèles sauvegardés
- Application Flask fonctionnelle
- Tests automatisés
- Dépôt GitHub documenté

---

# Critères de réussite

- Baseline documentée
- MLP inférieur à 2 % d'erreur
- CNN inférieur à 1 % d'erreur
- Application Flask fonctionnelle
- Tests unitaires validés
- Reproductibilité démontrée