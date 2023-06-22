# Scrape & Metadonnées

Le scrape permet de récupérer les informations et les médias des jeux de votre bibliothèque (images, vidéos, cartes, fichiers pad2key et manuels).

4 bases de données peuvent être scrapées:

* ScreenScraper (par défaut) : inscription requise sur le site web [screenscraper](https://www.screenscraper.fr/)
* [TheGamesDB](https://thegamesdb.net/)
* [HFSDB](https://db.hfsplay.fr/)
* ArcadeDB

### **Informations scrapées**

* Informations générales du jeu (titre, année de parution, nombre de joueurs, description...)
* Note
* Vignette (boîtier)
* Logo / bannière
* Vidéo
* Fanart
* Image (écran titre ou capture en jeu)
* Dos du boîtier
* Carte
* Manuel utilisateur
* Fichier pad2key

### Comment scraper ?

Le scrape peut être effectué globalement (pour tous les systèmes) ou pour un seul jeu.

#### Scrape global

Aller à la [section dédiée du wiki](../premiers-pas/adding-a-game.md#scrape-global).

#### Scrape individuel

Aller à la [section dédiée du wiki](../premiers-pas/adding-a-game.md#scrape-individuel-par-jeu).



### Options de scrape

Les options de scrape sont accessibles dans le [**MENU PRINCIPAL**](main-menu.md#parametres-des-jeux) en sélectionnant **SCRAPEUR:**

<div align="left">

<figure><img src="https://i.imgur.com/9CFSkvg.png" alt=""><figcaption></figcaption></figure>

</div>

Avant de démarrer le scrape, il est possible de:

* choisir la base de données à scraper
* ne scraper que les jeux ayant des médias manquants
* ignorer les jeux scrapés récemment
* limiter les systèmes à scraper

Chaque scrapeur possède également des réglages qui lui sont propre:

<div align="left">

<figure><img src="https://i.imgur.com/aGCeQUh.jpg" alt=""><figcaption></figcaption></figure>

</div>

Il est notamment possible de définir:

* le type de média à télécharger en tant que fichier "image" (image titre, capture en jeu...)
* le type d'image à utiliser pour représenter le boîtier (2D, 3D, etc.)
* le type d'image à utiliser comme logo (logo, bannière)

{% hint style="info" %}
Les paramètres de connexion au service Screenscraper doivent être renseigné dans les options du scrapeur.
{% endhint %}

### Stockage des médias téléchargés

Tous les médias téléchargés sont stockés dans le dossier des jeux (répertoire `\roms`)

<div align="left">

<figure><img src="https://i.imgur.com/XlUVX8L.png" alt=""><figcaption><p>Exemple</p></figcaption></figure>

</div>

<table><thead><tr><th width="199">Répertoire</th><th>Média stocké</th></tr></thead><tbody><tr><td>images</td><td>boîtier (thumb), fanart, dos du boîtier (boxback), image, logo (marquee), carte (map)</td></tr><tr><td>manuals</td><td>Manuel utilisateur</td></tr><tr><td>videos</td><td>Vidéo mp4</td></tr></tbody></table>

###

### Utiliser des médias locaux

Il est également possible d'utiliser des images et vidéos déjà disponible sur votre ordinateur, ou que vous auriez crées vous-même.\
\
Pour cela, il faudra :

* Renommer les médias exactement comme le jeu,
* Rajouter l'extension de fichier correspondant au type de média :
  * _nom\_du\_jeu_**-thumb** pour un visuel correspondant au boitier
  * _nom\_du\_jeu_**-image** pour un visuel correspondant à une image du jeu
  * _nom\_du\_jeu_**-marquee** pour un visuel correspondant au logo du jeu
  * _nom\_du\_jeu_**-video.mp4** pour une vidéo.
* Placer les médias dans un répertoire nommé "**images**" pour les images, et "**videos**" pour des vidéos
* Depuis les [**PARAMÈTRES SYSTÈMES**](main-menu.md#parametres-systeme), dans  "**options développeur**", activer l'option "**Rechercher des visuels complémentaires**"

<figure><img src="https://i.imgur.com/pTTYZa0.png" alt=""><figcaption></figcaption></figure>



### Gestion des métadonnées du jeu

Le menu [Options du Jeu](game-options.md) permet également de modifier manuellement les métadonnées des jeux:

<div align="left">

<figure><img src="https://i.imgur.com/PfePfik.png" alt=""><figcaption></figcaption></figure>

</div>

**Il est possible de :**

* Mettre à jour les informations générales (titre, description, note, date de sortie, développeur, éditeur, famille de jeu, genres, système d'arcade, nombre de joueurs, langue et région)
* Modifier les médias (attacher d'autres images)
* Ajouter le jeu aux favoris
* Masquer le jeu
* Etiquetter le jeu "enfant" afin de le faire apparaître dans l'[interface Enfant](../utilisation-avancee/kiosk-and-kid-mode.md#mode-enfant)
