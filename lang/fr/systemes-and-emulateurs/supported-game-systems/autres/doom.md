# Doom

<div align="left"><figure><img src="../../../.gitbook/assets/image (624).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

**Doom** (id Software, 1993) a lancé le jeu de tir à la première personne sur PC. Son moteur a servi à de nombreux autres jeux et à des milliers de mods créés par les joueurs, toujours actifs aujourd'hui.

Ce système lance les jeux de ce moteur avec des moteurs modernes : **Doom**, **The Ultimate Doom**, **Doom II**, **Final Doom** (TNT: Evilution, The Plutonia Experiment), **Heretic**, **Hexen**, **Strife**, **Chex Quest**, **Freedoom**, et les mods (cartes, épisodes, conversions totales comme **SIGIL** ou **Brutal Doom**).

RetroBat propose **UZDoom** (par défaut, successeur de GZDoom), **GZDoom** et le core libretro **prboom**.

Les fichiers des jeux ne sont pas fournis : utilisez ceux de votre propre exemplaire, ou **Freedoom**, un jeu libre et gratuit compatible avec les mods Doom.

{% embed url="https://github.com/UZDoom/uzdoom" %}

{% embed url="https://zdoom.org/index" %}

## En bref

<table><thead><tr><th width="280.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\doom</code></td></tr><tr><td><strong>Extensions</strong></td><td>.wad .iwad .pwad .pk3 .ipk3 .gzdoom .uzdoom</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>uzdoom</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Commandes par défaut d'UZDoom et de GZDoom ; automatique avec le core prboom</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core prboom ; UZDoom et GZDoom : sauvegardes du jeu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="162">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>uzdoom</strong> (défaut)</td><td>Le plus complet : rendu OpenGL ou Vulkan, haute résolution, presque tous les mods (formats ZDoom, <code>.pk3</code>), Heretic, Hexen et Strife, manette reconnue directement.</td><td>Pas de sauvegardes instantanées : sauvegardes du jeu, depuis son menu.</td></tr><tr><td><strong>gzdoom</strong></td><td>Version précédente du même moteur.</td><td>Mêmes limites qu'UZDoom.</td></tr><tr><td><strong>libretro: prboom</strong></td><td>Rendu fidèle au Doom d'origine, sauvegardes instantanées, raccourcis de RetroArch, mods Boom, MBF et MBF21.</td><td>Moins de mods ZDoom compatibles.</td></tr></tbody></table>

Pour changer d'émulateur, pour tout le système ou pour un seul jeu, voir la page **Configuration des systèmes et des jeux**.

## BIOS

Aucun BIOS n'est nécessaire. Il faut en revanche les fichiers du jeu (**IWAD**) :

<table><thead><tr><th width="292.75">Jeu</th><th>Fichier</th></tr></thead><tbody><tr><td>Doom, The Ultimate Doom</td><td><code>doom.wad</code></td></tr><tr><td>Doom (version shareware, gratuite)</td><td><code>doom1.wad</code></td></tr><tr><td>Doom II</td><td><code>doom2.wad</code></td></tr><tr><td>Final Doom</td><td><code>tnt.wad</code>, <code>plutonia.wad</code></td></tr><tr><td>Heretic</td><td><code>heretic.wad</code></td></tr><tr><td>Hexen</td><td><code>hexen.wad</code> (extension : <code>hexdd.wad</code>)</td></tr><tr><td>Strife</td><td><code>strife1.wad</code></td></tr><tr><td>Chex Quest</td><td><code>chex.wad</code></td></tr><tr><td>Freedoom (libre)</td><td><code>freedoom1.wad</code>, <code>freedoom2.wad</code></td></tr></tbody></table>

Les versions vendues aujourd'hui (Steam, GOG, réédition **Doom + Doom II**) contiennent ces fichiers.

## Quel format de jeu ?

<table><thead><tr><th width="197.75">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.wad</strong> / <strong>.iwad</strong></td><td>Jeu complet (IWAD) ou mod (PWAD).</td></tr><tr><td><strong>.pwad</strong></td><td>Mod : il a besoin de l'IWAD du jeu (voir <a href="doom.md#lancer-un-mod-pwad"><strong>Guides</strong></a>).</td></tr><tr><td><strong>.pk3</strong> / <strong>.ipk3</strong></td><td>Mod au format ZDoom (<code>.pk3</code>) ou jeu complet (<code>.ipk3</code>).</td></tr><tr><td><strong>.uzdoom</strong> / <strong>.gzdoom</strong></td><td>Fichier ou dossier de lancement : jeu et mods à charger ensemble (voir <a href="doom.md#charger-plusieurs-fichiers-.uzdoom-.gzdoom"><strong>Guides</strong></a>).</td></tr></tbody></table>

Organisation conseillée de `roms\doom` : un dossier par jeu, avec ses mods à côté ou dans un sous-dossier.

```
roms\doom\
├── Doom\
│   ├── doom.wad
│   └── SIGIL\
│       └── SIGIL.wad
└── Doom II\
    ├── doom2.wad
    └── Brutal Doom.uzdoom
```

## Contrôles

### Configuration automatique

**UZDoom** reconnaît la manette directement, avec ses commandes par défaut :

<table><thead><tr><th width="266.5">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Avancer, reculer, pas de côté</td></tr><tr><td>Stick droit</td><td>Tourner, regarder en haut et en bas</td></tr><tr><td>R2 / L2</td><td>Tirer / tir secondaire</td></tr><tr><td>SUD</td><td>Utiliser (ouvrir une porte, actionner)</td></tr><tr><td>EST</td><td>S'accroupir</td></tr><tr><td>OUEST</td><td>Recharger</td></tr><tr><td>NORD</td><td>Sauter</td></tr><tr><td>L1 / R1</td><td>Arme précédente / arme suivante</td></tr><tr><td>R3</td><td>Zoom</td></tr><tr><td>Croix : gauche / droite / bas</td><td>Objet précédent / suivant / utiliser l'objet</td></tr><tr><td>START</td><td>Menu</td></tr><tr><td>SELECT</td><td>Carte</td></tr></tbody></table>

Les commandes se changent dans le menu d'UZDoom (**Options > Customize Controls**). Avec GZDoom, moins de boutons sont associés par défaut : complétez-les dans le même menu.

**Core prboom** : **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit la disposition, MANETTE CLASSIQUE (par défaut, inspirée de Doom sur PlayStation) ou MANETTE MODERNE (sticks, inspirée de Doom 3 sur Xbox).

<table><thead><tr><th width="200.75">Manette RetroBat</th><th width="249.25">Manette classique</th><th>Manette moderne</th></tr></thead><tbody><tr><td>Croix</td><td>Se déplacer</td><td>—</td></tr><tr><td>Stick gauche</td><td>—</td><td>Avancer, reculer, pas de côté</td></tr><tr><td>Stick droit</td><td>—</td><td>Tourner</td></tr><tr><td>NORD</td><td>Tirer</td><td>Arme précédente</td></tr><tr><td>EST</td><td>Utiliser</td><td>Arme suivante</td></tr><tr><td>SUD</td><td>Pas de côté (maintenir)</td><td>Dernier message</td></tr><tr><td>OUEST</td><td>Courir</td><td>Utiliser</td></tr><tr><td>L1 / R1</td><td>Pas de côté gauche / droite</td><td>Chargement / sauvegarde rapide</td></tr><tr><td>L2 / R2</td><td>Arme précédente / suivante</td><td>Courir / tirer</td></tr><tr><td>L3</td><td>Courir (activer / désactiver)</td><td>Courir (activer / désactiver)</td></tr><tr><td>R3</td><td>Demi-tour</td><td>Demi-tour</td></tr><tr><td>START</td><td>Menu</td><td>Menu</td></tr><tr><td>SELECT</td><td>Carte</td><td>Carte</td></tr></tbody></table>

CLAVIER/SOURIS joue au clavier et à la souris. **CONTRÔLES > ACTIVER LA SOURIS** ajoute la souris aux dispositions manette.

### Raccourcis

* **UZDoom, GZDoom** : HOTKEY + START quitte le jeu. Les sauvegardes passent par le menu du jeu, ou par les touches de Doom : `F2` sauvegarder, `F3` charger, `F6` sauvegarde rapide, `F9` chargement rapide.
* **Core prboom** : raccourcis de RetroArch (sauvegardes instantanées, avance rapide…).

Pour plus de détails, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="335.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux et mods</td><td><code>roms\doom</code></td></tr><tr><td>UZDoom : sauvegardes</td><td><code>saves\uzdoom</code></td></tr><tr><td>GZDoom : sauvegardes</td><td><code>saves\gzdoom</code></td></tr><tr><td>Core prboom : sauvegardes</td><td><code>saves\doom</code></td></tr><tr><td>Core prboom : sauvegardes instantanées</td><td><code>saves\doom\libretro.prboom</code></td></tr><tr><td>UZDoom, GZDoom : captures d'écran</td><td><code>screenshots\uzdoom</code>, <code>screenshots\gzdoom</code></td></tr><tr><td>UZDoom, GZDoom : configuration</td><td><code>emulators\uzdoom\uzdoom_portable.ini</code>, <code>emulators\gzdoom\gzdoom_portable.ini</code></td></tr></tbody></table>

## Guides

### Lancer un mod (PWAD)

Placez le mod à côté de l'IWAD du jeu, ou dans un sous-dossier, puis lancez le mod depuis la liste des jeux. RetroBat cherche l'IWAD d'après les cartes du mod (cartes ExMy : Doom ou Heretic ; MAPxx : Doom II), dans le dossier du mod puis dans les dossiers parents.

* **UZDoom, GZDoom** : si aucun IWAD n'est trouvé, l'émulateur affiche une fenêtre pour le choisir. Les mods qui indiquent eux-mêmes leur jeu (lump GAMEINFO) le choisissent seuls.
* **Core prboom** : il cherche l'IWAD dans le dossier du mod et ses dossiers parents (**ÉMULATION > CHERCHER L'IWAD DANS LES DOSSIERS PARENTS**, activé par défaut). Pour **SIGIL**, désactivez cette option.

### Charger plusieurs fichiers (.uzdoom, .gzdoom)

Pour lancer un jeu avec un ou plusieurs mods, créez un fichier texte avec l'extension `.uzdoom` (ou `.gzdoom`) dans `roms\doom`. Il apparaît dans la liste des jeux.

* Une seule ligne : le jeu à lancer, par exemple `doom2.wad`.
* Plusieurs lignes : les arguments de la ligne de commande d'UZDoom, **un par ligne**. Les chemins sont relatifs au dossier du fichier. Les lignes qui commencent par `#` sont ignorées.

```
-iwad
doom2.wad
-file
mods\brutalv22.pk3
-skill
3
```

Autre solution : un **dossier** nommé avec l'extension `.uzdoom` (par exemple `Brutal Doom.uzdoom`), contenant l'IWAD et les mods. RetroBat charge l'IWAD, puis les mods par ordre alphabétique.

Le core prboom lit aussi ces fichiers et dossiers : il ne garde que les fichiers (IWAD, WAD, PK3, patchs DeHackEd) et ignore les autres arguments.

<div align="left"><figure><img src="../../../.gitbook/assets/image (625).png" alt=""><figcaption></figcaption></figure></div>

### Options utiles

* **UZDoom, GZDoom** : **PILOTES > VIDÉO** (OpenGL, Vulkan, OpenGL ES), **RENDU VISUEL > MODE DE RENDU** (ACCÉLÉRATION MATÉRIELLE, LOGICIEL), **ÉMULATION > MODE DE COMPATIBILITÉ** (pour les anciens mods et démos), **RENDU VISUEL > FRAMERATE D'ORIGINE** (35 images par seconde), **CONTRÔLES > TOUJOURS COURIR** (activé par défaut), **CONTRÔLES > AFFICHER CIBLE**.
* **Core prboom** : **RÉSOLUTION INTERNE**, **ÉMULATION > NIVEAU DE COMPATIBILITÉ** (MBF21 pour les mods qui l'exigent), **RENDU VISUEL > PROFONDEUR DES COULEURS**, **ÉMULATION > IMPACTS DE BALLES SUR LES MURS**.

## Problèmes connus

<table><thead><tr><th width="352.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>UZDoom ou GZDoom affiche une fenêtre pour choisir le jeu</td><td>L'IWAD n'a pas été trouvé : placez le mod à côté de l'IWAD ou dans un sous-dossier, ou utilisez un fichier <code>.uzdoom</code>.</td></tr><tr><td>Un mod ne fonctionne pas avec le core prboom</td><td>Il est fait pour ZDoom : utilisez UZDoom.</td></tr><tr><td>SIGIL ne démarre pas avec le core prboom</td><td>Désactivez <strong>ÉMULATION > CHERCHER L'IWAD DANS LES DOSSIERS PARENTS</strong> pour ce jeu.</td></tr><tr><td>Un mod récent ne se comporte pas comme prévu avec le core prboom</td><td>Réglez <strong>ÉMULATION > NIVEAU DE COMPATIBILITÉ</strong> sur MBF21.</td></tr><tr><td>Un ancien mod ou une démo se déroule mal avec UZDoom</td><td>Essayez un autre <strong>ÉMULATION > MODE DE COMPATIBILITÉ</strong> (DOOM, BOOM, MBF).</td></tr></tbody></table>
