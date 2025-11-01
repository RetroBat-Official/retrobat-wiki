---
description: Nintendo
---

# GameCube

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/gc-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/gc.svg" alt=""></picture><figcaption></figcaption></figure></div>

Console de jeu - Durée de vie : 2001 - 2007

{% embed url="https://fr.wikipedia.org/wiki/GameCube" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>dolphin</li><li>libretro: dolphin</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> gamecube</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.gcz .iso .ciso .wbfs .wad .rvz .wia .m3u .zip .7z .json</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>Dolphin : OUI<br>lr-dolphin : OUI</td><td>Dolphin : NON<br>lr-dolphin : NON</td><td>Dolphin : OUI<br>lr-dolphin : OUI</td></tr></tbody></table>

| Succès Rétro | Parties en Réseau |
| ------------ | ----------------- |
| NON          | NON               |

## BIOS

Les BIOS ne sont pas nécessaires pour lancer des jeux Gamecube, mais certains sont requis pour améliorer le support de certains jeux au niveau graphiques ou encore des polices de caractères pour les textes des jeux.

<table data-header-hidden><thead><tr><th width="169">File</th><th width="625">Location &#x26; MD5</th><th data-hidden>MD5 Hash</th></tr></thead><tbody><tr><td><code>IPL.bin</code><br>Europe</td><td><p>Emplacement: <code>\emulators\dolphin-emu\User\GC\EUR</code></p><p>Emplacement libretro: <code>\saves\dolphin\User\GC\EUR</code><br>md5: <code>0cdda509e2da83c85bfe423dd87346cc</code></p></td><td></td></tr><tr><td><code>IPL.bin</code><br>Japan</td><td><p>Emplacement: <code>\emulators\dolphin-emu\User\GC\JAP</code></p><p>Emplacement libretro: <code>\saves\dolphin\User\GC\JAP</code><br>md5: <code>fc924a7c879b661abc37cec4f018fdf3</code></p></td><td></td></tr><tr><td><code>IPL.bin</code><br>USA</td><td><p>Emplacement: <code>\emulators\dolphin-emu\User\GC\USA</code></p><p>Emplacement libretro: <code>\saves\dolphin\User\GC\USA</code><br>md5: <code>019e39822a9ca3029124f74dd4d55ac4</code></p></td><td></td></tr></tbody></table>

## Dossiers

### Sauvegardes

Par défaut, Dolphin génère des sauvegardes au format "dossier CGI" à l'emplacement suivant:

`saves\gamecube\dolphin-emu\User\GC\<region>`

{% hint style="info" %}
Libretro Dolphin utilise un sous-dossier "Card A"
{% endhint %}

Le sous-dossier de la région peut être modifié avec [le paramétrage](../../../../navigation/configuration-des-systemes-et-des-jeux.md) ci-dessous:

<div align="left"><figure><img src="https://i.imgur.com/A6MVJmv.png" alt=""><figcaption></figcaption></figure></div>

Il est possible également de configurer Dolphin afin d'utiliser des fichiers SRAM (ancienne méthode, un fichier correspond à une carte mémoire de Gamecube) plutôt que des dossiers CGI:

<div align="left"><figure><img src="https://i.imgur.com/GoF2dWZ.png" alt=""><figcaption></figcaption></figure></div>

Dans ce cas, le fichier de sauvegarde sera stocké dans le dossier :

`saves\gamecube\dolphin-emu\User\GC\`

### Sauvegardes d'état

<table><thead><tr><th width="133.20001220703125">Emulateur</th><th>Emplacement</th></tr></thead><tbody><tr><td>Dolphin</td><td>saves\gamecube\dolphin</td></tr><tr><td>Retroarch</td><td>saves\gamecube\libretro.dolphin</td></tr></tbody></table>

## Contrôles

{% hint style="info" %}
Les contrôleurs suivants peuvent être autoconfigurés depuis RetroBat dans Dolphin:

* Contrôleurs XInput
* Dualshock 4 et Dualsense
* Nintendo Switch Pro
* Contrôleur original Gamecube avec un adaptateur Gamecube
{% endhint %}

### Schémas de contrôles

Plusieurs schémas de contrôles sont disponibles dans RetroBat, pour les sélectionner, utiliser l'option ci-dessous dans [**options avancées du système**](../../../../navigation/view-options.md#configuration-avancee-du-systeme) **> contrôles**:

<div align="left"><figure><img src="https://i.imgur.com/npyMOTH.png" alt=""><figcaption></figcaption></figure></div>

| Option                                  | Schéma de contrôle                                                                                                                             |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>DISPOSITION NINTENDO<br>(défaut)</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gamecube.png?raw=true" alt="" data-size="original">          |
| POSITIONNEL                             | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gamecube_position.png?raw=true" alt="" data-size="original"> |
| DISPOSITION XBOX                        | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gamecube_xbox.png?raw=true" alt="" data-size="original">     |
| MIX                                     | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gamecube_xy.png?raw=true" alt="" data-size="original">       |

{% hint style="info" %}
Il est possible d'activer la fonction "RUMBLE" dans les options avancées.
{% endhint %}

### Utilisation d'un adaptateur Gamecube

Dolphin permet l'utilisation d'une manette GameCube originale, pour ce faire il est nécessaire d'installer les pilotes "Zadig":

**1.** Télécharge Zadig ici: [https://zadig.akeo.ie/](https://zadig.akeo.ie/)&#x20;

**2.** Lancer Zadig, aller dans `Options`, choisir`List All Devices`.&#x20;

**3.** Trouver l'adapteur GameCub dans la liste des périphériques (exemple: GC adapter - **WUP-028**, Bluetooth adapter - **CSR-XXXX**).&#x20;

**4.** Sélectionner le bon driver à remplacer. **libusbK** est recommandé.&#x20;

**5.** Utiliser les flèches haut/bas sur la droite pour sélectionner le driver.&#x20;

**6.** Cliquer sur`Replace Driver`. Patienter (cela peut prendre 5 minutes).

&#x20;**7.** Paramétrer RetroBat pour utiliser l'adaptateur Gamecube.

<div align="left"><figure><img src="https://i.imgur.com/hz0VYH2.png" alt=""><figcaption></figcaption></figure></div>

Si l'adaptateur ne fonctionne pas, il est possible qu'il ne soit pas pris en charge par Dolphin.

{% hint style="info" %}
RetroBat détecte actuellement de façon automatique les adaptateurs Raphnet et Mayflash, ceux-ci fonctionneront de façon idéale en suivant les étapes précédentes, mais peuvent également être configurés sans utiliser les pilotes zadig par RetroBat, dans ce cas il faut veiller à ne pas activer l'option "**ADAPTATEUR GAMECUBE**".
{% endhint %}

### Création d'un profil de contrôle spécifique pour un jeu

Il est possible de créer un profil de contrôle spécifique pour un jeu et de l'assigner automatiquement à chaque démarrage, [suivre ce lien pour connaître la procédure.](../../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-dolphin.md)

## Information spécifique au système

### Jeux multi-disques

Utiliser un fichier `.m3u` pour les jeux multi-disques.&#x20;

Le fichier m3u doit contenir une ligne par disque du jeu, par exemple pour le jeu Baten Kaitos:

<div align="left"><figure><img src="https://i.imgur.com/Hh12kWj.png" alt=""><figcaption></figcaption></figure></div>

Dans le fichier m3u, lister les noms exacts des fichiers des disques du jeu et sauvegarder:

<div align="left"><figure><img src="https://i.imgur.com/aBZpJ4W.png" alt=""><figcaption></figcaption></figure></div>

### Textures "custom"

Il est possible d'utiliser des textures "custom" avec l'émulateur Dolphin.

Les packs de textures doivent être placés dans le dossier `\saves\dolphin\User\Load\Textures`.

<div align="left"><figure><img src="https://i.imgur.com/jJm7Htu.png" alt=""><figcaption></figcaption></figure></div>

Le nom du dossier du pack de textures doit être strictement identique au **Game ID** du jeu, le Game ID est disponible depuis Dolphin en affichant les propriétés du jeu.

<div align="left"><figure><img src="https://i.imgur.com/wWaNFxC.png" alt=""><figcaption></figcaption></figure></div>

Une fois le pack de textures correctement nommé et placé dans le bon dossier, activer les  **CUSTOM TEXTURES** dans Retrobat.

<div align="left"><figure><img src="https://i.imgur.com/R5SWtvS.png" alt=""><figcaption><p>Options d'affichage > Configuration avancée du système</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/K5NInuR.png" alt=""><figcaption><p>Visual Rendering</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/UPixWDa.png" alt=""><figcaption><p>Custom Textures</p></figcaption></figure></div>

### Ajouter l'icône trophée manquante sur un jeu compatible retroachievements

Il est possible que pour certaines extensions de fichiers (par exemple .gcz ou .rvz), l'indexation RetroBat ne reconnaît pas un jeu pourtant compatible avec les succès rétro, quand bien même Dolphin fait apparaître au lancement un message vous alertant de la disponibilité de succès pour ce même jeu.&#x20;

<div align="left"><figure><img src="https://i.imgur.com/ThQfwGy.png" alt=""><figcaption></figcaption></figure></div>

Pour faire apparaitre l'indicateur de trophées, il faut éditer le fichier `gamelist.xml` disponible dans le répertoire `roms\<system>` pour y ajouter la ligne suivante :&#x20;

```
<cheevosId>XXXXX</cheevosId>
```

L' ID `XXXXX` ci-dessus doit être remplacé par l'identifiant du jeu, que vous pouvez retrouver à l'adresse [https://retroachievements.org](https://retroachievements.org). L'ID apparaît dans la barre d'adresse du navigateur quand vous consultez la page du jeu.

Dans notre exemple :

<div align="left"><figure><img src="https://i.imgur.com/t1Vyf3Y.png" alt=""><figcaption></figcaption></figure></div>

Ci-dessous l'exemple d'un fichier gamelist.xml file après l'avoir édité et ajouté l'identifiant cheevos correspondant :

<div align="left"><figure><img src="https://i.imgur.com/sh46QjQ.png" alt=""><figcaption></figcaption></figure></div>

Après avoir actualisé la liste de jeux, l'icône trophée apparaît à côté du jeu:

<div align="left"><figure><img src="https://i.imgur.com/81lKuBq.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="danger" %}
Le fichier`gamelist.xml` est un document sensible. Pensez a faire une sauvegarde de votre fichier avant toute modification.
{% endhint %}

