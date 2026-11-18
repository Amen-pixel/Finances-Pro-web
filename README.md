<div align="center">

# Finances Pro Web

**Gérez vos finances projet par projet : revenus, dépenses, épargne et objectifs. Depuis un simple lien, sur téléphone comme sur ordinateur.**

[![Ouvrir l'application](https://img.shields.io/badge/Ouvrir%20l'application-00C26B?style=for-the-badge)](https://amen-pixel.github.io/Finances-Pro-web/)

![PWA](https://img.shields.io/badge/PWA-installable-5A0FC8)
![JavaScript](https://img.shields.io/badge/JavaScript-natif-F7DF1E?logo=javascript&logoColor=black)
![Hors ligne](https://img.shields.io/badge/Fonctionne-hors%20ligne-brightgreen)
![Dépendances](https://img.shields.io/badge/Dépendances-0-blue)
![Hébergement](https://img.shields.io/badge/Hébergé%20sur-GitHub%20Pages-181717?logo=github)

</div>

---

## Présentation

**Finances Pro Web** est la version web de l'application de bureau [Finances Pro](https://github.com/Amen-pixel/finances-pro). Le principe reste le même : **un dossier par projet** (un achat, un voyage, un fonds d'urgence, un budget familial…). Dans chaque projet, vous suivez vos revenus, vos dépenses et votre épargne, et l'application vous montre où vous en êtes avec des graphiques et des conseils automatiques.

- **Aucun téléchargement** depuis un store : ouvrez le lien, c'est prêt.
- **Aucun compte, aucun serveur** : vos données restent sur votre appareil.
- **Installable** sur l'écran d'accueil, comme une vraie application.
- **Utilisable hors ligne** une fois ouvert une première fois.

<!-- Ajoutez vos captures d'écran dans un dossier docs/ puis décommentez ce bloc :
<p align="center">
  <img src="docs/accueil.png" width="30%">
  <img src="docs/tableau-de-bord.png" width="30%">
  <img src="docs/repartition.png" width="30%">
</p>
-->

## Essayer l'application

**https://amen-pixel.github.io/Finances-Pro-web/**

### Installer sur votre téléphone

| Appareil | Étapes |
|---|---|
| **Android** (Chrome) | Ouvrez le lien, appuyez sur le menu **⋮**, faites défiler jusqu'à **Installer l'application** (ou **Ajouter à l'écran d'accueil**), puis confirmez. |
| **iPhone** (Safari) | Ouvrez le lien, appuyez sur **Partager**, puis sur **Sur l'écran d'accueil**. |
| **Ordinateur** (Chrome, Edge) | Cliquez sur l'icône d'installation à droite de la barre d'adresse. |

L'application s'ouvre ensuite en plein écran, avec son icône « FP ».

## Fonctionnalités

### Projets
- Un projet par objectif, avec un **nom**, un **type** (Épargne, Objectif, Maison, Voiture, Études, Informatique, Voyage, Courses, Téléphone, Cadeau, Santé, Croissance) et une **couleur**.
- **Budget mensuel de dépenses** et **objectif d'épargne** par projet, avec barres de progression.
- Totaux cumulés de tous vos projets sur l'écran d'accueil.

### Opérations
- Trois types : **Revenu**, **Dépense** et **Épargne**.
- 11 catégories prêtes à l'emploi (Alimentation, Transport, Loyer, Santé, Éducation…) et une date par opération.
- **Export CSV** au même format que la version Windows : `Date;Description;Catégorie;Type;Montant`.

### Analyse et visualisation

Huit rubriques par projet, chacune sur sa **propre page plein écran** :

| Onglet | Ce qu'il apporte |
|---|---|
| **Tableau de bord** | Saisie d'une opération, dépenses par catégorie, taux d'épargne, budget du mois |
| **Historique** | Liste des opérations, filtre par type, suppression, export CSV |
| **Courbe** | Évolution chronologique par type d'opération, avec option *Cumulé* |
| **Répartition** | Diagramme circulaire par catégorie, avec légende et pourcentages |
| **Mensuel** | Revenus, dépenses et épargne sur les 12 derniers mois, avec le net de chaque mois |
| **Analyse** | Score de santé, dépense moyenne par jour, prévision de fin de mois, plus grosse dépense, catégorie dominante, conseils automatiques |
| **Objectifs** | Deux calculateurs : pour l'objectif du projet et pour un achat libre. Choisissez de cotiser par jour, semaine, mois ou an pour connaître la durée et la date, ou fixez un délai pour connaître le montant à cotiser |
| **Réglages du projet** | Nom, budget mensuel, objectif d'épargne, suppression du projet |

### Rapport, sécurité et confort
- **Rapport (PDF)** : le bouton ouvre l'impression du navigateur, où vous choisissez *Enregistrer en PDF*.
- **Code PIN** pour verrouiller l'accès à l'application. Il est enregistré sous forme d'empreinte (SHA-256), jamais en clair.
- **Sauvegarde et restauration** de toutes vos données dans un fichier `.json`.
- **Thème sombre ou clair**, adapté aux petits écrans.

## Vos données

Tout est enregistré **dans le navigateur de votre appareil** (stockage local). Rien n'est envoyé sur Internet.

- Chaque personne a ses propres données : personne d'autre ne voit les vôtres.
- Les données sont liées à un **appareil et à un navigateur**. Si vous changez de téléphone, ou si vous videz les données du navigateur, elles sont perdues.
- **Utilisez régulièrement le bouton « Sauvegarde »** de l'écran d'accueil, puis copiez le fichier sur une clé USB ou un cloud. Le bouton **Restaurer** les remet en place.
- Le **code PIN** empêche quelqu'un d'ouvrir l'application depuis votre téléphone déverrouillé, mais il **ne chiffre pas** les données du navigateur. Ce n'est pas une protection contre un attaquant expérimenté.

## Différences avec la version Windows

La version web reprend l'essentiel de [Finances Pro pour Windows](https://github.com/Amen-pixel/finances-pro). Ne sont pas encore disponibles :

- les opérations récurrentes (loyer, abonnement…) ;
- la modification d'une opération déjà saisie, et l'annulation d'une suppression ;
- l'import CSV et la recherche parmi les projets ;
- la sauvegarde automatique à la fermeture (remplacée par la sauvegarde manuelle).

## Technologies

- **HTML, CSS et JavaScript natifs** : un seul fichier `index.html`, sans framework ni bibliothèque.
- **PWA** : `manifest.webmanifest` et service worker (`sw.js`) pour l'installation et le mode hors ligne.
- **Graphiques en SVG** générés directement par le code.
- **Hébergement gratuit** sur GitHub Pages, sans serveur ni base de données.

## Structure du projet

```
Finances-Pro-web/
├── index.html              # application complète (interface, styles, logique)
├── manifest.webmanifest    # informations d'installation (nom, couleurs, icônes)
├── sw.js                   # service worker : mode hors ligne et mises à jour
├── icon-192.png            # icône de l'application
├── icon-512.png            # icône grande taille
└── README.md
```

## Lancer en local

Aucune installation n'est nécessaire. Le service worker demande de passer par un petit serveur local :

```bash
git clone https://github.com/Amen-pixel/Finances-Pro-web.git
cd Finances-Pro-web
python -m http.server 8000
```

Ouvrez ensuite `http://localhost:8000` dans votre navigateur.

## Déployer sa propre copie

1. Faites un *fork* du dépôt, ou créez un dépôt **public** avec les fichiers.
2. Allez dans **Settings**, puis **Pages**.
3. Choisissez la source **Deploy from a branch**, la branche `main` et le dossier `/ (root)`, puis **Save**.
4. Après une à deux minutes, votre lien apparaît en haut de la page.

Pour mettre à jour, modifiez les fichiers et faites un *commit* : le site se redéploie tout seul. Le service worker charge d'abord la dernière version en ligne, et garde une copie pour le mode hors ligne.

## Navigateurs compatibles

Chrome, Edge, Firefox, Opera et Samsung Internet sur Android et ordinateur, Safari sur iPhone et Mac. Sur iPhone, l'installation sur l'écran d'accueil se fait uniquement depuis Safari.

## Auteur

Développé par **Amen Quenum** ([@Amen-pixel](https://github.com/Amen-pixel)).

Une question, une idée, un bug ? Ouvrez une [*issue*](../../issues).

## Licence

Ce projet est distribué sous licence **MIT**. Voir le fichier `LICENSE` pour plus de détails.
