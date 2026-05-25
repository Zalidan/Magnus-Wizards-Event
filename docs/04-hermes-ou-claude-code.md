# 04 — Utiliser Claude Code ou Hermes Agent

## Option A — Claude Code

C'est le chemin le plus simple pour tester.

Prompt de démarrage :

```txt
Tu es mon assistant de clipping. Lis les fichiers dans ce dossier. Commence par analyser input/transcript.md avec le prompt templates/clip-selector.prompt.md. Écris le résultat dans outputs/selected-clips.md. Ensuite, attends ma validation avant de packager les clips.
```

Avantage : rapide, peu de setup.

Limite : moins adapté aux workflows réguliers et automatisés.

## Option B — Hermes Agent

Hermes est plus adapté si tu veux construire un vrai assistant réutilisable.

Exemple de logique :

```txt
1. Créer une skill clipping-agent
2. Lui donner les prompts de sélection et de packaging
3. Définir un dossier input/output
4. Ajouter une checklist qualité
5. Automatiser progressivement les étapes répétitives
```

Commandes utiles côté Hermes :

```bash
hermes
hermes skills list
hermes skills create
hermes cron list
```

> Les commandes exactes peuvent varier selon ton installation. Réfère-toi à la documentation Hermes Agent.

## Conseil

Si tu débutes : commence avec Claude Code.

Si tu veux construire un système qui tourne chaque semaine : passe ensuite à Hermes.
