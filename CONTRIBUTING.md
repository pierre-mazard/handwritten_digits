# Guide de contribution

Merci de contribuer au projet **Handwritten Digits Classifier**.

L'objectif est de maintenir un projet propre, reproductible, documenté et facile à comprendre pour tous les membres de l'équipe.

---

# Gestion du projet

Le suivi du projet est réalisé à l'aide des outils GitHub suivants :

- GitHub Projects
- GitHub Issues
- GitHub Milestones
- Pull Requests

Chaque tâche doit être associée à :

- une Issue ;
- une Milestone (Sprint) ;
- un responsable ;
- un statut dans le Kanban.

Les développements doivent être réalisés à partir d'une Issue existante.

---

# Workflow Git

Le projet utilise les branches suivantes :

| Branche | Description |
|----------|-------------|
| main | Version stable et validée du projet |
| develop | Branche d'intégration principale |
| feature/* | Développement de nouvelles fonctionnalités |
| fix/* | Correction de bugs |
| docs/* | Mise à jour de la documentation |
| ci/* | Configuration de l'intégration continue |
| release/* | Préparation d'une version majeure |

---

# Convention de nommage des branches

Toutes les branches doivent être créées à partir de `develop`.

## Nouvelles fonctionnalités

```bash
feature/nom-fonctionnalite
```

Exemples :

```text
feature/exploration-mnist
feature/baseline-sklearn
feature/mlp-learning-rate
feature/cnn-data-augmentation
feature/flask-upload
```

## Corrections

```bash
fix/nom-correction
```

Exemples :

```text
fix/image-normalization
fix/confusion-matrix
```

## Documentation

```bash
docs/nom-documentation
```

Exemples :

```text
docs/readme-update
docs/project-report
```

## Intégration continue

```bash
ci/nom-amelioration
```

Exemples :

```text
ci/add-github-actions
ci/update-workflow
```

---

# Processus de développement

## 1. Mettre à jour la branche develop

```bash
git checkout develop
git pull origin develop
```

## 2. Créer une branche de travail

```bash
git checkout -b feature/nom-fonctionnalite
```

ou

```bash
git checkout -b fix/nom-correction
```

ou

```bash
git checkout -b docs/nom-documentation
```

ou

```bash
git checkout -b ci/nom-amelioration
```

## 3. Développer la fonctionnalité

Respecter l'organisation des dossiers du projet :

```text
src/
tests/
docs/
notebooks/
reports/
```

Toute fonctionnalité importante doit être documentée.

---

## 4. Vérifier la qualité du code

Avant chaque commit :

```bash
ruff check .
```

```bash
ruff format .
```

```bash
pytest
```

Les erreurs signalées doivent être corrigées avant de poursuivre.

---

## 5. Ajouter les modifications

Ajouter tous les fichiers :

```bash
git add .
```

Ou uniquement certains fichiers :

```bash
git add chemin/fichier.py
```

---

## 6. Réaliser un commit

Les commits doivent suivre la convention définie ci-dessous.

Exemple :

```bash
git commit -m "feat: add sklearn baseline"
```

---

## 7. Pousser la branche

```bash
git push origin nom-branche
```

---

## 8. Ouvrir une Pull Request

Toute modification doit passer par une Pull Request.

La Pull Request doit :

- décrire les changements réalisés ;
- expliquer le problème résolu ;
- indiquer les éventuels impacts ;
- être associée à une ou plusieurs Issues ;
- avoir des tests fonctionnels ;
- être relue par un membre de l'équipe.

---

# Stratégie de fusion

Les modifications sont intégrées via Pull Request.

## Squash and Merge

Méthode recommandée pour ce projet.

Elle permet :

- de conserver un historique clair ;
- de regrouper plusieurs commits intermédiaires ;
- de simplifier la lecture de l'historique Git.

---

## Rebase and Merge

Peut être utilisé lorsque l'historique de la branche est déjà propre et cohérent.

---

## Merge Commit

À éviter autant que possible afin de conserver un historique lisible.

---

## Règle du projet

La stratégie recommandée est :

```text
Squash and Merge
```

sauf exception justifiée.

---

## 9. Fusion dans develop

Après validation :

- fusionner dans `develop` ;
- supprimer la branche devenue inutile ;
- mettre à jour sa branche locale.

---

# Fermeture des Issues

Une Pull Request doit référencer les Issues concernées.

Exemples :

```text
Closes #12
Closes #15
```

ou

```text
Fixes #12
```

Les Issues seront alors fermées automatiquement après la fusion.

---

# Convention de commits

Les messages de commit suivent la convention **Conventional Commits**.

## Nouvelle fonctionnalité

```text
feat: ajout d'une fonctionnalité
```

## Correction

```text
fix: correction d'un bug
```

## Documentation

```text
docs: mise à jour de la documentation
```

## Tests

```text
test: ajout ou modification de tests
```

## Refactorisation

```text
refactor: amélioration interne sans changement fonctionnel
```

## Intégration continue

```text
ci: modification des workflows GitHub Actions
```

## Maintenance

```text
chore: tâches de maintenance ou configuration
```

---

# Reproductibilité

Le sujet impose une démarche scientifique reproductible.

Les règles suivantes doivent être respectées :

- utilisation d'UV pour la gestion des dépendances ;
- conservation du fichier `pyproject.toml` à jour ;
- fixation des graines aléatoires ;
- documentation des expériences réalisées ;
- conservation des résultats importants dans le dossier `reports/`.

---

# Documentation des expérimentations

Toute expérimentation significative doit être documentée :

- configuration du modèle ;
- hyperparamètres ;
- durée d'entraînement ;
- métriques obtenues ;
- conclusions.

Les résultats seront centralisés dans :

```text
reports/
```

et

```text
docs/
```

---

# Structure du projet

```text
src/            Code source
tests/          Tests automatisés
notebooks/      Analyses et expérimentations
docs/           Documentation
reports/        Résultats et figures
data/           Données et modèles sauvegardés
flask_app/      Application web Flask
```

---

Merci de respecter ces règles afin de garantir la qualité, la lisibilité et la reproductibilité du projet.