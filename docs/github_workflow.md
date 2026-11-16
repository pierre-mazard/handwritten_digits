# Workflow GitHub

## Branches principales

### main

Branche stable du projet.

Elle contient uniquement les fonctionnalités validées.

---

### develop

Branche d'intégration.

Toutes les nouvelles fonctionnalités sont fusionnées ici avant d'être intégrées dans main.

---

## Branches secondaires

### feature/*

Développement de nouvelles fonctionnalités.

Exemples :

```text
feature/mlp-learning-rate
feature/cnn-data-augmentation
```

---

### fix/*

Corrections de bugs.

Exemples :

```text
fix/image-normalization
fix/flask-validation
```

---

### docs/*

Modifications de la documentation.

Exemples :

```text
docs/update-readme
docs/project-report
```

---

## Cycle de développement

```text
feature/*
        ↓
 Pull Request
        ↓
    develop
        ↓
 Pull Request
        ↓
      main
```

---

## Revue de code

Toute Pull Request doit :

- être relue par un collaborateur ;
- passer les vérifications automatiques ;
- respecter les conventions du projet.

---

## Qualité logicielle

Le projet utilise :

- Ruff
- Pre-Commit
- GitHub Actions
- Pytest

afin de garantir la qualité et la stabilité du code.