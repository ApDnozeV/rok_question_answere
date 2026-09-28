# ⚔️ Quiz d'Alliance — Rise of Kingdoms

Petit site statique regroupant les questions/réponses de l'événement **Quiz d'Alliance** du jeu *Rise of Kingdoms*, pour retrouver rapidement une réponse pendant la partie.

- 104 questions/réponses uniques (doublons retirés)
- Classement par catégorie : Jeu RoK, Histoire, Mythologie, Culture/Art/Sport, Sciences & Nature
- Recherche instantanée par mot-clé (insensible aux accents et à la casse)
- Un seul fichier HTML, sans dépendance, sans serveur, sans build
- Responsive (mobile et desktop)

> Projet de fans, non affilié à Lilith Games. *Rise of Kingdoms* est une marque de son propriétaire.

## Utilisation

Ouvre simplement `index.html` dans un navigateur. Aucune installation nécessaire.

## Ajouter ou modifier des questions

Toutes les données sont dans le fichier HTML, dans la balise `<script type="application/json" id="qa-data">`. Chaque question est un objet JSON :

```json
{
  "id": "e105",
  "category": "Histoire",
  "question": "Qui a fondé l'Empire mongol ?",
  "answer": "Gengis Khan"
}
```

| Champ      | Description                                                        |
|------------|--------------------------------------------------------------------|
| `id`       | Identifiant unique (ex. `e105`)                                    |
| `category` | Catégorie d'affichage. Une nouvelle catégorie crée une nouvelle section automatiquement |
| `question` | Texte de la question                                               |
| `answer`   | Texte de la réponse                                                |

Le site n'a pas besoin d'autre modification : la liste, les catégories et le compteur se mettent à jour tout seuls.

### Réponses à confirmer

Certaines réponses sont encore notées `Réponse A/B/C/D` (position du bon choix relevée sur une capture, pas son texte). Comme l'ordre des choix change d'une partie à l'autre, il vaut mieux les remplacer par le texte exact dès que possible.

## Publier sur GitHub Pages (gratuit)

1. Renomme le fichier en `index.html` à la racine du dépôt.
2. Sur GitHub : **Settings → Pages**.
3. Dans **Build and deployment**, choisis **Deploy from a branch**, branche `main`, dossier `/ (root)`.
4. Enregistre. Le site est disponible après une minute environ sur :
   `https://<ton-pseudo>.github.io/<nom-du-depot>/`

Alternative : glisser-déposer le fichier sur [Netlify Drop](https://app.netlify.com/drop) pour obtenir un lien public en quelques secondes.

## Structure

```
.
├── index.html   # le site complet (HTML + CSS + JS + données)
└── README.md
```

## Contribuer

Une question manquante ou une réponse erronée ? Ouvre une *issue* ou une *pull request* en modifiant le bloc `qa-data` de `index.html`.

## Licence

À définir (ex. MIT pour le code). Les questions proviennent du jeu et restent la propriété de leurs ayants droit.
