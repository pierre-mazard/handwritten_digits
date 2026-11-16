# Guide de contribution

Merci de contribuer au projet **MNIST Digit Classifier**.

L'objectif est de maintenir un projet propre, reproductible et facile à comprendre pour tous les membres de l'équipe.

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
docs/project-structure
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

## 6. Committer

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
- avoir des tests fonctionnels ;
- être relue par un membre de l'équipe.

---

## 9. Fusion dans develop

Après validation :

- fusionner dans `develop` ;
- supprimer la branche devenue inutile ;
- mettre à jour sa branche locale.

---

# Convention de commits

Les messages de commit suivent la convention **Conventional Commits**.

## Nouvelle fonctionnalité

```text
feat: ajout d'une fonctionnalité
```

Exemple :

```text
feat: implement first cnn architecture
```

## Correction

```text
fix: correction d'un bug
```

Exemple :

```text
fix: correct image preprocessing
```

## Documentation

```text
docs: mise à jour de la documentation
```

Exemple :

```text
docs: update installation guide
```

## Tests

```text
test: ajout ou modification de tests
```

Exemple :

```text
test: add flask endpoint tests
```

## Refactorisation

```text
refactor: amélioration interne sans changement fonctionnel
```

Exemple :

```text
refactor: simplify training pipeline
```

## Intégration continue

```text
ci: modification des workflows github actions
```

Exemple :

```text
ci: add automated test workflow
```

## Maintenance

```text
chore: tâches de maintenance ou configuration
```

Exemple :

```text
chore: configure pre-commit hooks
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