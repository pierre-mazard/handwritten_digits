# Workflow GitHub

# Branches principales

## main

Branche stable du projet.

Elle contient uniquement les fonctionnalités validées et prêtes à être livrées.

---

## develop

Branche d'intégration.

Toutes les nouvelles fonctionnalités sont fusionnées dans cette branche avant leur intégration dans `main`.

---

# Branches secondaires

## feature/*

Développement de nouvelles fonctionnalités.

Exemples :

```text
feature/exploration-mnist
feature/mlp-learning-rate
feature/cnn-data-augmentation
```

---

## fix/*

Corrections de bugs.

Exemples :

```text
fix/image-normalization
fix/flask-validation
```

---

## docs/*

Modifications de la documentation.

Exemples :

```text
docs/update-readme
docs/project-report
```

---

## ci/*

Amélioration de l'intégration continue ou des workflows GitHub.

Exemples :

```text
ci/add-github-actions
ci/update-workflow
```

---

# Cycle de développement

```text
Issue GitHub
        ↓
Création d'une branche
        ↓
Développement
        ↓
Commit(s)
        ↓
Push
        ↓
Pull Request
        ↓
GitHub Actions
        ↓
Revue de code
        ↓
Squash and Merge
        ↓
develop
```

---

# Cycle de livraison

```text
develop
        ↓
Validation complète
        ↓
Pull Request
        ↓
Squash and Merge
        ↓
main
```

---

# Revue de code

Toute Pull Request doit :

- être relue par un collaborateur ;
- passer les vérifications automatiques ;
- respecter les conventions du projet ;
- être associée à une ou plusieurs Issues.

---

# Gestion des Issues

Chaque Issue doit :

- appartenir à une Milestone ;
- être associée à un label ;
- être suivie dans le Kanban GitHub.

Organisation du Kanban :

```text
Backlog
À faire
En cours
En revue
Terminé
```

---

# Qualité logicielle

Le projet utilise :

- Ruff
- Pre-Commit
- GitHub Actions
- Pytest

afin de garantir la qualité et la stabilité du code.

---

# Intégration continue

La pipeline CI exécute automatiquement :

```text
ruff check
ruff format --check
pytest
```

Les Pull Requests doivent passer toutes les vérifications avant d'être fusionnées.

---

# Protection des branches

Les branches principales sont protégées :

## main

- Pull Request obligatoire
- Validation obligatoire
- Vérifications CI obligatoires

## develop

- Pull Request obligatoire
- Vérifications CI obligatoires

Aucun développement ne doit être effectué directement sur ces branches.