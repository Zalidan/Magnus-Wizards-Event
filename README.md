# Magnus — Public Clipping Kit

> Construire un assistant IA simple pour transformer un contenu long en extraits courts exploitables.

Ce dépôt accompagne le **Wizards Event**. Il montre la logique derrière Magnus : comment passer d'une vidéo longue à une liste d'extraits, puis à des angles, titres, descriptions et checklists de publication.

L'objectif n'est pas de livrer notre pipeline interne complet. C'est une version publique, pédagogique et reproductible pour démarrer avec **Hermes Agent** ou **Claude Code**.

---

## Ce que tu vas apprendre

- Penser le clipping comme un **système éditorial**, pas comme une simple découpe vidéo.
- Découper le travail en agents spécialisés : sélection, packaging, qualité, publication.
- Créer une première version semi-automatique avec Claude Code.
- Comprendre comment passer ensuite vers une automatisation Hermes.

## Ce que ce kit ne contient pas

Par choix, cette version publique ne contient pas :

- notre pipeline de production exact ;
- nos scores internes ;
- notre logique complète de miniatures, tracking, publication et backlog ;
- nos intégrations privées Studio / Zernio / analytics.

Ces éléments restent réservés aux accompagnements avancés et à la Wizards Academy.

## Démarrage rapide

1. Lis [`docs/01-vision.md`](docs/01-vision.md)
2. Suis le workflow dans [`docs/03-workflow-simple.md`](docs/03-workflow-simple.md)
3. Copie les prompts dans [`templates/`](templates/)
4. Teste sur une transcription courte de 10 à 20 minutes
5. Utilise [`checklists/quality-checklist.md`](checklists/quality-checklist.md) avant publication

## Structure

```txt
docs/        Explication du système et du workflow
templates/   Prompts copiables pour Claude Code ou Hermes
examples/    Exemple de formats de sortie
checklists/  Critères qualité avant publication
```

## Le principe en une image

```txt
Contenu long
   ↓
Transcription horodatée
   ↓
Sélection des passages forts
   ↓
Packaging éditorial : hook, titre, angle
   ↓
Montage / sous-titres
   ↓
Publication
   ↓
Retour qualité et amélioration
```

## Licence d'usage

Tu peux utiliser ce kit pour construire ta propre première version. Évite simplement de le revendre tel quel comme une formation ou un produit sans ajout substantiel.
