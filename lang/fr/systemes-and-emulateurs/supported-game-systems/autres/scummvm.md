---
description: ScummVM Team
---

# ScummVM

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/scummvm.svg" alt=""><figcaption></figcaption></figure></div>

Émulateur - Année de création : 2001

{% embed url="https://fr.wikipedia.org/wiki/ScummVM" %}

## Informations

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>Libretro : scummvm</li><li>scummvm</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> scummvm</td></tr><tr><td><strong>Extensions</strong></td><td>.scummvm .7z .zip .rar .squashfs</td></tr></tbody></table>

## Fonctionnalités

| Retroachievements | NetPlay |
| ----------------- | ------- |
| NON               | NON     |

## BIOS

<table><thead><tr><th width="221">Fichier BIOS</th><th width="177">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>MT32_CONTROL.ROM</td><td><code>\bios\scummvm\extra</code></td><td>5626206284b22c2734f3e9efefcd2675</td></tr><tr><td>MT32_PCM.ROM</td><td><code>\bios\scummvm\extra</code></td><td>89e42e386e82e0cacb4a2704a03706ca</td></tr></tbody></table>

## Contrôles

Il s'agit principalement de jeux prévus pour être joués au clavier et à la souris (point'n'click).&#x20;

Il est possible d'utiliser une configuration [pad2key ](../../../controleurs/pad2key.md)pour utiliser une manette.

## Information spécifique au système

### Ajouter un jeu

Les jeux ScummVM doivent être placés dans le dossier `\roms\scummvm` , chaque jeu dans son propre répertoire:

<div align="left"><figure><img src="https://i.imgur.com/qfDZ5Np.png" alt=""><figcaption></figcaption></figure></div>

Au sein de chaque dossier de jeu, créer un fichier .txt avec le nom du jeu, par exemple **Full Throttle.txt** pour le jeu "Full Throttle".

<div align="left"><figure><img src="https://i.imgur.com/k4GhSoC.png" alt=""><figcaption></figcaption></figure></div>

A l'intérieur du fichier .txt, renseigner le **shortname (nom court)** du jeu, se référer au site [https://www.scummvm.org/compatibility/](https://www.scummvm.org/compatibility/) pour retrouver le shortname du jeu.

{% hint style="info" %}
SLe shortname est composé du moteur de jeu (ici _scumm_), suivi du nom court du jeu (ici _ft_), séparés par un double point.
{% endhint %}

Enfin, renommer le fichier \*._txt_ en \*._scummvm_ (remplacer l'extension .txt par .scummvm) :\
\
Full Throttle.**txt**  **==>** Full Throttle.**scummvm**



### Lancer une version spécifique d'un jeu et gérer les options par jeu

SCUMMVM permet de gérer différentes versions d'un jeu, cela est particluièrement pour les jeux édités sur plusieurs machine (FM-Towns, DOS, Amiga...).

Si vous possédez plusieurs versions d'un même titre et souhaitez pouvoir sélectionner la version à laquelle jouer, il est nécessaire de procéder comme suit.

**Etape 1**: paramétrage du jeu dans SCUMMVM

* Ouvrir SCUMMVM et sélectionner "ajouter...":

<div align="left"><figure><img src="https://i.imgur.com/sk5E5Z7.png" alt=""><figcaption></figcaption></figure></div>

Sélectionner le dossier du jeu.

* Choisir la version du jeu à ajouter:

<div align="left"><figure><img src="https://i.imgur.com/e5o9Nvd.png" alt=""><figcaption></figcaption></figure></div>

* Définir l'ID du jeu et sélectionner les options à activer pour le jeu

<div align="left"><figure><img src="../../../.gitbook/assets/mZLGaKv.png" alt=""><figcaption></figcaption></figure></div>

Cliquer sur OK.

Le jeu est ajouté à SCUMMVM:

<div align="left"><figure><img src="https://i.imgur.com/BuNOCP6.png" alt=""><figcaption></figcaption></figure></div>

**Etape 2**: créer le fichier .scummvm

* Créer un fichier .scummvm spécifique à cette version du jeu dans le dossier `roms\scummvm`:

<div align="left"><figure><img src="https://i.imgur.com/nCNTake.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/5DiPExS.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
TLe contenu du fichier .scummvm doit correspondre exactement à l'ID utilisé lors de l'ajout du jeu dans l'émulateur à l'étape précédente.
{% endhint %}

**Etape 3**: résultat dans RetroBat

Dans RetroBat, plusieurs versions du jeu seront disponibles:

<div align="left"><figure><img src="../../../.gitbook/assets/OTcJf0h.png" alt=""><figcaption><p>2 versions de Indiana Jones</p></figcaption></figure></div>

NB: les short ID de chaque jeu installé dans scummvm peuvent être consultées dans le fichier scummvm.ini, ce fichier est situé dans les dossiers:

* \emulators\scummvm (SCUMMVM standalone)
* \bios (libretro:scummvm)

<div align="left"><figure><img src="https://i.imgur.com/YUsciw5.png" alt=""><figcaption></figcaption></figure></div>
