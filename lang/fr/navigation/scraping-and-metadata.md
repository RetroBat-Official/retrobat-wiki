# Scrape & Métadonnées

Le scrape télécharge les informations (nom, description, date de sortie, genre…) et les médias (images, vidéos, manuels, cartes…) de vos jeux depuis des bases de données en ligne.

## Services de scrape

<table><thead><tr><th width="262.75">Service</th><th>Compte</th></tr></thead><tbody><tr><td><a href="https://www.screenscraper.fr/">ScreenScraper</a> (par défaut)</td><td>Compte gratuit recommandé (plus rapide, moins de limites)</td></tr><tr><td><a href="https://thegamesdb.net/">TheGamesDB</a></td><td>Non nécessaire</td></tr><tr><td><a href="https://db.hfsplay.fr/">HFSDB</a></td><td>Non nécessaire</td></tr><tr><td>ArcadeDB</td><td>Non nécessaire (jeux d'arcade uniquement)</td></tr><tr><td><a href="https://www.igdb.com/">IGDB</a></td><td><strong>Obligatoire</strong> : Client ID et Client Secret, voir Configurer IGDB</td></tr></tbody></table>

## Informations récupérées

* Informations du jeu : nom, description, date de sortie, développeur, éditeur, genre, nombre de joueurs, note…
* Images : boîte (2D ou 3D), dos de la boîte, capture d'écran ou écran titre, logo, fan art, carte, cartouche, décoration (16:9)
* Vidéo
* Manuel
* Paramètres PadToKey

## Comment scraper

* **Tous les jeux ou plusieurs systèmes** : voir [Scrape global](../premiers-pas/adding-a-game.md#scrape-global).
* **Un seul jeu** : voir [Scrape individuel](../premiers-pas/adding-a-game.md#scrape-individuel-par-jeu).

## Le menu Scrapeur

Ouvrez **MENU PRINCIPAL** > **SCRAPEUR**. Le menu comporte trois onglets.

<div align="left"><figure><img src="../.gitbook/assets/image (296).png" alt=""><figcaption></figcaption></figure></div>

### Onglet SCRAPER

<table><thead><tr><th width="296.5">Paramètre</th><th>Description</th></tr></thead><tbody><tr><td><strong>SCRAPER DEPUIS</strong></td><td>Service à utiliser</td></tr><tr><td><strong>JEUX À SCRAPER</strong></td><td>Tous les jeux, jeux avec des médias manquants, ou jeux sans aucun média</td></tr><tr><td><strong>IGNORER LES JEUX SCRAPÉS RÉCEMMENT</strong></td><td>Ne pas scraper les jeux scrapés la veille, la semaine passée, le mois passé…</td></tr><tr><td><strong>SYSTÈMES INCLUS</strong></td><td>Systèmes à scraper</td></tr><tr><td><strong>SCRAPER MAINTENANT</strong></td><td>Lancer le scrape</td></tr></tbody></table>

### Onglet OPTIONS

Les réglages disponibles dépendent du service choisi.

<div align="left"><figure><img src="../.gitbook/assets/image (297).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="192.75">Section</th><th>Réglages</th></tr></thead><tbody><tr><td>Paramètres</td><td><strong>IMAGE SOURCE</strong> (capture, écran titre, mix, boîte…), <strong>BOÎTE SOURCE</strong> (boîte 2D ou 3D), <strong>LOGO SOURCE</strong> (logo, logo HD, bannière), <strong>RÉGION PRÉFÉRÉE</strong>, <strong>ÉCRASER LES NOMS / DESCRIPTIONS / MÉDIAS</strong></td></tr><tr><td>Scraper</td><td>Médias et informations à télécharger : nom court, notes de la communauté, vidéo, fan art, décoration (16:9), arrière des boîtes, carte, écran titre, cartouche, manuel, paramètres PadToKey</td></tr><tr><td>Scrape manuel</td><td><strong>SCRAPERS INCLUS</strong> : services interrogés quand vous scrapez un seul jeu</td></tr></tbody></table>

{% hint style="info" %}
Laissez **ÉCRASER LES NOMS / DESCRIPTIONS / MÉDIAS** désactivés si vous avez modifié vos jeux à la main : sinon vos modifications seront remplacées.
{% endhint %}

### Onglet COMPTES

<div align="left"><figure><img src="../.gitbook/assets/image (298).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="164">Section</th><th>Réglages</th></tr></thead><tbody><tr><td>ScreenScraper</td><td><strong>NOM D'UTILISATEUR</strong> et <strong>MOT DE PASSE</strong> de votre compte <a href="https://www.screenscraper.fr/">ScreenScraper</a></td></tr><tr><td>IGDB</td><td><strong>ID CLIENT</strong> et <strong>SECRET CLIENT</strong>, voir ci-dessous</td></tr></tbody></table>

## Configurer IGDB

IGDB appartient à Twitch : pour l'utiliser, vous devez créer une « application » (gratuite) sur le site développeur de Twitch, qui vous fournit un **Client ID** et un **Client Secret**.

1. **Créez un compte Twitch** sur [twitch.tv](https://www.twitch.tv/) si vous n'en avez pas, et validez votre adresse e-mail.
2. **Activez l'authentification à deux facteurs (2FA)** : **Paramètres** Twitch > **Sécurité et confidentialité** > **Configurer l'authentification à deux facteurs** (un numéro de téléphone est nécessaire). La console développeur ne fonctionne pas sans 2FA.
3. Ouvrez la [console développeur Twitch](https://dev.twitch.tv/console) et connectez-vous.
4. Dans l'onglet **Applications**, cliquez sur **Register Your Application** et remplissez le formulaire :
   * **Name** : un nom unique, par exemple `retrobat-` suivi de caractères au hasard (si le nom est déjà pris, la création échoue)
   * **OAuth Redirect URLs** : `http://localhost`
   * **Category** : **Application Integration**
   * **Client Type** : **Confidential**
5. Validez le captcha, puis cliquez sur **Create**.
6. Dans la liste des applications, cliquez sur **Manage** sur votre application :
   * copiez le **Client ID** ;
   * cliquez sur **New Secret**, confirmez, puis copiez le **Client Secret**.
7. Dans RetroBat, ouvrez **MENU PRINCIPAL** > **SCRAPEUR** > **COMPTES** et saisissez l'**ID CLIENT** et le **SECRET CLIENT** dans la section **IGDB**.
8. Dans l'onglet **SCRAPER**, choisissez **IGDB** dans **SCRAPER DEPUIS**.

{% hint style="info" %}
**Plus simple que la saisie à la manette :** fermez RetroBat, ouvrez `emulationstation\.emulationstation\es_settings.cfg` avec un éditeur de texte, et ajoutez (ou complétez) ces deux lignes :

```xml
<string name="IGDBClientID" value="votre client id" />
<string name="IGDBSecret" value="votre client secret" />
```
{% endhint %}

{% hint style="warning" %}
* Gardez votre Client Secret pour vous.
* Cliquer à nouveau sur **New Secret** crée un nouveau secret et invalide le précédent : il faut alors le saisir à nouveau dans RetroBat.
{% endhint %}

## Stockage des médias téléchargés

Les médias sont stockés dans le dossier de chaque système, dans des sous-dossiers. Chaque fichier porte le nom du fichier du jeu, suivi du type de média.

<div align="left"><figure><img src="../.gitbook/assets/image (299).png" alt=""><figcaption></figcaption></figure></div>

<table data-header-hidden><thead><tr><th width="139.5"></th><th width="259"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier</strong></td><td><strong>Médias</strong></td><td>Exemple pour <code>roms\snes\Super Metroid.zip</code></td></tr><tr><td><code>images</code></td><td>Boîte, dos de boîte, capture, logo, fan art, carte, cartouche, écran titre, décoration…</td><td><code>images\Super Metroid-thumb.png</code>, <code>-image</code>, <code>-marquee</code>, <code>-fanart</code>, <code>-boxback</code>, <code>-box</code>, <code>-wheel</code>, <code>-map</code>, <code>-cartridge</code>, <code>-titleshot</code>, <code>-bezel</code></td></tr><tr><td><code>videos</code></td><td>Vidéos</td><td><code>videos\Super Metroid-video.mp4</code></td></tr><tr><td><code>manuals</code></td><td>Manuels (PDF)</td><td><code>manuals\Super Metroid-manual.pdf</code></td></tr><tr><td><code>magazines</code></td><td>Magazines</td><td><code>magazines\Super Metroid-magazine.pdf</code></td></tr></tbody></table>

Les informations des jeux et les liens vers les médias sont enregistrés dans le fichier `gamelist.xml` du dossier du système (par exemple `roms\snes\gamelist.xml`).

## Utiliser vos propres médias

Vous pouvez utiliser des images et vidéos que vous avez déjà, ou que vous avez créées vous-même.

1. Nommez chaque fichier exactement comme le fichier du jeu (sans son extension), suivi du type de média :

<table><thead><tr><th>Fichier</th><th width="229.5">Média</th><th>Dossier</th></tr></thead><tbody><tr><td><code>Super Metroid-thumb.png</code></td><td>Boîte</td><td><code>images</code></td></tr><tr><td><code>Super Metroid-image.png</code></td><td>Image du jeu (capture)</td><td><code>images</code></td></tr><tr><td><code>Super Metroid-marquee.png</code></td><td>Logo</td><td><code>images</code></td></tr><tr><td><code>Super Metroid-video.mp4</code></td><td>Vidéo</td><td><code>videos</code></td></tr></tbody></table>

2. Copiez les fichiers dans le dossier `images` ou `videos` du système (par exemple `roms\snes\images`). Les images peuvent être en `.png` ou `.jpg`.
3. Activez **RECHERCHER DES VISUELS LOCAUX** dans **MENU PRINCIPAL** > **PARAMÈTRES SYSTÈME** > **OPTIONS DÉVELOPPEUR** > **GESTION DES DONNÉES**.

<div align="left"><figure><img src="../.gitbook/assets/image (300).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Vos fichiers ne sont utilisés que si le jeu n'a pas déjà un média de ce type dans la liste de jeux. Pour utiliser vos propres médias sur un jeu déjà scrapé, associez-les avec **ÉDITER LES MÉTADONNÉES DU JEU** (voir ci-dessous).
{% endhint %}

## Modifier les métadonnées d'un jeu

Dans le menu [Options du jeu](game-options.md), choisissez **ÉDITER LES MÉTADONNÉES DU JEU** :

<div align="left"><figure><img src="../.gitbook/assets/image (301).png" alt=""><figcaption></figcaption></figure></div>

Vous pouvez :

* modifier les informations du jeu : nom, description, note, date de sortie, développeur, éditeur, famille de jeu, genres, système d'arcade, nombre de joueurs, langues, région ;
* associer d'autres fichiers de médias (image, vidéo, logo, boîte, fan art, manuel, carte…) ;
* ajouter le jeu aux favoris ;
* masquer le jeu ;
* marquer le jeu comme **jeu pour enfants**, pour l'afficher en [mode Enfant](../utilisation-avancee/kiosk-and-kid-mode.md#mode-enfant).
