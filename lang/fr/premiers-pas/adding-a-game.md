---
description: Construire votre ludothèque
---

# Ajouter des jeux

L'ajout de jeux est très simple.

{% hint style="warning" %}
RetroBat ne fournit aucun jeu. Vous devez utiliser vos propres sauvegardes de jeux (ROMs).
{% endhint %}

## Ajouter un jeu

Placez vos fichiers de jeux (ROMs) dans le dossier du système correspondant, à l'intérieur du dossier `roms` de RetroBat :

`<dossier RetroBat>\roms\<système>\`

Par exemple, un jeu Super Nintendo se place dans `C:\RetroBat\roms\snes\`.

<div align="left"><figure><img src="../.gitbook/assets/image (226).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Le nom du dossier doit correspondre exactement au système (par exemple `snes`, et non `Super Nintendo`). Le nom du dossier et les formats de fichiers acceptés pour chaque système sont indiqués dans la section [Systèmes compatibles](../systemes-and-emulateurs/supported-game-systems/).

Certains systèmes nécessitent aussi des fichiers BIOS pour fonctionner : voir [Ajouter les BIOS](ajouter-les-bios.md).

Pour stocker vos jeux ailleurs (autre disque, NAS…), voir [Liens symboliques](../tutoriels/liens-symboliques.md).
{% endhint %}

Les nouveaux jeux sont détectés au prochain démarrage de RetroBat, ou lors de la mise à jour des listes de jeux (**MENU PRINCIPAL** > **PARAMÈTRES DES JEUX** > **METTRE À JOUR LES LISTES DE JEUX**).

Le système apparaît alors dans la **Vue Système**.

<div align="left"><figure><img src="../.gitbook/assets/image (227).png" alt=""><figcaption></figcaption></figure></div>

Appuyez sur ![](<../.gitbook/assets/image (20) (1).png>) pour afficher la liste des jeux dans la [Vue Jeux](../navigation/system-view-and-game-view.md#vue-jeux).

<div align="left"><figure><img src="../.gitbook/assets/image (228).png" alt=""><figcaption></figcaption></figure></div>

## Scraper les informations des jeux

L'étape suivante consiste à scraper les informations des jeux : votre ludothèque sera bien plus agréable avec des images, des vidéos et des descriptions.

Le scrape peut être effectué pour tous les systèmes (global), par système ou par jeu.

### Scrape global

Appuyez sur **START** (**ENTRÉE** au clavier) pour afficher le **MENU PRINCIPAL**, puis sélectionnez **SCRAPEUR**.

<div align="left"><figure><img src="../.gitbook/assets/image (229).png" alt=""><figcaption></figcaption></figure></div>

Configurez les **OPTIONS DU SCRAPEUR**, puis choisissez **SCRAPER MAINTENANT**.

<div align="left"><figure><img src="../.gitbook/assets/image (230).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Pour utiliser ScreenScraper, nous recommandons de créer un compte gratuit sur le [site ScreenScraper](https://www.screenscraper.fr/), puis de saisir vos identifiants (utilisateur / mot de passe) dans l'onglet **COMPTES**.

Plus d'informations dans la section [Scrape & Métadonnées](../navigation/scraping-and-metadata.md).
{% endhint %}

Pendant le scrape, le message ci-dessous s'affiche en haut à droite de l'écran.

<div align="left"><figure><img src="https://i.imgur.com/V7ng0Nd.png" alt=""><figcaption><p>Scrape en cours</p></figcaption></figure></div>

Une fois le scrape terminé, mettez à jour les listes de jeux : appuyez sur **START** (**ENTRÉE** au clavier) pour afficher le Menu Principal, choisissez **PARAMÈTRES DES JEUX**…

<div align="left"><figure><img src="../.gitbook/assets/image (231).png" alt=""><figcaption></figcaption></figure></div>

… puis **METTRE À JOUR LES LISTES DE JEUX**.

<div align="left"><figure><img src="../.gitbook/assets/image (232).png" alt=""><figcaption></figcaption></figure></div>

Les informations des jeux sont désormais affichées dans la Vue Jeux.

<div align="left"><figure><img src="../.gitbook/assets/image (233).png" alt=""><figcaption></figcaption></figure></div>

### Scrape individuel (par jeu)

Pour scraper un seul jeu, sélectionnez-le dans la Vue Jeux et maintenez ![](<../.gitbook/assets/image (20) (1).png>) appuyé pour afficher les Options du jeu, puis choisissez **SCRAPER**.

<div align="left"><figure><img src="../.gitbook/assets/image (234).png" alt=""><figcaption></figcaption></figure></div>

Une liste de jeux pouvant correspondre s'affiche. Sélectionnez le bon jeu et confirmez avec ![](<../.gitbook/assets/image (20) (1).png>).

{% hint style="info" %}
Par défaut, la recherche utilise le nom du fichier du jeu. Pour chercher avec un autre nom, utilisez l'option **EDITER** en bas de l'écran.
{% endhint %}

<div align="left"><figure><img src="../.gitbook/assets/image (235).png" alt=""><figcaption></figcaption></figure></div>

**Félicitations !** Vous avez ajouté vos premiers jeux à RetroBat. Étape suivante : Démarrer un jeu.
