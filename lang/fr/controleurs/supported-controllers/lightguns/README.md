---
description: Bang bang
---

# 🔫 Pistolets

RetroBat détecte les pistolets et les configure automatiquement dans les émulateurs compatibles. Cette page explique comment brancher et régler votre pistolet.

Pour savoir quels systèmes et émulateurs gèrent les pistolets, et comment les boutons sont mappés, voir la page [Contrôle des pistolets](../../pistolets_controles.md).

## Pistolets pris en charge

<table><thead><tr><th width="215.5">Pistolet</th><th width="139">Détection</th><th width="172.25">Plusieurs joueurs</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>Sinden</strong></td><td>Automatique</td><td>Oui</td><td>Nécessite le logiciel Sinden et une bordure blanche autour de l'écran (les deux sont gérés par RetroBat, voir plus bas).</td></tr><tr><td><strong>Gun4IR</strong></td><td>Automatique</td><td>Oui</td><td></td></tr><tr><td><strong>Blamcon</strong></td><td>Automatique</td><td>Oui</td><td></td></tr><tr><td><strong>RetroShooter</strong></td><td>Automatique</td><td>Oui</td><td></td></tr><tr><td><strong>AimTrak</strong> (Ultimarc)</td><td>Automatique</td><td>Oui</td><td></td></tr><tr><td><strong>AE Lightgun</strong></td><td>Automatique</td><td>Oui</td><td></td></tr><tr><td><strong>Xgunner</strong></td><td>Automatique</td><td>Oui</td><td></td></tr><tr><td><strong>OpenFIRE</strong> (et OpenFIRE-ESP32)</td><td>Automatique</td><td>Oui, jusqu'à 4</td><td>Donnez à chaque pistolet son propre identifiant USB (PID 1 à 4) dans l'application OpenFIRE : il définit le numéro du joueur. Ne modifiez pas le Vendor ID par défaut.</td></tr><tr><td><strong>Wiimote + DolphinBar</strong> (mode 1 ou 2)</td><td>Automatique</td><td>Oui, une DolphinBar par Wiimote</td><td>Voir <a href="wiimotedolphinbar.md">Wiimote et DolphinBar</a>.</td></tr><tr><td><strong>Wiimote + WiimoteGun</strong> (DolphinBar mode 4)</td><td>Quand WiimoteGun est lancé</td><td>Non (1 Wiimote)</td><td>Voir <a href="wiimotegun.md">WiimoteGun</a>.</td></tr><tr><td><strong>Wiimote + Wiimote4Guns</strong></td><td>Automatique</td><td>Oui, jusqu'à 4</td><td>Voir plus bas.</td></tr><tr><td><strong>Souris</strong></td><td>Toujours</td><td>–</td><td>Une souris peut servir de pistolet quand aucun pistolet n'est branché.</td></tr></tbody></table>

{% hint style="info" %}
La plupart des pistolets fonctionnent comme une **souris et un clavier**. Si votre pistolet a plusieurs modes, laissez-le en mode souris (voir son logiciel ou sa notice).
{% endhint %}

## Détection des pistolets

Quand un pistolet est branché, EmulationStation affiche une notification et une icône de pistolet ![](<../../../.gitbook/assets/image (346).png>) en haut à gauche, à côté des icônes des manettes :

<div align="left"><figure><img src="../../../.gitbook/assets/image (347).png" alt=""><figcaption></figcaption></figure></div>

Une mire s'affiche aussi à l'écran, ce qui permet de naviguer dans les menus avec le pistolet.

Ces éléments se règlent dans **MENU PRINCIPAL > PARAMÈTRES DES MANETTES** :

* **MONTRER LES NOTIFICATIONS DU PISTOLET** : notifications de branchement et de débranchement.
* **TRACER LA MIRE DU PISTOLET** : mire dans EmulationStation.

<div align="left"><figure><img src="../../../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure></div>

## Jeux au pistolet

RetroBat sait quels jeux se jouent au pistolet :

* Une icône de pistolet s'affiche à côté de leur nom dans la liste des jeux (**MENU PRINCIPAL > PARAMÈTRES D'AFFICHAGE > ICÔNES > AFFICHER L'ICÔNE PISTOLET**).

<div align="left"><figure><img src="../../../.gitbook/assets/image (349).png" alt=""><figcaption></figcaption></figure></div>

* Le filtre **PISTOLET OPTIQUE** n'affiche que ces jeux dans une liste.
* La collection **jeux au pistolet** les regroupe tous. Activez-la dans **MENU PRINCIPAL > PARAMÈTRES DES COLLECTIONS > COLLECTIONS AUTOMATIQUES**.

La liste des jeux au pistolet est le fichier `emulationstation\resources\gamesdb.xml`. Un jeu est reconnu quand son nom de fichier correspond à (ou contient) l'`id` d'un jeu marqué `<gun/>` pour son système.

{% hint style="info" %}
Pour personnaliser la liste, copiez le fichier dans `emulationstation\.emulationstation\resources\gamesdb.xml` et modifiez la copie : elle est lue en priorité et n'est pas écrasée par les mises à jour de RetroBat. Votre copie ne recevra pas les jeux ajoutés par les mises à jour suivantes.
{% endhint %}

{% hint style="info" %}
Certains jeux sont dans la liste alors que le pistolet ne sert que dans certains niveaux ou mini-jeux.
{% endhint %}

## Activer les pistolets

Pour les jeux de la liste, **les pistolets sont activés automatiquement** au lancement du jeu (sauf sur Wii, où les Wiimotes sont utilisées comme de vraies Wiimotes).

Pour les autres jeux, ou pour changer ce comportement, utilisez l'option **ACTIVER LES PISTOLETS** :

* Pour un système : ouvrez les [Options d'affichage](../../../navigation/view-options.md) du système, choisissez **CONFIGURATION AVANCÉE DU SYSTÈME**, puis **PISTOLETS**.
* Pour un jeu : ouvrez les [Options du jeu](../../../navigation/game-options.md), choisissez **CONFIGURATION AVANCÉE DU JEU**, puis **PISTOLETS**.

<div align="left"><figure><img src="../../../.gitbook/assets/image (350).png" alt=""><figcaption></figcaption></figure></div>

Réglez **ACTIVER LES PISTOLETS** sur **OFF** pour jouer à un jeu au pistolet avec une manette.

{% hint style="info" %}
Désactiver l'autoconfiguration des manettes ne désactive pas la configuration des pistolets : réglez aussi **ACTIVER LES PISTOLETS** sur **OFF**.
{% endhint %}

Autres options courantes du sous-menu **PISTOLETS** (selon l'émulateur) :

<table><thead><tr><th width="246.5">Option</th><th>Description</th></tr></thead><tbody><tr><td><strong>UN SEUL PISTOLET</strong></td><td>Ne configure qu'un seul pistolet quand plusieurs sont branchés.</td></tr><tr><td><strong>BOUTON POUR RECHARGER</strong></td><td>Recharge avec un bouton au lieu de tirer hors de l'écran, pour les pistolets qui ne savent pas tirer hors écran.</td></tr><tr><td><strong>INVERSER GÂCHETTE ET RECHARGE</strong></td><td>Inverse la gâchette et le bouton de recharge (par exemple avec un Wii Zapper).</td></tr></tbody></table>

## Plusieurs pistolets et ordre des joueurs

RetroBat attribue les pistolets aux joueurs dans cet ordre :

1. Les pistolets dédiés, selon leur propre numéro de joueur quand le pistolet en a un (Gun4IR, Blamcon, Sinden, RetroShooter, OpenFIRE...).
2. Les Wiimotes (Wiimote4Guns J1 à J4, puis DolphinBar).
3. Les autres souris.

Si l'ordre n'est pas le bon, vous pouvez le forcer avec **INDEX SOURIS/GUN JOUEUR 1** à **4** :

* RetroArch : **MENU PRINCIPAL > PARAMÈTRES DES JEUX > OPTIONS RETROARCH > PISTOLETS**.
* Autres émulateurs : configuration avancée du système > **PISTOLETS**, quand l'émulateur le propose.

{% hint style="info" %}
Les pistolets détectés, dans leur ordre, sont listés dans `emulationstation\emulatorLauncher.log` (lignes commençant par `[RawLightGun]`).
{% endhint %}

## Pistolet Sinden

<div align="left"><figure><img src="../../../.gitbook/assets/image (351).png" alt="" width="188"><figcaption></figcaption></figure></div>

Le pistolet Sinden nécessite le logiciel Sinden (`Lightgun.exe`), disponible sur le [site Sinden](https://sindenlightgun.com/drivers/).

### Premier réglage (hors RetroBat)

Avant d'utiliser les pistolets dans RetroBat, lancez une première fois le logiciel Sinden seul :

1. Configurez et calibrez votre ou vos pistolets dans le logiciel (un onglet par pistolet).
2. Activez **Start automatically**, pour que le pistolet démarre dès que le logiciel est lancé par RetroBat :

<div align="left"><figure><img src="../../../.gitbook/assets/image (352).png" alt=""><figcaption></figcaption></figure></div>

3. Fermez le logiciel : vos réglages sont enregistrés dans le fichier `Lightgun.exe.Config`, à côté de `Lightgun.exe`.

### Logiciel Sinden dans RetroBat

RetroBat le lance automatiquement quand un pistolet Sinden est détecté. Au choix :

* placez le logiciel dans le dossier `system\tools\sinden` de RetroBat,

<div align="left"><figure><img src="../../../.gitbook/assets/image (353).png" alt=""><figcaption></figcaption></figure></div>

* ou indiquez son emplacement dans **MENU PRINCIPAL > PARAMÈTRES DES JEUX > PISTOLETS > SINDEN > CHEMIN DU LOGICIEL SINDEN**.

<div align="left"><figure><img src="../../../.gitbook/assets/image (354).png" alt=""><figcaption></figcaption></figure></div>

Autres options dans **PARAMÈTRES DES JEUX > PISTOLETS > SINDEN** :

<table><thead><tr><th width="214">Option</th><th>Description</th></tr></thead><tbody><tr><td><strong>CONFIGURATION BOUTONS SINDEN</strong></td><td><strong>STANDARD</strong> (par défaut) : RetroBat règle les boutons du pistolet en boutons de souris et touches, comme l'attendent les émulateurs. <strong>MODE MANETTE</strong> : les boutons sont envoyés comme des boutons de manette. <strong>NE PAS MODIFIER</strong> : RetroBat conserve votre propre configuration Sinden.</td></tr><tr><td><strong>STOPPER LE LOGICIEL SINDEN</strong></td><td>Ferme le logiciel Sinden à la fin du jeu.</td></tr></tbody></table>

**Bordure blanche** : le Sinden a besoin d'une bordure blanche autour du jeu pour repérer l'écran. RetroBat l'ajoute automatiquement (sous forme de bezel) quand les pistolets sont activés.

Pour certains émulateurs standalone, la bordure est dessinée avec ReShade : choisissez le jeu de shaders **sindenborder** si la bordure n'apparaît pas.

<div align="left"><figure><img src="../../../.gitbook/assets/image (355).png" alt=""><figcaption></figcaption></figure></div>

### WiiMote

<div align="left"><figure><img src="../../../.gitbook/assets/image (356).png" alt=""><figcaption></figcaption></figure></div>

Une Wiimote peut servir de pistolet de trois façons :

<table><thead><tr><th width="146.5">Méthode</th><th width="183">Mode DolphinBar</th><th width="182.75">Joueurs</th><th>Logiciel</th></tr></thead><tbody><tr><td><strong>DolphinBar seule</strong></td><td>Mode 1 ou mode 2</td><td>Une DolphinBar par Wiimote</td><td>Aucun. Voir <a href="wiimotedolphinbar.md">Wiimote et DolphinBar</a>.</td></tr><tr><td><strong>WiimoteGun</strong></td><td>Mode 4</td><td>1</td><td>Fourni avec RetroBat. Voir <a href="wiimotegun.md">WiimoteGun</a>.</td></tr><tr><td><strong>Wiimote4Guns</strong></td><td>Mode 4, ou Bluetooth sans DolphinBar</td><td>Jusqu'à 4</td><td>À installer : <a href="https://github.com/Aynshe/WiimoteGun">Wiimote4Guns (Aynshe)</a>.</td></tr></tbody></table>

Indiquez à RetroBat le mode utilisé dans **MENU PRINCIPAL > PARAMÈTRES DES JEUX > PISTOLETS > WIIMOTE > MODE DE CONNEXION WIIMOTE**. Avec 2 Wiimotes, **WIIMOTE ASSOCIATION ALTERNATIVE** peut corriger une mauvaise association entre les Wiimotes et leur clavier dans certains émulateurs.

<div align="left"><figure><img src="../../../.gitbook/assets/image (357).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Pour les jeux Wii dans Dolphin, les Wiimotes sont utilisées comme de **vraies Wiimotes** (DolphinBar en mode 4) : voir la page [Wii](../../../systemes-and-emulateurs/supported-game-systems/consoles-de-jeu/nintendo-consoles-de-jeu/wii.md).
{% endhint %}

### Wiimote4Guns

Wiimote4Guns est une version de WiimoteGun par Aynshe qui gère **jusqu'à 4 Wiimotes**, avec une barre de capteur classique ou une disposition à 4 LED. Chaque Wiimote est vue par RetroBat comme un pistolet distinct (Wiimote4Guns P1 à P4) et configurée automatiquement pour les jeux multijoueurs.

1. Installez Wiimote4Guns comme indiqué sur la [page du projet](https://github.com/Aynshe/WiimoteGun) (Windows 10 ou 11, runtime .NET 10 x64 ; Wiimote4Guns installe son propre pilote virtuel).
2. Désactivez le WiimoteGun fourni avec RetroBat : dans le fichier `retrobat.ini` à la racine de RetroBat, réglez `WiimoteGun=0` (valeur par défaut).
3. Réglez la DolphinBar en **mode 4**.

{% hint style="info" %}
Pour plus de précision, placez la DolphinBar (ou la barre de capteur) **sous** l'écran, au plus près de l'image, et mettez l'interrupteur à l'arrière de la DolphinBar en position **basse**.
{% endhint %}

{% hint style="warning" %}
WiimoteGun et Wiimote4Guns ne doivent pas tourner en même temps.
{% endhint %}

## Autres pistolets

* [Gun4IR](https://www.gun4ir.com/)
* [RetroShooter](https://retroshooter.com/)
* [Blamcon](https://blamcon.com/)
* [AimTrak (Ultimarc)](https://www.ultimarc.com/)
* [OpenFIRE](https://openfirelightgun.org/) ([firmware](https://github.com/TeamOpenFIRE/OpenFIRE-Firmware))
* [OpenFIRE-ESP32](https://alessandro-satanassi.github.io/OpenFIRE-ESP32/) ([firmware](https://github.com/alessandro-satanassi/OpenFIRE-Firmware-ESP32))

Ces pistolets sont détectés automatiquement grâce à leur identifiant USB. S'ils ont plusieurs modes, réglez-les en mode souris (et clavier) avec leur propre logiciel.
