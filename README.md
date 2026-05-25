# Magnus Public Clipping Kit

> Le kit public pour comprendre comment transformer une vidéo longue en machine à contenus courts avec l'IA.

Une conférence, un podcast, un live, une masterclass : la plupart des créateurs publient le contenu long, puis laissent mourir 80% de sa valeur.

Magnus part du principe inverse.

Dans un bon contenu long, il y a déjà des dizaines de moments courts : une preuve, une punchline, une méthode, une objection, une histoire, un déclic. Le problème n'est pas de "faire des Shorts". Le problème est de repérer les bons moments, de leur donner un angle, puis de les publier proprement.

Ce dépôt te donne une version publique et simple de cette logique.

Pas notre pipeline interne complet. Pas nos intégrations privées. Pas la machine entière.

Mais assez pour construire ton premier assistant de clipping avec **Claude Code** ou **Hermes Agent**.

---

## Ce que Magnus fait vraiment

Magnus n'est pas un monteur vidéo.

C'est un système éditorial.

Il aide à répondre à 5 questions :

1. Quels passages méritent vraiment d'être extraits ?
2. Pourquoi quelqu'un s'arrêterait dessus dans son feed ?
3. Quel angle rend le passage plus désirable ?
4. Est-ce que le clip sert un objectif business clair ?
5. Est-ce qu'on doit publier, retravailler ou jeter ?

La découpe vidéo arrive après. Le jugement éditorial vient d'abord.

---

## Le pipeline public

```txt
Contenu long
   ↓
Transcription horodatée
   ↓
Sélection des passages forts
   ↓
Packaging : hook, titre, angle, CTA
   ↓
Contrôle qualité
   ↓
Montage et publication
```

La version avancée de Magnus va beaucoup plus loin : automatisation, backlog, scoring, publication, tracking, itérations.

Cette version publique se concentre sur le coeur : obtenir de meilleurs choix de clips.

Parce qu'automatiser de mauvais clips ne crée pas un système. Ça crée juste du bruit plus vite.

---

## Pour qui ?

Ce kit est pour toi si tu as :

- un podcast ;
- une chaîne YouTube ;
- des lives ;
- des webinaires ;
- des formations ;
- des interviews ;
- des conférences ;
- des vidéos longues qui dorment dans un disque dur.

Et si tu veux en tirer des extraits qui servent quelque chose : audience, autorité, preuve, acquisition, vente.

---

## Ce que tu vas trouver ici

```txt
docs/
  01-vision.md                 Comprendre la logique Magnus
  02-architecture.md           Les briques du système
  03-workflow-simple.md        Une V1 faisable en 45 minutes
  04-hermes-ou-claude-code.md  Deux chemins pour construire ton agent
  05-adapter-a-son-business.md Relier les clips à un objectif business

templates/
  clip-selector.prompt.md      Repérer les meilleurs passages
  packaging.prompt.md          Transformer un passage en angle publiable
  quality-gate.prompt.md       Refuser les clips faibles

checklists/
  quality-checklist.md         Vérification avant publication

examples/
  selected-clips-example.md    Exemple de sortie attendue
```

---

## Démarrage rapide

### Option 1 : tu veux tester vite avec Claude Code

1. Crée un dossier avec une transcription dans `input/transcript.md`.
2. Copie les prompts du dossier `templates/`.
3. Demande à Claude Code d'appliquer `clip-selector.prompt.md`.
4. Garde seulement les 3 à 5 meilleurs passages.
5. Applique `packaging.prompt.md`.
6. Passe chaque clip dans `quality-gate.prompt.md`.

Prompt de départ :

```txt
Lis input/transcript.md.
Utilise templates/clip-selector.prompt.md pour identifier les meilleurs extraits.
Écris la sortie dans outputs/selected-clips.md.
Ne cherche pas à faire beaucoup de clips : je veux les meilleurs.
```

### Option 2 : tu veux construire un agent avec Hermes

Hermes est plus adapté si tu veux transformer cette logique en assistant réutilisable.

L'idée : créer une skill de clipping, lui donner les prompts, définir un dossier de travail, puis automatiser les étapes répétitives.

Commence simple :

```txt
input/transcript.md
   → sélection
   → packaging
   → quality gate
   → outputs/final-clips.md
```

Ensuite seulement, tu ajoutes montage, publication, calendrier, analytics.

---

## La règle qui change tout

Ne demande pas à l'IA :

```txt
Découpe-moi 10 Shorts.
```

Demande plutôt :

```txt
Analyse ce contenu comme un éditeur.
Trouve les passages qui peuvent vivre seuls, créer de la curiosité ou prouver quelque chose.
Refuse les passages moyens.
```

La différence est énorme.

La première demande produit du volume.

La seconde produit du jugement.

---

## Exemple de résultat attendu

Un bon extrait candidat doit ressembler à ça :

```md
## Clip — YouTube reste sous-exploité en affiliation

- Début : 00:12:10
- Fin : 00:13:35
- Pourquoi ça peut marcher : contraste fort entre une opportunité connue et une exécution rarement maîtrisée.
- Type : désir / autorité
- Angle : "Le canal que tout le monde regarde, mais que peu de gens exploitent correctement."
- Verdict : publiable après packaging.
```

Ce n'est pas encore une vidéo.

C'est mieux : c'est une décision éditoriale.

---

## Ce qu'on garde volontairement privé

Ce dépôt est public. Il est donc volontairement incomplet.

Tu ne trouveras pas ici :

- notre architecture de production exacte ;
- nos scores internes ;
- nos prompts avancés ;
- notre logique complète de miniatures ;
- notre système de backlog ;
- nos automatisations de publication ;
- nos intégrations privées ;
- nos boucles d'analyse de performance.

Ce kit est une porte d'entrée.

La version complète, celle qui transforme ce principe en vraie machine opérationnelle, reste réservée à nos accompagnements privés et à la Wizards Academy.

---

## Commence ici

Si tu veux comprendre la logique :

👉 [`docs/01-vision.md`](docs/01-vision.md)

Si tu veux tester tout de suite :

👉 [`docs/03-workflow-simple.md`](docs/03-workflow-simple.md)

Si tu veux copier les prompts :

👉 [`templates/`](templates/)

Si tu ne dois retenir qu'une phrase :

> Un bon système de clipping ne cherche pas plus de clips. Il cherche de meilleures décisions.
