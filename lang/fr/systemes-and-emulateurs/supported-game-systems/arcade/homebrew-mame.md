---
description: MAME Team
---

# HomeBrew MAME

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/hbmame.svg" alt=""><figcaption></figcaption></figure></div>

**HBMAME** (HomeBrew MAME) est un dérivé de MAME 0.245 qui permet de lancer plusieurs hacks et homebrews.

{% embed url="https://arcade.mameworld.info/hbmame/index.html" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>hbmame</li><li>Libretro : mame</li></ul></td></tr><tr><td><strong>Dossier de jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> hbmame</td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr></tbody></table>

## Bios

Se référer à la section [MAME](mame.md#bios-information) du wiki, HBMAME a besoin des mêmes BIOS que MAME pour fonctionner.

## Contrôles

[Se référer à la page MAME ](mame.md#controls)du wiki.

## Informations spécifiques au système

### Ajouter des jeux HBMame à Retrobat

La plupart des jeux pour HBMame sont fournis dans des romsets de type "merged", cela signifie, si vous avez lu notre "[guide arcade](../../arcade-guide.md#roms)", que plusieurs jeux et hacks de jeux sont présents dans un seul fichier .zip.

Or, RetroBat et Mame ne supportent pas les roms de type "merged", il est donc nécessaire d'extraire les différentes versions du zip principal afin de les stocker comme n'importe quel autre jeu, dans un fichier .zip indépendant.

L'exemple ci-dessous est réalisé avec le hack "Arrange v1.1" du jeu DoDonPachi:

<div align="left"><figure><img src="https://i.imgur.com/5Zh2T6D.png" alt=""><figcaption></figcaption></figure></div>

#### Etape 1: vérifier la rom de jeu

Avant toute chose, il faut s'assurer que la rom de jeu soit correcte et dans une version compatible avec l'émulateur.

Pour cela, vous pouvez télécharger la dernière version de HBMame [ici](https://hbmame.1emulation.com/), et vous assurer que la version que vous possédez du jeu et de ses hacks est correcte en auditant les roms.

Si tout apparaît en vert comme dans l'exemple ci-dessus : vous pouvez continuer.

#### Etape 2: extraire la rom du hack

Placer le zip que vous possédez (jeu + hacks) dans le dossier `\roms\hbmame` de votre installation RetroBat.

Ouvrir l'archive et extraire de l'archive le hack que vous souhaitez lancer depuis RetroBat (`ddonpacha` dans notre exemple):

<div align="left"><figure><img src="https://i.imgur.com/uPE1ZDY.png" alt=""><figcaption></figcaption></figure></div>

Une fois extrait, placez-vous dans le dossier `ddonpacha` et créez un fichier zip avec le contenu du dossier (le zip doit avoir le nom officiel du hack, comme illustré dans HBMame):

<div align="left"><figure><img src="https://i.imgur.com/QiLS3QV.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/dmRocxJ.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="danger" %}
Assurez-vous que le zip contienne directement le contenu du hack du jeu, sans dossier intermédiaire.
{% endhint %}

#### Etape 3: lancer le jeu depuis RetroBat

Les 2 roms apparaîssent désormais dans RetroBat: le jeu principal (ddonpach) et le hack (ddonpacha).

<div align="left"><figure><img src="../../../.gitbook/assets/hVLvQ5N.png" alt=""><figcaption></figcaption></figure></div>

Il est possible de lancer le hack du jeu directement depuis RetroBat avec le core Mame ou l'émulateur Mame standalone:

<div align="left"><figure><img src="https://i.imgur.com/ERVSQi8.png" alt=""><figcaption></figcaption></figure></div>

### Version du romset&#x20;

ROM set : 0.245

### Fichiers CHD ou IMG

Se référer au [Guide Arcade](../../arcade-guide.md#fichiers-chd-ou-img).

### **Fichiers Sample**

Se référer au [Guide Arcade](../../arcade-guide.md#samples).
