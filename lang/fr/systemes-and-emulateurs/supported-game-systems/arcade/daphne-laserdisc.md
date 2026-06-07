# LaserDisc

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/daphne.svg" alt=""><figcaption></figcaption></figure></div>

Arcade - Date de sortie du premier jeu LaserDisc : 1983

{% embed url="https://fr.wikipedia.org/wiki/DAPHNE" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>hypseus</li><li>daphne</li><li>singe2</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> daphne</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.daphne .hypseus .7z .rar .squashfs</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès rétro</th><th width="200">Netplay</th><th>Autoconfiguration contrôleurs</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>hypseus: OUI<br>daphne: NON<br>singe2: OUI</td></tr></tbody></table>

## BIOS

Aucun BIOS nécessaire pour les jeux DAPHNE ou SINGE.

## Contrôles

### Manettes de jeux&#x20;

<table><thead><tr><th width="311">Action</th><th>Bouton Manette</th></tr></thead><tbody><tr><td>Mouvement directionnel</td><td>D-PAD ou Stick analogique gauche</td></tr><tr><td>COIN 1</td><td>SELECT</td></tr><tr><td>START 1</td><td>START</td></tr><tr><td>Bouton 1</td><td>A (SUD)</td></tr><tr><td>Bouton 2</td><td>B (EST)</td></tr><tr><td>Bouton 3</td><td>R1 (EPAULE DROITE)</td></tr><tr><td>Skill 1</td><td>Y (OUEST)</td></tr><tr><td>Skill 2</td><td>X (NORD)</td></tr><tr><td>Skill 3</td><td>L1 (EPAULE GAUCHE)</td></tr><tr><td>SERVICE</td><td>L3 (STICK GAUCHE)</td></tr><tr><td>TEST</td><td>R3 (STICK DROIT)</td></tr></tbody></table>

### Clavier

<table><thead><tr><th width="265">Action</th><th>Clavier sous Hypseus</th><th>Clavier sous Daphne</th></tr></thead><tbody><tr><td>Déplacements</td><td>Flèches directionnelles</td><td><p>Flèches directionnelles </p><p>(ou 8,4,2,6)</p></td></tr><tr><td>COIN 1</td><td>5</td><td>5 ou c</td></tr><tr><td>COIN 2</td><td>6</td><td>6</td></tr><tr><td>START 1</td><td>1</td><td>1</td></tr><tr><td>START 2</td><td>2</td><td>2</td></tr><tr><td>Bouton 1</td><td>CTRL gauche</td><td>CTRL gauche ou ESPACE</td></tr><tr><td>Bouton 2</td><td>ALT gauche</td><td>ALT gauche</td></tr><tr><td>Bouton 3</td><td>ESPACE</td><td>MAJ gauche</td></tr><tr><td>Skill 1</td><td>MAJ gauche</td><td>/</td></tr><tr><td>Skill 2</td><td>Z</td><td>*</td></tr><tr><td>Skill 3</td><td>X</td><td>-</td></tr><tr><td>SERVICE</td><td>9</td><td>9</td></tr><tr><td>TEST</td><td>F2</td><td>F2</td></tr><tr><td>RESET</td><td>0</td><td>F3</td></tr><tr><td>Screenshot</td><td>F12</td><td>F12</td></tr><tr><td>Quit</td><td>ECHAP</td><td>ECHAP ou q</td></tr><tr><td>Pause</td><td>P</td><td>P</td></tr><tr><td>Console</td><td>BACKLASH</td><td></td></tr><tr><td>Title</td><td>T</td><td>t</td></tr></tbody></table>

## Informations spécifiques au système

### Ajout de jeux DAPHNE

Les jeux DAPHNE se composent de 2 éléments:

* un dossier contenant les fichiers **videos**, \*.**dat** et \*.**txt** du jeu
* un fichier .zip placé dans un sous-répertoire **roms** du dossier des jeux

Pour ajouter des jeux DAPHNE, le dossier du jeu doit être placé dans le répertoire "**\roms\daphne**" et le nom du dossier doit être renommé en ajoutant **.daphne** au nom du jeu.

Par exemple, le dossier de jeu "**lair**" (Dragon's Lair) doit être renommé **lair.daphne**

```
roms\
└─ daphne\
   ├─ roms\
   │  └─ lair.zip
   └─ lair.daphne\
      └─ lair.dat
      └─ lair.m2v
      └─ lair.ogg
      └─ lair.txt
```

Une fois le jeu ajouté à la bibliothèque, il apparaît dans Retrobat en double.&#x20;

En effet le système détecte le répertoire .daphne mais également le fichier .zip.

<div align="left"><figure><img src="https://i.imgur.com/crqriZ1.png" alt=""><figcaption><p>lair appears twice</p></figcaption></figure></div>

Il est possible de masquer l'affichage du fichier zip depuis les [**OPTIONS D'AFFICHAGE**](../../../navigation/view-options.md#options-daffichage).&#x20;

Pour cela appuyer sur **SELECT**

<div align="left"><figure><img src="https://i.imgur.com/Orvrz9Z.png" alt=""><figcaption></figcaption></figure></div>

Sélectionner [**PERSONNALISER LA VUE**](../../../navigation/view-options.md#options-daffichage) puis EXTENSIONS

<div align="left"><figure><img src="https://i.imgur.com/4qx30od.png" alt=""><figcaption></figcaption></figure></div>

Décocher l'extension .zip.

<div align="left"><figure><img src="https://i.imgur.com/QQwL8qq.png" alt=""><figcaption></figcaption></figure></div>
