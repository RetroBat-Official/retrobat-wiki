# Quake 2

<div align="left"><figure><img src="../../../.gitbook/assets/image (808).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**Quake II** (id Software, 1997) est la suite de Quake : une campagne de science-fiction contre les Strogg, avec des niveaux reliés entre eux et un mode multijoueur devenu une référence.

Ce système lance **Quake II**, ses packs de mission (**The Reckoning**, **Ground Zero**), **Zaero**, **Capture The Flag** et les mods.

RetroBat propose le core libretro **vitaquake2** (par défaut) et **vkQuake2**, un moteur en Vulkan.

Les fichiers du jeu ne sont pas fournis : utilisez ceux de votre propre exemplaire.

{% embed url="https://github.com/libretro/vitaquake2" %}

{% embed url="https://github.com/kondrak/vkQuake2" %}

## En bref

<table><thead><tr><th width="286.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\quake2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pak .quake2</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: vitaquake2</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique avec le core vitaquake2 ; vkQuake2 : clavier et souris</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu (vkQuake2 : sauvegarde / chargement rapide aux raccourcis)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="190.75">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: vitaquake2</strong> (défaut)</td><td>Manette configurée, menus compris ; raccourcis de RetroArch ; RetroBat choisit seul le core du pack de mission (The Reckoning, Ground Zero, Zaero).</td><td>Pas de sauvegardes instantanées. Jeu de base et ces trois packs seulement : pas de Capture The Flag ni de mods.</td></tr><tr><td><strong>vkquake2</strong></td><td>Rendu Vulkan, tous les packs de mission et les mods. Sauvegarde et chargement rapides aux raccourcis.</td><td>Fait pour le clavier et la souris : la manette n'a aucune commande par défaut et les menus ne se pilotent pas à la manette.</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire. Il faut en revanche les fichiers du jeu :

<table><thead><tr><th>Jeu</th><th width="122">Dossier</th><th>Fichiers</th></tr></thead><tbody><tr><td>Quake II</td><td><code>baseq2</code></td><td><code>pak0.pak</code>, <code>pak1.pak</code>, <code>pak2.pak</code></td></tr><tr><td>The Reckoning (pack de mission 1)</td><td><code>xatrix</code></td><td><code>pak0.pak</code></td></tr><tr><td>Ground Zero (pack de mission 2)</td><td><code>rogue</code></td><td><code>pak0.pak</code></td></tr><tr><td>Zaero</td><td><code>zaero</code></td><td><code>pak0.pak</code></td></tr><tr><td>Capture The Flag</td><td><code>ctf</code></td><td><code>pak0.pak</code></td></tr></tbody></table>

Les versions vendues aujourd'hui (Steam, GOG) contiennent ces fichiers.

## Quel format de jeu ?

<table><thead><tr><th width="151.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.pak</strong></td><td>Fichier de données du jeu. Le jeu lancé est celui du dossier du fichier (<code>baseq2</code>, <code>xatrix</code>, <code>rogue</code>, mod…).</td></tr><tr><td><strong>.quake2</strong></td><td>Fichier de lancement placé dans <code>roms\quake2</code> : il indique le dossier du jeu à lancer (voir <a href="quake-2.md#fichiers-de-lancement-.quake2"><strong>Guides</strong></a>).</td></tr></tbody></table>

Organisation conseillée de `roms\quake2` : le jeu de base dans `baseq2`, chaque pack de mission ou mod dans son propre dossier, à côté.

```
roms\quake2\
├── baseq2\
│   ├── pak0.pak
│   ├── pak1.pak
│   ├── pak2.pak
│   ├── music\
│   │   ├── track02.ogg
│   │   └── ...
│   ├── video\
│   └── players\
├── xatrix\
│   ├── pak0.pak
│   └── video\
├── rogue\
│   ├── pak0.pak
│   └── video\
├── zaero\
│   └── pak0.pak
├── ctf\
│   └── pak0.pak
└── Quake II.quake2
```

La musique (pistes du CD) se place en `.ogg` dans le dossier `music` de chaque jeu (`track02.ogg`, `track03.ogg`…).

## Contrôles

### Configuration automatique

**Core vitaquake2** : la manette est configurée automatiquement.

<table><thead><tr><th width="277.75">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Avancer, reculer, pas de côté</td></tr><tr><td>Stick droit</td><td>Regarder</td></tr><tr><td>R2</td><td>Tirer</td></tr><tr><td>L2</td><td>Sauter, monter</td></tr><tr><td>R1</td><td>S'accroupir, descendre</td></tr><tr><td>L1</td><td>Courir</td></tr><tr><td>OUEST</td><td>Arme suivante</td></tr><tr><td>Croix gauche / droite</td><td>Ouvrir l'inventaire / utiliser l'objet</td></tr><tr><td>Croix haut / bas</td><td>Objet précédent / suivant</td></tr><tr><td>R3</td><td>Jeter l'objet</td></tr><tr><td>SELECT</td><td>Ordinateur de mission</td></tr><tr><td>START</td><td>Menu</td></tr><tr><td>EST / SUD</td><td>Valider / retour (menus)</td></tr></tbody></table>

* **CONTRÔLES > TYPE DE CONTRÔLEUR > CLAVIER/SOURIS** joue au clavier et à la souris : RetroBat donne alors tout le clavier au jeu et capture la souris. La touche `Arrêt défil` rend le clavier aux raccourcis de RetroArch.
* **CONTRÔLES > INVERSER L'AXE VERTICAL** inverse le regard haut / bas.
* **CONTRÔLES > SENSIBILITÉ DE LA SOURIS** règle la vitesse de la caméra, au stick droit comme à la souris.

**vkQuake2** : jouez au clavier et à la souris. **CONTRÔLES > UTILISER LE JOYSTICK** active la manette, mais vkQuake2 n'utilise que la première manette trouvée par Windows, sans bouton assigné : il faut associer les boutons dans le menu du jeu (**Options > Customize Controls**), au clavier. Dans les menus du jeu, tous les boutons de la manette valident.

### Raccourcis

* **Core vitaquake2** : raccourcis de RetroArch (avance rapide, captures…), sans sauvegardes instantanées : sauvegardez depuis le menu du jeu.
* **vkQuake2** :

<table><thead><tr><th width="237.75">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarde rapide</td></tr><tr><td>HOTKEY + NORD</td><td>Chargement rapide</td></tr><tr><td>HOTKEY + R3</td><td>Capture d'écran</td></tr></tbody></table>

Pour plus de détails, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="299">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux et mods</td><td><code>roms\quake2</code></td></tr><tr><td>Core vitaquake2 : sauvegardes et configuration</td><td><p><code>saves\quake2\&#x3C;dossier du jeu></code></p><p>(par exemple <code>saves\quake2\baseq2</code>)</p></td></tr><tr><td>vkQuake2 : sauvegardes</td><td><code>roms\quake2\&#x3C;dossier du jeu>\save</code></td></tr><tr><td>vkQuake2 : configuration</td><td><code>roms\quake2\baseq2\config.cfg</code> (ou <code>config.cfg</code> du dossier du pack de mission, s'il existe)</td></tr><tr><td>vkQuake2 : captures d'écran</td><td><code>roms\quake2\&#x3C;dossier du jeu>\scrnshot</code></td></tr></tbody></table>

## Guides

### Lancer un pack de mission ou un mod

Lancez un fichier `.pak` du dossier du jeu (par exemple `xatrix\pak0.pak`) : RetroBat lance le jeu de ce dossier.

* **Core vitaquake2** : un core existe pour chaque jeu (vitaquake2, vitaquake2-xatrix, vitaquake2-rogue, vitaquake2-zaero). RetroBat choisit seul le bon d'après le dossier : gardez le core **vitaquake2**. Capture The Flag (`ctf`), les autres packs et les mods ne sont pas pris en charge : RetroBat affiche un message, lancez-les avec vkquake2.
* **vkQuake2** : tous les dossiers sont acceptés. Chaque jeu a besoin de sa bibliothèque (`gamex64.dll`) dans son dossier : RetroBat copie celle fournie avec vkQuake2 quand elle manque (jeu de base et packs de mission). Un mod doit fournir la sienne.

### Fichiers de lancement (.quake2)

Un fichier `.quake2` est un fichier texte placé dans `roms\quake2`. Il apparaît dans la liste des jeux avec son nom.

* Sa première ligne donne le dossier du jeu, par exemple `xatrix`.
* Si le fichier est vide, RetroBat lance le dossier qui porte le même nom que le fichier (`zaero.quake2` lance `zaero`).
* Les anciens fichiers de RetroBat continuent de fonctionner (nom contenant `rogue`, `xatrix` ou `zaero` ; sinon Quake II).

<div align="left"><figure><img src="../../../.gitbook/assets/image (809).png" alt=""><figcaption></figcaption></figure></div>

### Options utiles

* **Core vitaquake2** : **PILOTES > PILOTE VIDÉO DU CORE** (OPENGL par défaut, ou LOGICIEL). Les résolutions internes marquées OPENGL UNIQUEMENT demandent le rendu OpenGL.

## Problèmes connus

<table><thead><tr><th width="349">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Message « vitaQuake II does not support the game folder »</td><td>Ce dossier (Capture The Flag, mod) n'est pas pris en charge par le core : choisissez l'émulateur vkquake2 pour ce jeu.</td></tr><tr><td>La manette ne fait rien avec vkQuake2</td><td>Activez <strong>CONTRÔLES > UTILISER LE JOYSTICK</strong> et associez les boutons dans le menu du jeu, ou utilisez le core vitaquake2.</td></tr><tr><td>Un mod ne démarre pas avec vkQuake2</td><td>Il lui faut sa propre <code>gamex64.dll</code> (version 64 bits) dans son dossier.</td></tr><tr><td>Pas de musique</td><td>Placez les pistes en <code>.ogg</code> dans le dossier <code>music</code> du jeu.</td></tr></tbody></table>
