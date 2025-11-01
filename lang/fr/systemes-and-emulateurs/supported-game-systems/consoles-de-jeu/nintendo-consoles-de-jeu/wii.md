---
description: Nintendo
---

# Wii

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/wii-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/wii.svg" alt=""></picture><figcaption></figcaption></figure></div>

Console de jeu - Durée de vie : 2006 - 2017

{% embed url="https://fr.wikipedia.org/wiki/Wii" %}

## Information

<table data-header-hidden><thead><tr><th width="201"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>dolphin</li><li>libretro: dolphin</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> wii</td></tr><tr><td><strong>Extensions</strong></td><td>.gcz .iso .ciso .wbfs .wad .rvz .wia .zip .7z .json</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>Dolphin : NON<br>lr-dolphin : NON</td><td>Dolphin : NON<br>lr-dolphin : NON</td><td>Dolphin : OUI<br>lr-dolphin : OUI</td></tr></tbody></table>

| Succès Rétro | Parties en Réseau |
| ------------ | ----------------- |
| NON          | NON               |

## BIOS

Aucun BIOS nécessaire.

## Dossiers

### NAND

Les fichiers de la NAND Wii sont sauvegardés à l'emplacement:

`saves\wii\dolphin-emu\User\Wii\`

## Contrôles (Dolphin émulateur)

{% hint style="info" %}
Les contrôleurs suivants peuvent être autoconfigurés depuis RetroBat dans Dolphin:

* Wiimotes avec une DolphinBar
* Contrôleurs XInput
* Dualshock 4 et Dualsense
* Nintendo Switch Pro
* Contrôleur original Gamecube avec un adaptateur Gamecube
{% endhint %}

### WIIMOTE réelle

Pour une expérience de jeu optimale, il est possible de jouer avec des **Wiimotes** authentiques en les connectant à une **Mayflash DolphinBar** (en mode 4) et en activant l'option **REAL WIIMOTES** dans Retrobat (disponible dans les [Options Avancées du système](../../../../navigation/view-options.md#configuration-avancees-du-systeme) ou dans les [Options Avancées du jeu](../../../../navigation/game-options.md#configuration-avancee-du-jeu))

<figure><img src="https://i.imgur.com/0jC9b8z.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://i.imgur.com/FFWtrsV.png" alt=""><figcaption><p>Wiimote type : select REAL</p></figcaption></figure>

### WIIMOTE émulée

Si vous ne possédez pas de Wiimote, Retrobat permet d'émuler une wiimote avec une manette de jeu et offre de multiples configurations afin de s'adapter à chaque configuration de jeu.

Les différentes options sont disponibles dans le menu "CONTROLS" de la configuration avancée du jeu:

<figure><img src="https://i.imgur.com/ZrsVFNx.png" alt=""><figcaption></figcaption></figure>

Le tableau ci-dessous détaille la correspondance de boutons "standard" lorsque l'option WIIMOTE EMULEE est sélectionnée et lorsque l'option EMULATED DEVICES n'est pas modifiée:

| RetroBat                                                                           | Wiimote émulée                    |
| ---------------------------------------------------------------------------------- | --------------------------------- |
| START                                                                              |                                   |
| SELECT / BACK                                                                      | Home (bouton maison)              |
| D-PAD                                                                              | D-PAD                             |
| Stick analogique gauche                                                            | Pointeur infrarouge de la Wiimote |
| Stick analogique droit                                                             | Mouvement "Tilt"                  |
| ![A](<../../../../.gitbook/assets/image (20).png>)                                 | A                                 |
| ![B](<../../../../.gitbook/assets/image (7).png>)                                  | B                                 |
| <img src="../../../../.gitbook/assets/image (35).png" alt="" data-size="original"> | 2                                 |
| <img src="../../../../.gitbook/assets/image (33).png" alt="" data-size="line">     | 1                                 |
| LB (L1)                                                                            | -                                 |
| RB (R1)                                                                            | +                                 |

Ce mapping n'est pas idéal pour certains jeux, c'est pour cette raison que l'option "EMULATED DEVICE" existe, elle permet de contrôler plus précisément la façon dont la correspondance des boutons est paramétrée.

<figure><img src="https://i.imgur.com/XiT8CDQ.png" alt=""><figcaption></figcaption></figure>

La liste des options est assez longue et détaillée ci-dessous.

{% hint style="info" %}
Les mêmes résultats peuvent être atteints en modifiant le nommage des roms de jeux et en gardant l'option "EMULATED DEVICES" sur **AUTO**.
{% endhint %}

<figure><img src="https://i.imgur.com/9r9NzJp.png" alt=""><figcaption><p>Liste des options de configuration des Wiimotes émulées</p></figcaption></figure>

#### CLASSIC CONTROLLER (ou ajout de ".cc." dans le nom de la ROM du jeu)

Mapping à utiliser pour reproduire l'utilisation du Classic Controller, la meilleure option pour les jeux compatibles (par exemple `Super Smash Bros WII`).

Correspondance des boutons pour le mode Classic Controller:

| Retrobat                                                                           | Classic Controller |
| ---------------------------------------------------------------------------------- | ------------------ |
| START                                                                              | +                  |
| SELECT                                                                             | -                  |
| D-PAD                                                                              | D-PAD              |
| Stick analogique gauche                                                            | Stick gauche       |
| Stick analogique droit                                                             | Stick droit        |
| ![A](<../../../../.gitbook/assets/image (20).png>)                                 | B                  |
| ![B](<../../../../.gitbook/assets/image (7).png>)                                  | A                  |
| <img src="../../../../.gitbook/assets/image (35).png" alt="" data-size="original"> | X                  |
| <img src="../../../../.gitbook/assets/image (33).png" alt="" data-size="line">     | Y                  |
| L1                                                                                 | L                  |
| R1                                                                                 | R                  |
| L2                                                                                 | ZL                 |
| R2                                                                                 | ZR                 |

<details>

<summary>Liste des jeux Wii compatibles avec le Classic Controller</summary>

```
Blast Works: Build Trade Destroy
Bleach: Versus Crusade
Call of Duty: Black Ops
Call of Duty: Modern Warfare 3
Castlevania Judgment
Dokapon Kingdom
Dragon Ball Z: Budokai Tenkaichi 2
Dragon Ball Z: Budokai Tenkaichi 3
Fifa 09
Fifa 10
Fifa 15
Final Fantasy Crystal Chronicles: Echoes of Time
Fire Emblem: Radiant Dawn
Geometry Wars Galaxies
G.I. Joe: The Rise of Cobra
Grim Adventures of Billy & Mandy, The
Guilty Gear XX Accent Core
Harvest Moon: Tree of Tranquility
Kirby's Dream Collection
Mario Kart Wii
MLB Power Pros
MLB Power Pros 2008
Mortal Kombat: Armageddon
Monster Hunter Tri
Muramasa: The Demon Blade
MySims Racing
Naruto: Clash of Ninja Revolution 1
Naruto Shippuden: Clash of Ninja Revolution 3
Naruto Shippuuden Gekitou! Ninja Taisen EX
Naruto Shippuuden Gekitou! Ninja Taisen EX2
Naruto Shippuuden Gekitou! Ninja Taisen EX3
Need for Speed: Undercover
Newer Super Mario Bros Wii [HACK]
NHL 2k10
NiGHTS: Journey of Dreams
No More Heroes 2
Opoona
Pro Evolution Soccer 2009
Rampage: Total Destruction
Resident Evil Archives: Resident Evil
Resident Evil 4 Wii Edition
Rune Factory Frontier
Samurai Shodown Anthology
Sengoku Basara: Samurai Heroes
SNK Arcade Classics Vol. 1
Sonic Colors
Sonic Unleashed
SpongeBob's Truth or Square
Super Mario Kart Wii
Super Smash Bros. Brawl
Taiko No Tatsujin
Tatsunoko vs. Capcom: Cross Generation of Heroes
Teenage Mutant Ninja Turtles: Smash-Up
Tetris Party Deluxe
The Last Story
TNA Impact
Ultimate Shooting Collection
WWE SmackDown vs. Raw 2010
Victorious Boxers Revolution
Virtual Console Games
Pro Evolution Soccer 2010
Xenoblade Chronicles
Zhu Zhu Pets: Featuring the Wild Bunch
```

</details>

(Exemple de nom de ROM si la technique du renommage de ROM est utilisée : `Super Smash Bros WII.cc.iso`)

#### WIIMOTE: HORIZONTAL (ou ajout de ".side." dans le nom de la ROM du jeu)

C'est le paramétrage à utiliser pour les jeux demandant de tenir la wiimote à l'horizontal tels que  `New Super Mario Bros Wii`.

La correspondance des touches est identique à la correspondance par défaut, avec les différences suivantes:

| Retrobat                                                                           | Wiimote     |
| ---------------------------------------------------------------------------------- | ----------- |
| ![A](<../../../../.gitbook/assets/image (20).png>)                                 | 1           |
| ![B](<../../../../.gitbook/assets/image (7).png>)                                  | 2           |
| <img src="../../../../.gitbook/assets/image (35).png" alt="" data-size="original"> | B           |
| <img src="../../../../.gitbook/assets/image (33).png" alt="" data-size="line">     | A           |
| L2                                                                                 | Shake       |
| SELECT                                                                             | -           |
| START                                                                              | +           |
| L1                                                                                 | Tilt gauche |
| R1                                                                                 | Tilt droite |

(Exemple de nom de ROM si la technique du renommage de ROM est utilisé : `New Super Mario WII.side.iso`)

#### Autres options (ou ajout de ".<mark style="color:red;">xx</mark>" dans le nom de la ROM du jeu)

Permet de modifier la correspondance des sticks analogiques gauche et droit.

Le stick analogique gauche sera utilisé pour la fonction décrite à gauche du signe `/` et le stick analogique droit pour la fonction décrite à droite du signe `/`.

Les fonctions sont les suivantes:

<table><thead><tr><th width="176.33333333333331">Fonction</th><th width="341">Explication</th><th>Caractère à insérer dans le nom de la ROM</th></tr></thead><tbody><tr><td>Curseur</td><td>Le stick sélectionné reproduit la fonction de pointeur infrarouge de la Wiimote.</td><td>i</td></tr><tr><td>Swing</td><td>Le stick sélectionné reproduit les mouvements de "Swing" de la Wiimote.</td><td>s</td></tr><tr><td>Tilt</td><td>Le stick sélectionné reproduit les mouvements de "Tilt" de la Wiimote.</td><td>t</td></tr><tr><td>Nunchuk</td><td><p>Le stick sélectionné correspond au stick analogique du Nunchuk. </p><p>De plus le mapping des boutons suivants sera modifié:</p><p>L2 = C </p><p>R2 = Z</p></td><td>n</td></tr></tbody></table>

Par exemple, pour un jeu utilisant le Nunchuk et nécessitant l'utilisation du pointeur infrarouge  (par exemple `Super Mario Galaxy`), vous pouvez sélectionner les options suivantes:

<table><thead><tr><th width="210">Option</th><th width="170">Stick gauche</th><th width="194">Stick droit</th><th>Nom de la ROM</th></tr></thead><tbody><tr><td>NUNCHUK/CURSOR</td><td>Stick du nunchuk</td><td>Pointeur IR</td><td>.ni.</td></tr><tr><td>CURSOR/NUNCHUK</td><td>Pointeur IR</td><td>Stick du nunchuk</td><td>.in.</td></tr></tbody></table>

(Exemple de nom de ROM si la technique du nommage de ROM est utilisée : `Super Mario Galaxy.ni.iso` ou `Super Mario Galaxy.in.iso`)

#### Autres extensions

D'autres options sont disponibles pour configurer certaines extensions:

<div align="left"><figure><img src="https://i.imgur.com/zJzeH8F.png" alt=""><figcaption></figcaption></figure></div>

#### Motion Control

Si vous disposez d'une manette compatible avec le motion control (les manettes Switch Pro ou Playstation sont compatibles avec la fonction gyroscope), il est possible de l'utiliser pour simuler les mouvements de la wiimotes.

Pour cela, activer l'option "MOTION CONTROL" dans les options avancées du système:

<div align="left"><figure><img src="https://i.imgur.com/ZZBhOLk.png" alt=""><figcaption></figcaption></figure></div>

### Adaptateur Gamecube

L'utilisation d'un adaptateur est possible pour la console Wii, pour cela il faut suivre la [même procédure que pour la Gamecube (ici)](gamecube.md#utilisation-dun-adaptateur-gamecube), l'option pour activer l'adaptateur depuis RetroBat se trouve ici:

<div align="left"><figure><img src="https://i.imgur.com/QlxyNja.png" alt=""><figcaption></figcaption></figure></div>

### Lightgun (pistolet)

Il est possible de jouer au pistolet en activant l'option suivante :

<div align="left"><figure><img src="https://i.imgur.com/llDVUl7.png" alt=""><figcaption></figcaption></figure></div>

Les contrôles au gun sont les suivants:

<table><thead><tr><th width="176.33333333333331">Bouton Wiimote</th><th width="220">Bouton gun</th><th>Bouton clavier</th></tr></thead><tbody><tr><td>B</td><td>Gâchette</td><td>Souris gauche</td></tr><tr><td>A</td><td></td><td>Souris droite</td></tr><tr><td>-</td><td></td><td>Retour arrière</td></tr><tr><td>+</td><td></td><td>ENTREE</td></tr><tr><td>D-PAD</td><td></td><td>FLECHES</td></tr><tr><td>1</td><td></td><td>Souris milieu</td></tr><tr><td>2</td><td></td><td>2</td></tr><tr><td>Shake</td><td></td><td>Souris milieu</td></tr><tr><td>Nunchuk C</td><td></td><td>CTRL gauche</td></tr><tr><td>Nunchuk Z</td><td></td><td>MAJ gauche</td></tr><tr><td>Nunchuk stick</td><td></td><td>WASD</td></tr><tr><td>Nunchuk Shake</td><td></td><td>Souris milieu</td></tr></tbody></table>

## Contrôles (Core Libretro)

Le core libretro Dolphin permet de sélectionner parmi les types de contrôleurs suivants:

* WIIMOTE
* WIIMOTE SIDEWAYS
* WIIMOTE + NUNCHUK
* CLASSIC CONTROLLER
* CLASSIC CONTROLLER PRO
* REAL WIIMOTE
* GAMECUBE CONTROLLER ([Voir le mapping Gamecube](gamecube.md#controles))

<table><thead><tr><th width="192">Retrobat</th><th width="102">WIIMOTE</th><th width="98">SIDE</th><th width="130">NUNCHUK</th><th>CLASSIC CONTROLLER</th></tr></thead><tbody><tr><td>START</td><td>+</td><td>+</td><td>1</td><td>+</td></tr><tr><td>SELECT</td><td>-</td><td>-</td><td>2</td><td>-</td></tr><tr><td>D-PAD</td><td>D-PAD</td><td>D-PAD</td><td>D-PAD</td><td>D-PAD</td></tr><tr><td>Stick analogique gauche</td><td>Tilt</td><td>Tilt</td><td>Nunchuk<br>Stick</td><td>Stick gauche</td></tr><tr><td>Stick analogique droite</td><td></td><td></td><td>Tilt</td><td>Stick droit</td></tr><tr><td><img src="../../../../.gitbook/assets/image (20).png" alt="A"></td><td>B</td><td>1</td><td>B</td><td>B</td></tr><tr><td><img src="../../../../.gitbook/assets/image (7).png" alt="B"></td><td>A</td><td>2</td><td>A</td><td>A</td></tr><tr><td><img src="../../../../.gitbook/assets/image (35).png" alt="" data-size="original"></td><td>1</td><td>A</td><td>C</td><td>X</td></tr><tr><td><img src="../../../../.gitbook/assets/image (33).png" alt="" data-size="line"></td><td>2</td><td>B</td><td>Z</td><td>Y</td></tr><tr><td>L1</td><td></td><td></td><td>-</td><td>ZL<br>PRO: L</td></tr><tr><td>R1</td><td></td><td></td><td>+</td><td>ZR<br>PRO: R</td></tr><tr><td>L2</td><td></td><td></td><td>Secouer<br>Nunchuk</td><td>L<br>PRO: ZL</td></tr><tr><td>R2</td><td>Secouer</td><td>Secouer</td><td>Secouer<br>Wiimote</td><td>R<br>PRO: ZR</td></tr><tr><td>L3</td><td></td><td></td><td></td><td></td></tr><tr><td>R3</td><td>Home</td><td>Home</td><td>Home</td><td>Home</td></tr></tbody></table>

## Information spécifique au système

### Charger le menu Wii

Si le menu Wii est installé dans Dolphin, il est possible de le lancer directement avec l'option suivante:

<div align="left"><figure><img src="https://i.imgur.com/G4tfNHl.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/aGImoS5.png" alt=""><figcaption></figcaption></figure></div>

Pour vérifier si le menu Wii est bien installé dans Dolphin, tenter de le lancer directement depuis l'émulateur:

<div align="left"><figure><img src="https://i.imgur.com/g1UJjln.png" alt=""><figcaption></figcaption></figure></div>

### Textures personalisées

La procédure est similaire à la [procédure décrite pour les jeux Gamecube](gamecube.md#textures-custom).
