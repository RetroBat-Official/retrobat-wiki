# Visual Pinball

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/vpinball.svg" alt=""><figcaption></figcaption></figure>

</div>

Simulation de Flipper

{% embed url="https://en.wikipedia.org/wiki/Visual_Pinball" %}

{% embed url="https://www.vpforums.org/" %}

## Information

<table data-header-hidden><thead><tr><th width="198"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>vpinball</li></ul></td><td></td></tr><tr><td><strong>Dossier des tables</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span>roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> vpinball</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.vpx .7z .zip .rar</td><td></td></tr></tbody></table>

## BIOS

Aucun BIOS nécessaire.

## Contrôles

<table><thead><tr><th width="250">Manette</th><th width="152">Clavier</th><th width="443">Visual Pinball</th></tr></thead><tbody><tr><td>START</td><td>1</td><td>Démarrer la partie</td></tr><tr><td>SELECT</td><td>5</td><td>Insérer monnaie</td></tr><tr><td>D-PAD - HAUT</td><td>ESPACE</td><td>Taper le cabinet en avant</td></tr><tr><td>D-PAD - BAS</td><td>TAB</td><td></td></tr><tr><td>D-PAD - GAUCHE</td><td>Z</td><td>Taper le cabinet à gauche</td></tr><tr><td>D-PAD - DROITE</td><td>SLASH (/)</td><td>Taper le cabinet à droite</td></tr><tr><td>Stick analogique gauche</td><td></td><td></td></tr><tr><td>Stick analogique droit</td><td></td><td></td></tr><tr><td><img src="../../../.gitbook/assets/image (19).png" alt="A"></td><td>ENTER</td><td>Plunger</td></tr><tr><td><img src="../../../.gitbook/assets/image (6).png" alt="B"></td><td></td><td></td></tr><tr><td><img src="../../../.gitbook/assets/image (34).png" alt="" data-size="original"></td><td>PAUSE</td><td></td></tr><tr><td><img src="../../../.gitbook/assets/image (32).png" alt="" data-size="line"></td><td>RIGHTBRACE</td><td></td></tr><tr><td>L1</td><td>MAJ</td><td>Flipper gauche</td></tr><tr><td>R1</td><td>MAJ DROIT</td><td>Flipper droit</td></tr><tr><td>L2</td><td></td><td></td></tr><tr><td>R2</td><td></td><td></td></tr><tr><td>L3</td><td></td><td></td></tr><tr><td>R3</td><td></td><td></td></tr></tbody></table>

## Information spécifique au système

### Tables

Visual Pinball est complexe, chaque table peut nécessiter plusieurs types de fichiers:

* .vpx (table)
* .directb2s (vitre arrière)
* .UltraDMD (panneau d'information sous la vitre)
* fichier rom
* fichiers sons

Certaines tables fonctionnent avec uniquement un fichier .vpx, d'autres avec plusieurs des fichiers listés précédemment.

#### Fichiers vpx

Les fichiers vpx doivent être placés dans le dossier `\roms\vpinball\`.

#### Fichiers directb2s&#x20;

Les fichiers directb2s doivent être placés dans le dossier `\roms\vpinball\`, le nom doit être identique au fichier vpx:

<div align="left">

<figure><img src="https://i.imgur.com/muDyjzI.png" alt=""><figcaption></figcaption></figure>

</div>

#### Dossiers UltraDMD&#x20;

Les dossiers UltraDMD doivent être placés dans le dossier `\roms\vpinball\`, ne pas modifier le nom du dossier fourni avec la table:

<div align="left">

<figure><img src="https://i.imgur.com/LIDc6B0.png" alt=""><figcaption></figcaption></figure>

</div>

#### Fichiers ROM&#x20;

Les tables utilisant VPinMAME nécessitent l'ajout d'un fichier ROM au format .zip.

Ce fichier doit être placé dans le dossier `\emulators\vpinball\VPinMAME\roms` :&#x20;

<div align="left">

<figure><img src="https://i.imgur.com/TpXP6dI.png" alt=""><figcaption></figcaption></figure>

</div>

Lancer le programme **PinMAME32.exe** se trouvant dans le dossier `\emulators\vpinball\VPinMAME` pour connaître le nom du fichier ROM pour la table:

<div align="left">

<figure><img src="https://i.imgur.com/FMuBSQ3.png" alt=""><figcaption></figcaption></figure>

</div>

#### Fichiers audio

Des fichiers audio aux formats mp3 ou ogg sont requis pour certaines tables, ils doivent être placés dans le répertoire `\emulators\vpinball\Music` :

<div align="left">

<figure><img src="https://i.imgur.com/V3nna49.png" alt=""><figcaption></figcaption></figure>

</div>
