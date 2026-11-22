# Wolfenstein 3D

<div align="left"><figure><img src="../../../.gitbook/assets/image (706).png" alt="" width="479"><figcaption></figcaption></figure></div>

## Présentation

**Wolfenstein 3D** (id Software, 1992) est le jeu fondateur du jeu de tir à la première personne. RetroBat le lance avec le core libretro **ECWolf**, qui lance aussi **Spear of Destiny** et ses missions, ainsi que la version shareware.

ECWolf apporte la haute résolution, l'écran large et le jeu à la manette ou au clavier et à la souris.

Les fichiers des jeux ne sont pas fournis : utilisez ceux de vos propres exemplaires (Steam, GOG) ou la version shareware.

{% embed url="https://docs.libretro.com/library/ecwolf/" %}

## En bref

<table><thead><tr><th width="272.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\ecwolf</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pk3 .exe</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: ecwolf</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (manette, ou clavier et souris)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Oui</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire : les données du moteur (`ecwolf.pk3`) sont intégrées au core.

Il faut les fichiers du jeu :

<table><thead><tr><th width="287.75">Jeu</th><th>Extension des fichiers</th></tr></thead><tbody><tr><td>Wolfenstein 3D</td><td><code>.WL6</code></td></tr><tr><td>Wolfenstein 3D (shareware)</td><td><code>.WL1</code></td></tr><tr><td>Spear of Destiny</td><td><code>.SOD</code></td></tr><tr><td>Spear of Destiny (démo)</td><td><code>.SDM</code></td></tr><tr><td>Super 3-D Noah's Ark</td><td><code>.N3D</code></td></tr></tbody></table>

## Quel format de jeu ?

<table><thead><tr><th width="125.25">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.exe</strong></td><td>Exécutable DOS du jeu (<code>WOLF3D.EXE</code>, <code>SPEAR.EXE</code>) : le core lance le jeu du dossier du fichier.</td></tr><tr><td><strong>.pk3</strong></td><td>Mod au format ECWolf.</td></tr></tbody></table>

Placez chaque jeu dans son propre dossier de `roms\ecwolf`.

## Contrôles

### Configuration automatique

<table><thead><tr><th width="199">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Avancer, reculer, pas de côté</td></tr><tr><td>Stick droit</td><td>Tourner</td></tr><tr><td>Croix</td><td>Avancer, reculer, tourner</td></tr><tr><td>EST</td><td>Tirer</td></tr><tr><td>SUD</td><td>Utiliser (ouvrir les portes)</td></tr><tr><td>NORD</td><td>Courir (maintenu)</td></tr><tr><td>OUEST</td><td>Afficher la barre d'état</td></tr><tr><td>L1 / R1</td><td>Pas de côté à gauche / à droite</td></tr><tr><td>L2 / R2</td><td>Arme précédente / suivante</td></tr><tr><td>SELECT</td><td>Carte</td></tr><tr><td>START</td><td>Menu</td></tr></tbody></table>

Options utiles : **CONTRÔLES > TOUJOURS COURIR** (NORD fait alors marcher), **ZONE MORTE ANALOGIQUE(CORE)**, **SENSIBILITÉ ANALOGIQUE(CORE)**.

### Clavier et souris

Le clavier et la souris marchent en même temps que la manette. **CONTRÔLES > CLAVIER ET SOURIS** donne tout le clavier au jeu et capture la souris : la touche `Arrêt défil` rend le clavier aux raccourcis de RetroArch. **CONTRÔLES > SENSIBILITÉ DE LA SOURIS** règle la vitesse de rotation (10 par défaut).

<table><thead><tr><th width="256.5">Clavier / souris</th><th>Action</th></tr></thead><tbody><tr><td>Flèches haut / bas, W / S</td><td>Avancer, reculer</td></tr><tr><td>Flèches gauche / droite</td><td>Tourner</td></tr><tr><td>A / D (ou <code>,</code> / <code>.</code>)</td><td>Pas de côté</td></tr><tr><td>Souris</td><td>Tourner</td></tr><tr><td>Ctrl, Entrée, clic gauche</td><td>Tirer</td></tr><tr><td>Espace, clic droit</td><td>Utiliser (ouvrir les portes)</td></tr><tr><td>Maj</td><td>Courir</td></tr><tr><td><code>[</code> / <code>]</code></td><td>Arme précédente / suivante</td></tr><tr><td>Tab</td><td>Carte</td></tr><tr><td>Échap</td><td>Menu</td></tr></tbody></table>

### Raccourcis

Raccourcis de RetroArch, sauvegardes instantanées comprises. Voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="314">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\ecwolf\&#x3C;jeu></code></td></tr><tr><td>Sauvegardes du jeu et sauvegardes instantanées</td><td><code>saves\ecwolf</code></td></tr></tbody></table>

## Guides

### Organisation des fichiers

```
roms\ecwolf\
├── Wolfenstein 3D\
│   ├── WOLF3D.EXE
│   ├── AUDIOHED.WL6
│   ├── AUDIOT.WL6
│   ├── GAMEMAPS.WL6
│   ├── MAPHEAD.WL6
│   ├── VGADICT.WL6
│   ├── VGAGRAPH.WL6
│   ├── VGAHEAD.WL6
│   └── VSWAP.WL6
└── Spear of Destiny\
    ├── SPEAR.EXE
    └── *.SOD
```

### Options

* **RÉSOLUTION INTERNE** jusqu'à 2560x1600, **VIDÉO > TAUX DE RAFRAÎCHISSEMENT (FPS)** jusqu'à 240 images par seconde.
* **VIDÉO > RAPPORT D'ASPECT DU CORE** règle l'image quand le **RAPPORT D'ASPECT** est sur AUTO.

## Problèmes connus

<table><thead><tr><th width="280.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le core ne trouve pas le jeu</td><td>Les fichiers <code>.WL6</code> / <code>.SOD</code> doivent être dans le même dossier que le fichier lancé.</td></tr></tbody></table>
