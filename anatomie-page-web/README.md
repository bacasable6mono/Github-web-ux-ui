# Anatomie d’une page web

Support de cours interactif (format 16:9) pour des étudiants de 2ᵉ année de BUT Communication : atomiser la page d’accueil de l’ENT Ernest (Université de Strasbourg), nommer ses composants et comprendre son environnement (URL, serveur, identification).

## Contenu du dépôt

```
index.html                  la présentation (HTML, CSS et JS dans un seul fichier)
assets/ernest.jpg           la capture pleine page utilisée par toutes les diapositives
assets/components.js        les 40 éléments repérés : coordonnées, définition, rôle, bonne pratique
assets/lexique.js           le lexique (103 termes, 6 catégories)
assets/fonts/               Manrope (variable, auto-hébergée)
anatomie-page-web.pdf       la version PDF
```

## Mise en ligne avec GitHub Pages

1. Créer un dépôt sur GitHub et y déposer le contenu de ce dossier (le fichier `.nojekyll` inclus).
2. *Settings › Pages › Build and deployment* : source « Deploy from a branch », branche `main`, dossier `/ (root)`.
3. La présentation est publiée à l’adresse `https://<compte>.github.io/<depot>/`.

Pour un test en local, lancer un petit serveur dans le dossier (`python3 -m http.server`) : certains navigateurs bloquent les polices si l’on ouvre `index.html` directement.

## Navigation

- flèches ← →, espace ou glissement sur écran tactile : diapositive précédente / suivante ;
- `O` : sommaire ; `F` : plein écran ; `#12` à la fin de l’adresse ouvre directement la diapositive 12 ;
- sur les diapositives annotées, le survol d’une légende met en évidence l’élément sur la capture, et inversement.

Diapositives propres à l’écran : l’explorateur cliquable, le lexique avec recherche, le quiz. Dans le PDF, elles sont remplacées par le lexique paginé, un exercice à compléter et son corrigé.

## Régénérer le PDF

Ouvrir `index.html?print` dans Chrome, puis *Imprimer › Enregistrer au format PDF* (marges : aucune, graphismes d’arrière-plan cochés). Le format de page 1920 × 1080 px est défini dans la feuille de style.

## Modifier le contenu

- Ajouter ou corriger un terme : `assets/lexique.js`.
- Ajouter un élément repéré : `assets/components.js` (`box` = x, y, largeur, hauteur en pixels de la capture d’origine, 2896 × 5287 px).
- Changer de capture : remplacer `assets/ernest.jpg`, mettre à jour `IW` et `IH` dans `index.html`, puis les coordonnées.

Capture : page d’accueil de la plateforme Ernest, Université de Strasbourg, 5 novembre 2026, utilisée à des fins pédagogiques.
