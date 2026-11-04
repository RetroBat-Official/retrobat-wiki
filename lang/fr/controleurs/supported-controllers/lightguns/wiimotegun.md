---
description: Utiliser une Wiimote comme pistolet.
---

# WiimoteGun et Wiimote4Guns

Avec une DolphinBar en **mode 4**, la Wiimote n'est pas vue comme une souris par Windows : un logiciel est nécessaire pour la transformer en pistolet. Deux logiciels sont compatibles avec RetroBat :

<table data-header-hidden><thead><tr><th width="137"></th><th width="276.25"></th><th></th></tr></thead><tbody><tr><td></td><td><strong>WiimoteGun</strong></td><td><strong>Wiimote4Guns</strong></td></tr><tr><td>Auteur</td><td>Fabrice Caruso (<a href="https://github.com/fabricecaruso/WiimoteGun">GitHub</a>)</td><td>Aynshe (<a href="https://github.com/Aynshe/WiimoteGun">GitHub</a>), basé sur WiimoteGun</td></tr><tr><td>Installation</td><td>Fourni avec RetroBat</td><td>À installer vous-même</td></tr><tr><td>Wiimotes</td><td>1</td><td><strong>Jusqu'à 4 sur une seule DolphinBar</strong></td></tr><tr><td>Démarrage</td><td>Avec RetroBat (<code>retrobat.ini</code>)</td><td>Son propre démarrage (service)</td></tr><tr><td>En plus</td><td>–</td><td>Mode manette, vibrations, dispositions de capteur à 4 LED…</td></tr></tbody></table>

{% hint style="warning" %}
N'utilisez **qu'un seul** de ces deux logiciels à la fois.
{% endhint %}

Pour les modes 1 et 2 de la DolphinBar (sans logiciel), voir [Wiimote et DolphinBar](wiimotedolphinbar.md).

## Réglage de la DolphinBar

1. Placez la DolphinBar **sous** l'écran, au plus près de l'image, et réglez l'interrupteur à l'arrière sur **BOTTOM** (ou **TOP** si la barre est au-dessus de l'écran).
2. Passez la DolphinBar en **mode 4** : appuyez sur le bouton **MODE** de la barre jusqu'à ce que la LED 4 s'allume, ou maintenez **Home** et appuyez sur **croix Droite** sur la Wiimote.
3. Appairez votre ou vos Wiimotes avec le bouton **SYNC** de la DolphinBar.

## WiimoteGun

### Activer WiimoteGun

WiimoteGun est fourni avec RetroBat mais désactivé par défaut. Pour le lancer avec RetroBat, réglez `WiimoteGun=1` dans le fichier [retrobat.ini](../../../utilisation-avancee/retrobat.ini.md) à la racine de RetroBat.

Ensuite, dans **MENU PRINCIPAL > PARAMÈTRES DES JEUX > PISTOLETS > WIIMOTE**, réglez **MODE DE CONNEXION WIIMOTE** sur **MODE 4 (WIIMOTEGUN)**.

Quand WiimoteGun est lancé, son icône apparaît dans la barre des tâches de Windows. Elle est grise quand aucune Wiimote n'est détectée, et verte quand une Wiimote est détectée :

<div align="left"><figure><img src="../../../.gitbook/assets/image (360).png" alt=""><figcaption></figcaption></figure></div>

### Calibration

Faites un appui long sur le bouton **Home** de la Wiimote pour lancer la calibration, puis suivez les instructions à l'écran.

### Options

Faites un clic droit sur l'icône de WiimoteGun dans la barre des tâches et choisissez **Options** pour indiquer comment votre Wiimote est connectée :

<div align="left"><figure><img src="../../../.gitbook/assets/image (361).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
WiimoteGun n'est actif que lorsque la DolphinBar est en mode 4.
{% endhint %}

## Wiimote4Guns

Wiimote4Guns est une version de WiimoteGun par Aynshe. Son principal avantage : **jusqu'à 4 Wiimotes sur une seule DolphinBar**, pour les jeux au pistolet à plusieurs, avec une barre de capteur classique ou une disposition à 4 LED.

### Installation

1. Désactivez le WiimoteGun fourni avec RetroBat : dans `retrobat.ini`, laissez `WiimoteGun=0` (valeur par défaut).
2. Téléchargez et installez Wiimote4Guns depuis la [page du projet](https://github.com/Aynshe/WiimoteGun/releases). Il nécessite Windows 10 ou 11 et le runtime .NET 10 (x64), et installe son propre pilote virtuel.
3. Passez la DolphinBar en **mode 4** et appairez vos Wiimotes.

{% hint style="info" %}
Wiimote4Guns est en version bêta et évolue vite : reportez-vous à sa page de projet pour les instructions d'installation et les options les plus récentes.
{% endhint %}

### Utilisation dans RetroBat

* Chaque Wiimote est détectée comme un pistolet distinct (**Wiimote4Guns P1** à **P4**) : RetroBat les configure automatiquement, dans l'ordre des joueurs.
* Chaque Wiimote envoie les touches Start et Coin de son propre joueur (`1` / `5` pour le joueur 1, `2` / `6` pour le joueur 2…) : chaque joueur démarre et met des crédits avec sa propre Wiimote.
* Calibration : appui long sur **Home** sur la Wiimote.

Wiimote4Guns propose aussi :

* un **mode manette** (manettes virtuelles pour chaque joueur), utilisé notamment pour les rail shooters dans Dolphin, PCSX2 et DuckStation ;
* les **vibrations** dans les Wiimotes, avec OutputHooker et DemulShooter ;
* un menu à l'écran (overlay) pour changer ses réglages en cours de jeu.

## Jeux Wii (Dolphin)

Pour les jeux Wii, Dolphin utilise directement les Wiimotes comme de **vraies Wiimotes** avec la DolphinBar en mode 4 : voir la page [Wii](../../../systemes-and-emulateurs/supported-game-systems/consoles-de-jeu/nintendo-consoles-de-jeu/wii.md).
