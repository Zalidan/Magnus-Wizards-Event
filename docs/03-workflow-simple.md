# 03 — Workflow simple en 45 minutes

Objectif : produire 3 à 5 idées d'extraits solides depuis un contenu long.

## Pré-requis

- Une transcription horodatée, même imparfaite.
- Claude Code ou Hermes Agent.
- Un dossier de travail.

Exemple :

```txt
my-clipping-test/
├── input/
│   └── transcript.md
├── outputs/
└── prompts/
```

## Étape 1 — Préparer la transcription

Place la transcription dans `input/transcript.md`.

Format conseillé :

```md
[00:01:12] Arthur explique pourquoi YouTube reste sous-exploité en affiliation...
[00:02:45] Exemple d'un élève qui a utilisé une vidéo pour générer des ventes...
```

## Étape 2 — Sélectionner les passages

Utilise : [`templates/clip-selector.prompt.md`](../templates/clip-selector.prompt.md)

Demande à l'agent de produire une sortie JSON ou Markdown avec :

- timestamp de début ;
- timestamp de fin ;
- résumé ;
- raison du potentiel ;
- score simple sur 10.

## Étape 3 — Packager les meilleurs clips

Prends seulement les 3 à 5 meilleurs passages.

Utilise : [`templates/packaging.prompt.md`](../templates/packaging.prompt.md)

Sortie attendue :

- hook ;
- titre ;
- angle ;
- description courte ;
- CTA possible.

## Étape 4 — Passer la checklist qualité

Utilise : [`checklists/quality-checklist.md`](../checklists/quality-checklist.md)

Si un clip ne passe pas la checklist, ne le publie pas.

## Étape 5 — Monter et publier

Cette partie peut rester manuelle au début.

Le but de la V1 n'est pas l'automatisation complète. Le but est de valider que la sélection éditoriale est bonne.

## Règle importante

Ne cherche pas à automatiser un mauvais jugement éditorial. Commence par obtenir de bons choix de clips, puis automatise.
