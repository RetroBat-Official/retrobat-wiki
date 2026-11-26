# Duke Nukem 3D

<div align="left"><figure><img src="../../../.gitbook/assets/image (759).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

**Duke Nukem 3D** (3D Realms, 1996) est un jeu de tir à la première personne sur le moteur Build, célèbre pour son humour et ses niveaux interactifs.

Ce système lance Duke Nukem 3D, ses extensions (**Duke It Out in D.C.**, **Duke Caribbean: Life's a Beach**, **Duke: Nuclear Winter**, **Penthouse Paradise**) et les mods.

RetroBat propose **eduke32** (par défaut) et **Raze**, un moteur moderne qui lance aussi les autres jeux Build (voir la page [**Raze**](raze.md)).

Les fichiers du jeu ne sont pas fournis : utilisez ceux de votre propre exemplaire (Steam, GOG, CD).

{% embed url="http://www.eduke32.com/" %}

## En bref

<table><thead><tr><th width="280.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\eduke32</code></td></tr><tr><td><strong>Extensions</strong></td><td>.eduke32</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>eduke32</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (manette du joueur 1)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu, sauvegarde / chargement rapide aux raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="170.75">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>eduke32</strong> (défaut)</td><td>Moteur de référence de Duke Nukem 3D, rendu logiciel d'origine ou OpenGL (packs HD), très compatible avec les mods.</td><td>Duke Nukem 3D seulement.</td></tr><tr><td><strong>raze</strong></td><td>Moteur moderne (OpenGL / Vulkan), mêmes fichiers de lancement <code>.eduke32</code>.</td><td>Moins de mods compatibles.</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire. Il faut les fichiers de votre jeu, par exemple dans `roms\eduke32\duke` :

<table><thead><tr><th width="316.5">Jeu</th><th>Fichiers</th></tr></thead><tbody><tr><td>Duke Nukem 3D (Atomic Edition)</td><td><code>DUKE3D.GRP</code> (et <code>DUKE.RTS</code>)</td></tr><tr><td>Duke It Out in D.C.</td><td><code>DUKEDC.GRP</code></td></tr><tr><td>Duke Caribbean: Life's a Beach</td><td><code>VACATION.GRP</code></td></tr><tr><td>Duke: Nuclear Winter</td><td><code>NWINTER.GRP</code></td></tr><tr><td>Duke Nukem's Penthouse Paradise</td><td><code>PENTHOUS.GRP</code> et son <code>GAME.CON</code></td></tr></tbody></table>

## Quel format de jeu ?

Un jeu se lance avec un fichier texte `.eduke32` placé dans `roms\eduke32`. Il indique, une ligne par paramètre, les fichiers à charger. Un chemin qui commence par `/` ou `\` part du dossier du fichier `.eduke32`.

<table><thead><tr><th width="104.5">Paramètre</th><th>Rôle</th><th>Équivalent</th></tr></thead><tbody><tr><td><code>FILE</code></td><td>Fichier principal du jeu (<code>.grp</code>, <code>.zip</code>)</td><td><code>-gamegrp</code></td></tr><tr><td><code>FILE+</code></td><td>Fichier ajouté (extension, mod)</td><td><code>-g</code></td></tr><tr><td><code>CON</code></td><td>Script principal</td><td><code>-x</code></td></tr><tr><td><code>CON+</code></td><td>Script ajouté</td><td><code>-mx</code></td></tr><tr><td><code>DEF</code></td><td>Fichier de définitions principal</td><td><code>-h</code></td></tr><tr><td><code>DEF+</code></td><td>Fichier de définitions ajouté</td><td><code>-mh</code></td></tr><tr><td><code>DIR</code></td><td>Dossier de recherche</td><td><code>-j</code></td></tr><tr><td><code>MAP</code></td><td>Carte à lancer</td><td><code>-map</code></td></tr></tbody></table>

`FILE`, `CON`, `DEF` et `MAP` ne sont lus qu'une fois ; `FILE+`, `CON+`, `DEF+` et `DIR` peuvent être répétés.

## Contrôles

### Configuration automatique

RetroBat configure la manette du joueur 1 (eduke32 n'en utilise qu'une) :

<table><thead><tr><th width="246.5">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Avancer, reculer, pas de côté</td></tr><tr><td>Stick droit</td><td>Tourner, regarder haut / bas</td></tr><tr><td>R2</td><td>Tirer</td></tr><tr><td>L2</td><td>Sauter</td></tr><tr><td>SUD</td><td>Ouvrir / utiliser</td></tr><tr><td>EST / OUEST</td><td>Inventaire (utiliser l'objet)</td></tr><tr><td>NORD</td><td>Coup de pied</td></tr><tr><td>L1</td><td>S'accroupir (maintenu)</td></tr><tr><td>R1</td><td>Tir secondaire</td></tr><tr><td>L3</td><td>Courir</td></tr><tr><td>R3</td><td>S'accroupir (bascule)</td></tr><tr><td>Croix gauche / droite</td><td>Objet précédent / suivant de l'inventaire</td></tr><tr><td>Croix haut / bas</td><td>Arme précédente / suivante</td></tr><tr><td>START</td><td>Menu</td></tr></tbody></table>

SELECT reste libre pour les raccourcis de RetroBat. Options utiles : **CONTRÔLES > INVERSER L'AXE Y**, **ZONE MORTE JOYSTICK**, **TOUJOURS COURIR** (activé par défaut), **VISÉE AUTOMATIQUE**.

### Raccourcis

<table><thead><tr><th width="227.75">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr><tr><td>HOTKEY + SUD</td><td>Menu (Échap)</td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarde rapide</td></tr><tr><td>HOTKEY + NORD</td><td>Chargement rapide</td></tr><tr><td>HOTKEY + R3</td><td>Capture d'écran</td></tr></tbody></table>

Pour plus de détails, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="301.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux et fichiers de lancement</td><td><code>roms\eduke32</code></td></tr><tr><td>Packs HD, sons et mods chargés automatiquement</td><td><code>roms\eduke32\autoload</code></td></tr><tr><td>Configuration</td><td><code>emulators\eduke32\eduke32.cfg</code>, <code>emulators\eduke32\settings.cfg</code></td></tr></tbody></table>

## Guides

### Exemples de fichiers .eduke32

Avec cette organisation :

```
roms\eduke32\
├── duke\
│   ├── DUKE3D.GRP
│   ├── DUKE.RTS
│   ├── DUKEDC.GRP
│   ├── VACATION.GRP
│   ├── NWINTER.GRP
│   ├── PENTHOUS.GRP
│   └── GAME.CON      (celui de Penthouse Paradise)
├── Duke Nukem 3D.eduke32
└── Duke It Out in D.C..eduke32
```

**Duke Nukem 3D**

```
FILE = /duke/DUKE3D.GRP
```

**Duke It Out in D.C.** (de même avec `VACATION.GRP` ou `NWINTER.GRP`)

```
FILE = /duke/DUKE3D.GRP
FILE+ = /duke/DUKEDC.GRP
```

**Duke Nukem's Penthouse Paradise**

```
FILE = /duke/DUKE3D.GRP
FILE+ = /duke/PENTHOUS.GRP
CON = /duke/GAME.CON
```

### Packs HD

Placez les packs (textures HD, sons, modèles 3D) dans `roms\eduke32\autoload`, puis activez **ÉMULATION > CHARGEMENT AUTO DU CONTENU** :

<div align="left"><figure><img src="../../../.gitbook/assets/image (761).png" alt=""><figcaption></figcaption></figure></div>

Exemple :

<div align="left"><figure><img src="https://i.imgur.com/MvPC3Qb.png" alt=""><figcaption></figcaption></figure></div>

Les textures HD et les modèles 3D demandent un rendu OpenGL : **VIDÉO > MOTEUR DE RENDU** sur POLYMOST ou POLYMER.

### Musique

**AUDIO > SORTIE MIDI** sur SOUNDFONT utilise la banque Roland SC-55 fournie avec RetroBat (`bios\scummvm\extra\Roland_SC-55.sf2`). Sans ce fichier, la musique repasse en émulation OPL3.

## Problèmes connus

<table><thead><tr><th width="319">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas ou ouvre l'écran de choix du jeu</td><td>Vérifiez les chemins du fichier <code>.eduke32</code> (ils partent du dossier du fichier).</td></tr><tr><td>Les packs HD ne s'affichent pas</td><td>Activez <strong>CHARGEMENT AUTO DU CONTENU</strong> et passez le rendu en POLYMOST ou POLYMER.</td></tr><tr><td>Le cadre décoratif n'apparaît pas</td><td>Il ne s'affiche qu'en plein écran fenêtré, sans résolution forcée.</td></tr></tbody></table>
