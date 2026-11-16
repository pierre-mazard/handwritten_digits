# Décisions d'architecture

## ADR-001 : Gestion des dépendances

Décision :

Utilisation d'UV pour la gestion des dépendances Python.

Justification :

- rapidité ;
- reproductibilité ;
- simplicité d'installation.

---

## ADR-002 : Workflow Git

Décision :

Utilisation des branches :

- main
- develop
- feature/*
- fix/*
- docs/*

Justification :

Permettre le développement parallèle et les revues de code.

---

## ADR-003 : Organisation du code

Décision :

Séparation du projet en plusieurs modules :

```text
data/
models/
training/
evaluation/
utils/
```

Justification :

Faciliter la maintenance et la réutilisation du code.