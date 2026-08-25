---
description: Sony
---

# Playstation 3

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/ps3-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/ps3.svg" alt=""></picture><figcaption></figcaption></figure></div>

Console de jeu - Durée de vie : 2006 - 2017

{% embed url="https://fr.wikipedia.org/wiki/PlayStation_3" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>rpcs3</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> ps3</td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .lnk .ps3 .iso .7z .zip .rar .squashfs .decomp</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="201">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>OUI</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="187">Fichier BIOS</th><th width="109">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>PS3UPDAT.PUP</td><td><code>\bios</code></td><td>3694eb3fb8d9915c112e6ab41a60c69f</td></tr></tbody></table>

#### Installation automatique du firmware

Au premier lancement d'un jeu PS3 avec l'émulateur rpcs3 depuis Retrobat, si le fichier PS3UPDAT.PUP présent dans le dossier \bios de Retrobat, l'émulateur vous proposera automatiquement d'installer le firmware. Une fois l'installation terminée, vous pouvez quitter Rpcs3 et relancer le jeu depuis Retrobat.

<div align="left"><figure><img src="https://i.imgur.com/1ovzizA.png" alt=""><figcaption></figcaption></figure></div>

#### Installation manuelle du firmware

Lancer l'éxecutable rpcs3.exe dans le dossier `\emulators\rpcs3` et sélectionner **install firmware**

<div align="left"><figure><img src="https://i.imgur.com/18HE0DC.png" alt=""><figcaption></figcaption></figure></div>

Choisir le fichier **PS3UPDAT.PUP** pour démarrer l'installation du firmware.

La version installée du Firmware apparait dans le log en bas de l'écran de l'émulateur:

<div align="left"><figure><img src="https://i.imgur.com/JFjxamH.png" alt=""><figcaption></figcaption></figure></div>

## Contrôles

{% hint style="info" %}
Les contrôleurs suivants peuvent être autoconfigurés depuis RetroBat dans rpcs3:

* Contrôleurs XInput
* Dualshocks & DualSense
* Nintendo Switch Pro
{% endhint %}

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/psx.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Boutons sensitifs

La manette originale de la PS3 possède des "boutons sensitifs", RPCS3 permet d'utiliser cette fonction utile pour des jeux tel que Gran Turismo.

Pour cela, il est nécéssaire de posséder un contrôleur Dualshock 3 ou Sisaxis et d'installer le pilote DsHidMini comme décrit ici:

{% embed url="https://wiki.rpcs3.net/index.php?title=Help:Controller_Configuration#Using_Nefarius'_DsHidMini" %}

## Information spécifique au système

### Emplacement des fichiers

<table><thead><tr><th width="254">Data</th><th>Chemin (relatif au dossier RetroBat)</th></tr></thead><tbody><tr><td>dev_hdd0</td><td>saves\ps3\rpcs3\dev_hdd0</td></tr><tr><td>config file</td><td>emulators\rpcs3\config.yml</td></tr><tr><td>gui config file</td><td>emulators\rpcs3\GuiConfigs\CurrentSettings.ini</td></tr><tr><td>Controller configuration file</td><td>emulators\rpcs3\config\input_configs\global\Default.yml</td></tr></tbody></table>

{% hint style="info" %}
Il est possible d'utiliser le dossier `emulators\rpcs3\dev_hdd0` au lieu de saves.

Pour cela il suffit de supprimer le dossier `saves\ps3\rpcs3`.
{% endhint %}

### Ajouter les jeux

Il existe 2 formats de jeux pour la PS3: les disques Blu-Ray et les jeux PSN (PlayStation Network):

* Les jeux ayant une ID commençant par la lettre 'B' sont des jeux Blu-Ray.
* Les jeux ayant une ID commençant par la lettre 'N' sont des jeux dématérialisés (PS Store)

<div align="left"><figure><img src="https://i.imgur.com/EsmEoB4.png" alt=""><figcaption></figcaption></figure></div>

Les jeux au format Blu-ray disc peuvent être placés directement dans le dossier  `\roms\ps3`, les jeux dématérialisés doivent être placés dans le dossier `\saves\ps3\rpcs3\dev_hdd0\game` de votre installation RetroBat.

{% hint style="danger" %}
Les jeux PSN doivent être décryptés pour pouvoir être lus par RPCS3.
{% endhint %}

#### Ajouter un jeu Blu-ray

Copier simplement le dossier du jeu dans le dossier `\roms\ps3` de votre installation RetroBat et renommer le dossier avec une extension .ps3:

<div align="left"><figure><img src="https://i.imgur.com/E98BUs9.png" alt=""><figcaption></figcaption></figure></div>

Le jeu sera directement disponible dans RetroBat.

#### Ajouter un jeu PSN - option 1

Une fois que l'émulateur est configuré, que le jeu est ajouté et qu'il fonctionne correctement lorsqu'il est lancé depuis l'émulateur, créer un fichier m3u et le placer dans le dossier `\roms\ps3` .

Le fichier m3u doit pointer vers le fichier **EBOOT.BIN** se trouvant dans le dossier du jeu dans le répertoire `\saves\ps3\rpcs3\dev_hdd0\game`, ci-dessous un exemple pour le jeu BulletStorm:

<div align="left"><figure><img src="https://i.imgur.com/qV3GMuC.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/LmL6NUh.png" alt=""><figcaption></figcaption></figure></div>

**NOTE**: il est possible de pointer vers d'autres dossiers en utilisant des alias au début de la ligne de contenu du fichier .m3u:

* EMULATORPATH : pointe vers le dossier de l'émulateur
* SAVESPATH : pointe vers le dossier saves\ps3\rpcs3
* ROMPATH :pointe vers le dossier roms\ps3

Par exemple, le fichier ci-dessous pointe vers: `emulators\rpcs3\dev_hdd0\game\Rayman Origins[BLES01386].ps3\PS3_GAME\USRDIR\EBOOT.BIN`

<div align="left"><figure><img src="../../../../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure></div>

#### Ajouter un jeu PSN - option 2

Créer un fichier m3u et le placer dans le dossier `\roms\ps3` .

Le fichier doit contenir l'ID du jeu précédé de GAMEID:

<div align="left"><figure><img src="https://i.imgur.com/DanYmrt.png" alt=""><figcaption></figcaption></figure></div>

L'ID du jeu peut être récupérée dans l'émulateur:

<div align="left"><figure><img src="https://i.imgur.com/2dAJlIN.png" alt=""><figcaption></figcaption></figure></div>

### Utiliser les configurations par jeu de l'émulateur

Par défaut, RetroBat lancera les jeux avec les options définis depuis le menu avancée, ignorant ainsi tout paramétrage par jeu, spécifiquement réalisé depuis l'émulateur RPCS3.

Si vous souhaitez que RetroBat utilise les paramètres par jeu crées depuis RPCS3, il faudra alors activer l'option "**USE CUSTOM CONFIG**" depuis la section émulation des paramètres avancés.

<figure><img src="https://i.imgur.com/JA0W5c2.png" alt=""><figcaption></figcaption></figure>
