---
description: >-
  Classer les jeux d'un système dans des sous-dossiers et leur donner une image,
  un logo, une vidéo
---

# Créer des sous-dossiers de jeux

## Pourquoi des sous-dossiers ?

Dans le dossier d'un système (par exemple `roms\snes`), vous pouvez ranger vos jeux dans des sous-dossiers : hacks, homebrews, traductions, jeux par région, jeux eShop… RetroBat peut afficher ces sous-dossiers dans la liste de jeux, et vous pouvez les « habiller » avec une image, un logo, une boîte, une vidéo et une description, comme un jeu.

{% hint style="info" %}
Pour regrouper des jeux **sans déplacer leurs fichiers**, utilisez plutôt les collections personnalisées. Pour plus de détails, voir la page Collections.
{% endhint %}

## Créer les sous-dossiers

1. Fermez RetroBat.
2. Dans le dossier du système, créez un sous-dossier par catégorie et déplacez-y les jeux. Dans l'exemple de cette page, le dossier `roms\snes` contient trois sous-dossiers : `HACKS`, `HOMEBREWS` et `TRADS`.
3. Relancez RetroBat.

{% hint style="warning" %}
Les informations et les médias des jeux déjà scrapés sont liés au chemin du fichier du jeu dans `gamelist.xml`. Après avoir déplacé un jeu déjà scrapé, scrapez-le à nouveau, ou corrigez sa balise `<path>` dans `gamelist.xml` (RetroBat fermé, par exemple `./HACKS/Super Metroid Redesign.sfc`).
{% endhint %}

## Afficher les sous-dossiers

Par défaut, RetroBat n'affiche pas les dossiers : les jeux des sous-dossiers apparaissent tous ensemble dans la liste du système.

Pour afficher les dossiers dans tous les systèmes :

1. Appuyez sur **START** pour ouvrir le **MENU PRINCIPAL**.
2. Allez dans **PARAMÈTRES D'AFFICHAGE** > **OPTIONS DES LISTES DE JEUX**.
3. Réglez **AFFICHER LES DOSSIERS** sur **TOUJOURS**.

<div align="left"><figure><img src="../.gitbook/assets/image (745).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="220.25">Choix</th><th>Effet</th></tr></thead><tbody><tr><td><strong>JAMAIS</strong> (défaut)</td><td>Pas de dossiers : tous les jeux du système sont affichés dans une seule liste.</td></tr><tr><td><strong>TOUJOURS</strong></td><td>Chaque sous-dossier est affiché comme une entrée de la liste. Ouvrez-le avec <strong>SUD</strong>, revenez avec <strong>EST</strong>.</td></tr><tr><td><strong>AVEC JEUX MULTIPLES</strong></td><td>Seuls les dossiers qui contiennent plusieurs jeux sont affichés. Un dossier qui ne contient qu'un jeu est remplacé par ce jeu, un dossier vide est masqué.</td></tr></tbody></table>

Avec **AFFICHER LES DOSSIERS EN PREMIER** (activé par défaut, même menu), les dossiers sont placés en haut de la liste.

Pour afficher les dossiers dans un seul système : dans la liste de jeux de ce système, appuyez sur **SELECT**, puis allez dans **PERSONNALISER LA VUE** > **OPTIONS DES LISTES DE JEUX** > **AFFICHER LES DOSSIERS**. Ce réglage remplace, pour ce système, celui du **MENU PRINCIPAL** (**AUTO** utilise le réglage général). Pour plus de détails, voir la page Options d'affichage.

<div align="left"><figure><img src="../.gitbook/assets/image (744).png" alt=""><figcaption></figcaption></figure></div>

## Habiller les sous-dossiers

Un dossier peut recevoir les mêmes médias qu'un jeu. Trois méthodes, de la plus simple à la plus technique.

### Méthode 1 : depuis RetroBat (le plus simple)

1. Dans la liste de jeux, placez-vous sur le dossier.
2. Maintenez **SUD** pour ouvrir le menu **OPTIONS DU JEU** (ou appuyez sur **NORD** si l'option **ACCÉDER AUX OPTIONS DU JEUX AVEC LE BOUTON NORD** est activée).
3. Choisissez **ÉDITER LES MÉTADONNÉES DU DOSSIER**.
4. Renseignez le nom affiché, la description, et associez l'image, le logo, la boîte, la vidéo… comme pour un jeu.

<div align="left"><figure><img src="../.gitbook/assets/image (743).png" alt=""><figcaption></figcaption></figure></div>

RetroBat enregistre ces informations dans le `gamelist.xml` du système.

{% hint style="info" %}
L'entrée **SCRAPER** est aussi proposée sur un dossier, mais les services de scrape trouvent rarement un résultat pour un nom de dossier : préférez les méthodes de cette page.
{% endhint %}

### Méthode 2 : nommer les fichiers de médias

RetroBat peut trouver tout seul les médias d'un dossier s'ils portent le nom du dossier, suivi du type de média.

1. Activez **RECHERCHER DES VISUELS LOCAUX** dans **MENU PRINCIPAL** > **PARAMÈTRES SYSTÈME** > **OPTIONS DÉVELOPPEUR** > **GESTION DES DONNÉES**.
2. Dans le dossier du système (et non dans le sous-dossier), créez si besoin les dossiers `images` et `videos`. Ce sont les dossiers utilisés par le scrapeur : ils existent déjà si vous avez scrapé ce système.
3. Copiez-y vos fichiers, nommés d'après le dossier :

| Fichier             | Média           | Dossier  |
| ------------------- | --------------- | -------- |
| `HACKS-thumb.png`   | Boîte           | `images` |
| `HACKS-image.png`   | Image (capture) | `images` |
| `HACKS-marquee.png` | Logo            | `images` |
| `HACKS-video.mp4`   | Vidéo           | `videos` |

Pour notre exemple, les fichiers sont donc `roms\snes\images\HACKS-thumb.png`, `roms\snes\images\HACKS-image.png`, `roms\snes\images\HACKS-marquee.png` et `roms\snes\videos\HACKS-video.mp4`.

<div align="left"><figure><img src="../.gitbook/assets/image (742).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
* Les images peuvent être en `.png` ou en `.jpg`, les vidéos en `.mp4`.
* Le nom doit être exactement celui du dossier, majuscules comprises.
* Ces fichiers ne sont utilisés que si le dossier n'a pas déjà un média de ce type dans `gamelist.xml` (par exemple un média associé avec la méthode 1).
* Pour plus de détails sur les noms des médias, voir la page Scrape & Métadonnées.
{% endhint %}

### Méthode 3 : modifier le fichier gamelist.xml (avancé)

Le fichier `gamelist.xml` du système (par exemple `roms\snes\gamelist.xml`) fait le lien entre les jeux, les dossiers et leurs médias. Il est créé par RetroBat (scrape, modification des métadonnées) et peut être modifié avec un éditeur de texte (Bloc-notes, Notepad++…).

1. **Fermez RetroBat** : RetroBat enregistre les listes de jeux en quittant, et écraserait vos modifications.
2. Faites une copie de sauvegarde de `gamelist.xml`.
3. Ajoutez un bloc `<folder>` juste avant la dernière ligne, `</gameList>`. Si le fichier contient déjà un bloc `<folder>` avec le même `<path>`, complétez celui-ci au lieu d'en ajouter un second.

Exemple pour le dossier `HACKS` :

```xml
    <folder>
        <path>./HACKS</path>
        <name>HACKS</name>
        <desc>Hacks de jeux Super Nintendo.</desc>
        <image>./images/HACKS-image.png</image>
        <thumbnail>./images/HACKS-thumb.png</thumbnail>
        <marquee>./images/HACKS-marquee.png</marquee>
        <video>./videos/HACKS-video.mp4</video>
    </folder>
```

| Balise                                           | Contenu                                                                                                                   |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| `<path>`                                         | Chemin du sous-dossier depuis le dossier du système, commençant par `./`. Doit correspondre exactement au nom du dossier. |
| `<name>`                                         | Nom affiché dans la liste de jeux.                                                                                        |
| `<desc>`                                         | Description.                                                                                                              |
| `<image>`, `<thumbnail>`, `<marquee>`, `<video>` | Chemins des médias depuis le dossier du système. Avec cette méthode, les fichiers peuvent porter n'importe quel nom.      |

Seules les balises dont vous avez besoin sont nécessaires. Les autres balises des jeux (`<fanart>`, `<boxback>`, `<manual>`…) sont aussi acceptées.

## Bonus : drapeaux dans le nom d'un dossier

RetroBat remplace certains caractères spéciaux par un drapeau. Ces drapeaux sont les images du dossier `emulationstation\resources\flags` de RetroBat.

<div align="left"><figure><img src="../.gitbook/assets/image (741).png" alt=""><figcaption></figcaption></figure></div>

Copiez le caractère de la colonne **Caractère à copier** et collez-le dans le nom du dossier (dans l'Explorateur Windows), ou dans le nom affiché du dossier (méthode 1 ou balise `<name>` de la méthode 3).

| Pays         | Fichier  | Code     | Caractère à copier |
| ------------ | -------- | -------- | ------------------ |
| Australie    | `au.png` | `0xF300` | ``                |
| Brésil       | `br.png` | `0xF301` | ``                |
| Canada       | `ca.png` | `0xF302` | ``                |
| Chine        | `cn.png` | `0xF303` | ``                |
| Allemagne    | `de.png` | `0xF304` | ``                |
| Espagne      | `es.png` | `0xF305` | ``                |
| Europe       | `eu.png` | `0xF306` | ``                |
| France       | `fr.png` | `0xF307` | ``                |
| Grèce        | `gr.png` | `0xF308` | ``                |
| Inde         | `in.png` | `0xF309` | ``                |
| Italie       | `it.png` | `0xF30A` | ``                |
| Japon        | `jp.png` | `0xF30B` | ``                |
| Corée du Sud | `kr.png` | `0xF30C` | ``                |
| Pays-Bas     | `nl.png` | `0xF30D` | ``                |
| Norvège      | `no.png` | `0xF30E` | ``                |
| Portugal     | `pt.png` | `0xF30F` | ``                |
| Russie       | `ru.png` | `0xF310` | ``                |
| Suède        | `sw.png` | `0xF311` | ``                |
| Royaume-Uni  | `uk.png` | `0xF312` | ``                |
| États-Unis   | `us.png` | `0xF313` | ``                |
| Monde        | `wr.png` | `0xF314` | ``                |

{% hint style="info" %}
* Ces caractères ne sont pas visibles sur cette page ni dans Windows (case vide ou carré) : ils ne s'affichent qu'en drapeau dans RetroBat.
* Ils fonctionnent aussi dans le nom affiché d'un jeu.
* Si vous changez le nom d'un dossier, renommez aussi ses fichiers de médias (méthode 2) ou son `<path>` (méthode 3).
{% endhint %}
