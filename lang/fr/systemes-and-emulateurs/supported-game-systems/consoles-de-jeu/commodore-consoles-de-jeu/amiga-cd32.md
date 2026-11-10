---
description: Commodore
---

# Amiga CD32

<div align="left"><figure><img src="../../../../.gitbook/assets/image (488).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

L'**Amiga CD32** est la console de jeux de la famille Amiga, sortie par Commodore en septembre 1993. Présentée comme la première console CD 32 bits en Europe, elle reprend l'Amiga 1200 : processeur Motorola 68EC020, jeu de puces **AGA**, 2 Mo de mémoire, avec en plus un lecteur CD-ROM double vitesse et la puce Akiko, qui accélère certains effets 3D. Sa manette compte 7 boutons : quatre boutons de couleur (rouge, bleu, vert, jaune), deux boutons de tranche (retour rapide, avance rapide) et Play.

La CD32 a reçu environ 150 jeux. Beaucoup sont des jeux Amiga 1200 enrichis de musiques CD, d'introductions ou de voix : _Microcosm_, _Super Stardust_, _Banshee_, _Guardian_, _Liberation_, _Fears_, _The Chaos Engine_, _Beneath a Steel Sky_ entièrement parlé… Commodore a fait faillite en avril 1994, quelques mois seulement après la sortie.

{% embed url="https://fr.wikipedia.org/wiki/Amiga_CD32" %}

## En bref

<table><thead><tr><th width="250.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\amigacd32</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .chd .iso .ccd .nrg .mds .lha .rp9 .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: puae</td></tr><tr><td><strong>BIOS</strong></td><td><code>kick40060.CD32</code> + <code>kick40060.CD32.ext</code> (ou <code>amiga-os-310-cd32.rom</code> + <code>amiga-os-310-cd32-ext.rom</code>)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, sauf Amiga Forever</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, Amiberry</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                   | Points forts                                                           | Limites                                                                 |
| --------------------------- | ---------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| **libretro: puae** (défaut) | Fiable, manette CD32 complète, options CD, une sauvegarde par jeu      |                                                                         |
| libretro: amiberry          | Moteur UAE récent, .rp9                                                | Manette CD32 non émulée : seuls les boutons de tir 1 et 2 (pas de Play) |
| amiberry                    | Version standalone : manette CD32 complète, menu Amiberry              |                                                                         |
| winuae                      | L'émulateur Amiga de référence, le plus précis                         |                                                                         |
| amigaforever                | Lance les paquets .rp9 de l'offre commerciale Amiga Forever de Cloanto | Amiga Forever doit être installé, pas d'autoconfiguration               |

## BIOS

### Fichiers obligatoires

La CD32 a besoin de **deux** ROM : son Kickstart et sa ROM étendue. Copiez-les dans le dossier `bios` (ou `bios\amiga`).

| Fichier               | Nom court          | Nom Amiga Forever         | MD5 (nom court)                  | Utilisé pour                              |
| --------------------- | ------------------ | ------------------------- | -------------------------------- | ----------------------------------------- |
| Kickstart 3.1 CD32    | kick40060.CD32     | amiga-os-310-cd32.rom     | 5f8924d013dd57a89cf349f4cdedc6b1 | **Obligatoire**                           |
| ROM étendue CD32      | kick40060.CD32.ext | amiga-os-310-cd32-ext.rom | bb72565701b1b6faece07d68ea5da639 | **Obligatoire**                           |
| Kickstart 3.1 (A1200) | kick40068.A1200    | amiga-os-310-a1200.rom    | 646773759326fbac3b2311fd8c8793ee | Optionnel – jeux WHDLoad (.lha)           |
| Clé Amiga Forever     | rom.key            |                           |                                  | Optionnel – ROM chiffrées d'Amiga Forever |

{% hint style="info" %}
RetroBat vérifie la présence des deux fichiers CD32. Les autres fichiers sont indiqués comme OPTIONAL.
{% endhint %}

### Quel nom de fichier utiliser ?

* Les **noms courts** (`kick40060.CD32`, `kick40060.CD32.ext`) fonctionnent avec tous les émulateurs : utilisez-les en cas de doute.
* Les ROM Amiga Forever sont chiffrées : copiez à côté le fichier **rom.key** fourni avec Amiga Forever.
* Certains packs contiennent une ROM CD32 « combinée » de 1 Mo. Seul lr-puae la lit : préférez les deux fichiers séparés.

### Choisir le modèle de CD32

Par défaut, RetroBat émule une CD32 standard (2 Mo de mémoire). Certains jeux tournent mieux avec 8 Mo de Fast RAM en plus (sous-menu ÉMULATION) :

<table><thead><tr><th width="179.5">Émulateur</th><th>Option</th><th>Choix</th></tr></thead><tbody><tr><td>lr-puae</td><td>MODÈLE</td><td>CD32, CD32 + 8 Mo de Fast</td></tr><tr><td>lr-amiberry</td><td>MODÈLE</td><td>CD32, CD32 + 8 Mo de Fast</td></tr><tr><td>Amiberry</td><td>MODÈLE</td><td>CD32, CD32 + 8 Mo de Fast</td></tr><tr><td>WinUAE</td><td>FAST RAM / ACTIVER LE JIT / UTILISER LE FPU</td><td>+8 Mo de Fast RAM, JIT et FPU</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (489).png" alt=""><figcaption></figcaption></figure></div>

## Quel format pour les jeux ?

### Formats

<table><thead><tr><th width="186.5">Format</th><th>Description</th></tr></thead><tbody><tr><td>.chd</td><td>Image CD compressée, un seul fichier par jeu, avec les pistes audio. <strong>Recommandé</strong></td></tr><tr><td>.cue (+ .bin)</td><td>Image CD avec ses pistes audio</td></tr><tr><td>.iso</td><td>Image CD sans les pistes audio : la musique CD manque</td></tr><tr><td>.ccd / .nrg / .mds</td><td>Autres formats d'image CD (CloneCD, Nero, Alcohol)</td></tr><tr><td>.lha</td><td>Version <strong>WHDLoad</strong> d'un jeu CD32</td></tr><tr><td>.rp9</td><td>Paquet Amiga Forever (Amiga Forever, lr-amiberry, lr-puae)</td></tr><tr><td>.zip / .7z</td><td>Images CD compressées, <strong>cores libretro uniquement</strong></td></tr></tbody></table>

{% hint style="success" %}
Préférez le **.chd** : un seul fichier par jeu, plus léger, avec la musique CD. Pour convertir un jeu .cue/.bin : `chdman createcd -i "jeu.cue" -o "jeu.chd"`.
{% endhint %}

## Contrôles

### Configuration automatique des manettes

| Émulateur     | Configuration auto | Joueurs |
| ------------- | ------------------ | ------- |
| lr-puae       | Oui                | 2       |
| lr-amiberry   | Oui                | 2       |
| Amiberry      | Oui                | 2       |
| WinUAE        | Oui                | 2       |
| Amiga Forever | Non                |         |

La manette du joueur 1 va dans le port 2 de la console, celle du joueur 2 dans le port 1.

### Disposition par défaut

<table><thead><tr><th width="310.25">Manette CD32</th><th>lr-puae, Amiberry</th></tr></thead><tbody><tr><td>Croix</td><td>Croix</td></tr><tr><td>Rouge</td><td>SUD</td></tr><tr><td>Bleu</td><td>EST</td></tr><tr><td>Vert</td><td>OUEST</td></tr><tr><td>Jaune</td><td>NORD</td></tr><tr><td>Retour rapide</td><td>L1</td></tr><tr><td>Avance rapide</td><td>R1</td></tr><tr><td>Play</td><td>START</td></tr><tr><td>Clavier virtuel</td><td>SELECT</td></tr><tr><td>Menu de l'émulateur (Amiberry)</td><td>R3</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (490).png" alt="" width="225"><figcaption></figcaption></figure></div>

WinUAE émule aussi la manette CD32 complète. Avec lr-amiberry, seuls les boutons rouge et bleu fonctionnent pour l'instant.

### Options de contrôle utiles

<table><thead><tr><th width="155.75">Émulateur</th><th>Option</th><th>Description</th></tr></thead><tbody><tr><td>lr-puae</td><td>DISPOSITION DES BOUTONS DE LA MANETTE</td><td>Faire tourner les boutons de façade et/ou sauter avec le bouton bleu</td></tr><tr><td>lr-puae</td><td>TYPE DE CONTRÔLEUR JOUEUR 1</td><td>Laissez sur AUTO : la manette CD32 est choisie automatiquement</td></tr><tr><td>Amiberry</td><td>TYPE DE CONTRÔLEUR</td><td>Manette CD32 par défaut sur ce système</td></tr><tr><td>Amiberry</td><td>PÉRIPHÉRIQUE PORT 1</td><td>Joystick (joueur 2), souris ou rien dans le second port</td></tr><tr><td>WinUAE</td><td>MODE DE LA MANETTE / DEUXIÈME MANETTE</td><td>Manette CD32 ou joystick, joueur 2 ou souris dans le second port</td></tr></tbody></table>

### Raccourcis

**Cores libretro** : [raccourcis standards de RetroBat](../../../../navigation/hotkeys.md).

| Raccourci      | Amiberry           | WinUAE  | Amiga Forever |
| -------------- | ------------------ | ------- | ------------- |
| HOTKEY + START | Quitter            | Quitter |               |
| HOTKEY + OUEST | Sauvegarder l'état |         |               |
| HOTKEY + NORD  | Charger l'état     |         |               |

START seul correspond au bouton Play de la manette CD32. Le menu d'Amiberry s'ouvre avec R3 ou F12, celui de WinUAE avec F12.

## Dossiers

<table><thead><tr><th width="125.75">Émulateur</th><th>Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>lr-puae</td><td>Sauvegardes des jeux (NVRAM, une par jeu)</td><td><code>saves\amigacd32</code></td></tr><tr><td>lr-amiberry</td><td>Sauvegardes des jeux</td><td><code>saves\amigacd32\LR-amiberry</code></td></tr><tr><td>libretro</td><td>Sauvegardes d'état</td><td><code>saves\amigacd32\libretro.&#x3C;core></code></td></tr><tr><td>Amiberry</td><td>Sauvegardes d'état, sauvegardes des jeux (NVRAM)</td><td><code>saves\amigacd32\amiberry</code></td></tr><tr><td>Amiberry</td><td>Captures d'écran</td><td><code>screenshots\amiberry</code></td></tr><tr><td>WinUAE</td><td>Sauvegardes d'état</td><td><code>saves\amigacd32\winuae</code></td></tr><tr><td>WinUAE</td><td>Sauvegardes des jeux (NVRAM)</td><td><code>saves\amigacd32\winuae\nvram</code></td></tr><tr><td>WinUAE</td><td>Captures d'écran / vidéos</td><td><code>screenshots\winuae</code> / <code>records\winuae</code></td></tr></tbody></table>

## Guides

### Sauvegardes des jeux

Les jeux CD32 sauvegardent dans la petite mémoire interne de la console (NVRAM). Chaque émulateur la garde dans son propre dossier de sauvegardes : changer d'émulateur ne reprend pas vos sauvegardes. Avec lr-puae, chaque jeu a son propre fichier de sauvegarde, la mémoire n'est donc jamais pleine.

### Jeux WHDLoad

Certains jeux CD32 existent aussi en version WHDLoad (.lha). Ils démarrent comme sur un Amiga 1200 et demandent le Kickstart 3.1 (A1200). Vous pouvez aussi les placer dans le système Amiga AGA : voir la page Amiga 1200.

## Problèmes connus

<table><thead><tr><th width="339">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>« Kickstart not found » ou écran noir</td><td>Copiez kick40060.CD32 <strong>et</strong> kick40060.CD32.ext dans le dossier bios.</td></tr><tr><td>Les ROM Amiga Forever ne fonctionnent pas</td><td>Copiez rom.key à côté.</td></tr><tr><td>Pas de musique dans le jeu</td><td>Le format .iso n'a pas l'audio CD : utilisez une image .cue/.bin ou .chd.</td></tr><tr><td>Le jeu reste sur le logo CD32 ou ne charge pas</td><td>Avec lr-puae, activez DÉLAI D'INSERTION DU CD. Sinon, essayez le modèle CD32 + 8 Mo de Fast ou un autre émulateur.</td></tr><tr><td>Les boutons Play, vert ou jaune ne font rien</td><td>lr-amiberry n'émule pas encore la manette CD32 : utilisez lr-puae, Amiberry ou WinUAE.</td></tr><tr><td>Un jeu .zip/.7z ne démarre pas</td><td>Seuls les cores libretro lisent les archives : décompressez-le, ou convertissez-le en .chd.</td></tr><tr><td>Les sauvegardes ont disparu après un changement d'émulateur</td><td>Chaque émulateur a ses propres sauvegardes : revenez à l'émulateur précédent.</td></tr></tbody></table>
