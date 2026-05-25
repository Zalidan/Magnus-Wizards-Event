# 02 — Architecture simple

Voici l'architecture publique recommandée.

```txt
[input]
  video.mp4 ou transcript.md
      ↓
[Agent 1] Clip Selector
  Sortie : passages candidats
      ↓
[Agent 2] Packaging
  Sortie : titre, hook, angle, CTA
      ↓
[Agent 3] Quality Gate
  Sortie : publier / retravailler / jeter
      ↓
[Humain ou script]
  Montage, sous-titres, publication
```

## Pourquoi plusieurs agents ?

Parce qu'un seul prompt qui fait tout devient vite moyen partout.

Mieux vaut séparer :

- la sélection ;
- le packaging ;
- la vérification qualité.

## Version Claude Code

Claude Code peut lire les fichiers du dossier, appliquer les prompts, écrire les sorties dans `outputs/`, puis t'aider à itérer.

## Version Hermes Agent

Hermes peut aller plus loin :

- conserver des skills ;
- lancer des workflows récurrents ;
- manipuler des fichiers ;
- utiliser des outils système ;
- automatiser certaines étapes.

Dans cette version publique, on reste volontairement sur une architecture simple.
