---
description: Nintendo
---

# Nintendo 3DS

<div align="left"><figure><img src="../../../../.gitbook/assets/image (618).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

La **Nintendo 3DS** est une console portable de Nintendo, sortie en 2011. Elle a deux écrans : celui du haut affiche la 3D sans lunettes, celui du bas est tactile et se joue au stylet. Elle a aussi un pad circulaire, un gyroscope et trois caméras. La **New 3DS** (2014) ajoute un petit stick (C-stick), les gâchettes ZL et ZR et un processeur plus rapide : quelques jeux ne fonctionnent que sur ce modèle (**Xenoblade Chronicles 3D**).

Parmi ses jeux : **Mario Kart 7**, **Super Mario 3D Land**, **The Legend of Zelda: A Link Between Worlds**, **Ocarina of Time 3D**, **Pokémon X / Y**, **Pokémon Soleil / Lune**, **Animal Crossing: New Leaf**, **Fire Emblem Awakening**, **Monster Hunter 4 Ultimate**, **Kid Icarus: Uprising**, **Luigi's Mansion 2**.

RetroBat propose plusieurs émulateurs : **Azahar** (par défaut), le core libretro **azahar**, **Azahar Plus**, **Mandarine**, **Citra** et **BizHawk** (core Encore).

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_3DS" %}

## En bref

<table><thead><tr><th width="275.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\3ds</code></td></tr><tr><td><strong>Extensions</strong></td><td>.3ds .3dsx .z3dsx .cia .zcia .elf .axf .cci .zcci .cxi .zcxi .app .m3u .zip .7z .squashfs .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>azahar</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Azahar, Azahar Plus, core azahar, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>aes_keys.txt</code>, <code>seeddb.bin</code> dans <code>bios</code> (BizHawk)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="158.25">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>azahar</strong> (défaut)</td><td>Suite officielle de Citra, la plus à jour. Résolution jusqu'à 18x, Vulkan ou OpenGL, formats compressés (.zcci, .zcia…), sauvegardes instantanées gérées par RetroBat, raccourcis manette alignés sur RetroBat.</td><td>Ne lit que les jeux déchiffrés.</td></tr><tr><td><strong>libretro: azahar</strong></td><td>Même émulation dans RetroArch : shaders, raccourcis RetroArch, écran tactile à la souris ou au stick droit.</td><td>Pas de lancement par <code>.m3u</code> (jeux installés).</td></tr><tr><td><strong>azahar-plus</strong></td><td>Version modifiée d'Azahar qui lit tous les fichiers acceptés par les anciennes versions de Citra.</td><td>Projet non officiel.</td></tr><tr><td><strong>mandarine</strong></td><td>Autre version dérivée de Citra (Mandarine Neo).</td><td>Pas de formats compressés d'Azahar. Sauvegardes instantanées non gérées par RetroBat.</td></tr><tr><td><strong>citra</strong></td><td>Citra d'origine.</td><td>N'évolue plus depuis 2024. Pas de formats compressés d'Azahar.</td></tr><tr><td><strong>bizhawk</strong> (Encore)</td><td>Outils de BizHawk (enregistrement, TAS), écran tactile au stick droit.</td><td>Pas de formats compressés d'Azahar.</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire.

BizHawk utilise aussi, s'ils sont présents dans `bios`, `aes_keys.txt` (clés de déchiffrement) et `seeddb.bin` (clés de certains jeux téléchargés).

## Quel format de jeu ?

<table><thead><tr><th width="221.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.cci</strong> / <strong>.3ds</strong></td><td>Copie d'une cartouche. Elle doit être déchiffrée. Si Azahar refuse un <code>.3ds</code>, renommez-le en <code>.cci</code> (même format) ou utilisez Azahar Plus.</td></tr><tr><td><strong>.cxi</strong></td><td>Application seule (contenu exécutable d'un jeu).</td></tr><tr><td><strong>.3dsx</strong> / <strong>.elf</strong> / <strong>.axf</strong></td><td>Homebrew.</td></tr><tr><td><strong>.cia</strong></td><td>Fichier d'installation : il s'installe dans la console émulée (voir <a href="nintendo-3ds.md#lancer-un-jeu-installe-.cia-eshop"><strong>Guides</strong></a>), il ne se lance pas directement.</td></tr><tr><td><strong>.zcci</strong> / <strong>.zcxi</strong> / <strong>.z3dsx</strong> / <strong>.zcia</strong></td><td>Formats compressés d'Azahar (menu <strong>Tools > Compress ROM File</strong> d'Azahar). Lus par Azahar, Azahar Plus et le core azahar.</td></tr><tr><td><strong>.app</strong> / <strong>.m3u</strong></td><td>Jeu installé dans la console émulée ; le <code>.m3u</code> contient le chemin du <code>.app</code> (voir <a href="nintendo-3ds.md#lancer-un-jeu-installe-.cia-eshop"><strong>Guides</strong></a>).</td></tr><tr><td><strong>.zip</strong> / <strong>.7z</strong> / <strong>.squashfs</strong></td><td>Archive contenant le jeu, décompressée au lancement.</td></tr><tr><td><strong>.decomp</strong></td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

Les jeux doivent être déchiffrés : copiés depuis votre console avec GodMode9, par exemple. Un jeu chiffré ne démarre pas avec Azahar.

## Contrôles

### Configuration automatique

Les boutons sont associés par position, comme sur la console :

<table><thead><tr><th width="269">Manette RetroBat</th><th>3DS</th></tr></thead><tbody><tr><td>EST / SUD / NORD / OUEST</td><td>A / B / X / Y</td></tr><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>Stick gauche</td><td>Pad circulaire</td></tr><tr><td>Stick droit</td><td>C-stick (New 3DS) ; pointeur de l'écran tactile avec le core azahar et BizHawk (voir plus bas)</td></tr><tr><td>L1 / R1</td><td>L / R</td></tr><tr><td>L2 / R2</td><td>ZL / ZR (New 3DS)</td></tr><tr><td>START / SELECT</td><td>START / SELECT</td></tr></tbody></table>

**CONTRÔLES > INVERSER LES BOUTONS A/B/X/Y** place les boutons d'après leur nom sur une manette Xbox (A sur SUD, B sur EST…).

| Standard                                           | Inversé                                            |
| -------------------------------------------------- | -------------------------------------------------- |
| ![](<../../../../.gitbook/assets/image (619).png>) | ![](<../../../../.gitbook/assets/image (620).png>) |

### Écran tactile

* **Azahar, Azahar Plus, Mandarine, Citra** : cliquez dans l'écran du bas avec la souris. Avec Azahar et Azahar Plus, **CONTRÔLES > PÉRIPHÉRIQUE TACTILE** permet aussi d'utiliser un appareil CemuHook. **CONTRÔLES > UTILISER LE PROFIL TACTILE** charge un profil « toucher par bouton » créé dans l'émulateur (un bouton de la manette touche un point de l'écran) : saisissez le nom exact du profil.
* **Core azahar** : souris (sauf avec **CONTRÔLES > DÉSACTIVER LA SOURIS**) ou pointeur au stick droit, selon **CONTRÔLES > FONCTION DU STICK DE DROITE** (C-STICK ET POINTEUR par défaut, POINTEUR, C-STICK). **L3** touche l'écran à l'endroit du pointeur. **CONTRÔLES > MASQUER LE POINTEUR DE L'ÉCRAN TACTILE** le cache quand il ne bouge pas.
* **BizHawk** : pointeur au stick droit, selon **CONTRÔLES > FONCTION DU STICK DE DROITE**.

Avec le core azahar et BizHawk, le tatouage affiché suit la fonction choisie pour le stick droit.

| Option                                                                  | Schéma de contrôles                                                                                                                                   |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Stick de droite comme pointeur d'écran tactile**                      | <img src="../../../../.gitbook/assets/image (46).png" alt="" data-size="original">                                                                    |
| **Stick de droite comme pointeur d'écran tactile (inversé)**            | <img src="../../../../.gitbook/assets/image (45).png" alt="" data-size="original">                                                                    |
| **Stick de droite comme C-stick et pointeur d'écran tactile**           | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick.png?raw=true" alt="" data-size="original">        |
| **Stick de droite comme C-stick et pointeur d'écran tactile (inversé)** | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick_revert.png?raw=true" alt="" data-size="original"> |

### Gyroscope

* **Azahar, Azahar Plus, Mandarine, Citra** : **CONTRÔLES > ACTIVER LE MOTION INPUT** : SOURIS (par défaut), CONTRÔLEUR (manette avec gyroscope : DualShock 4, DualSense, Switch Pro…) ou CEMUHOOK.
* **Core azahar** : **CONTRÔLES > ACTIVER LE MOTION CONTROL** (manette avec gyroscope).

### Raccourcis

Azahar et Azahar Plus utilisent les raccourcis de RetroBat :

| Action                            | Manette         | Clavier |
| --------------------------------- | --------------- | ------- |
| Quitter                           | HOTKEY + START  | `Échap` |
| Sauvegarde instantanée            | HOTKEY + OUEST  | `F2`    |
| Chargement                        | HOTKEY + NORD   | `F4`    |
| Capture d'écran                   | HOTKEY + R3     | `F8`    |
| Pause                             | HOTKEY + SUD    | `P`     |
| Avance rapide (maintenir)         | HOTKEY + Droite | —       |
| Inverser les écrans               | HOTKEY + L1     | —       |
| Changer la disposition des écrans | HOTKEY + R1     | —       |
| Plein écran                       | —               | `F1`    |

* **Mandarine** : HOTKEY + START (quitter), HOTKEY + SUD (pause), HOTKEY + R3 (capture), HOTKEY + L3 (plein écran).
* **Citra** : HOTKEY + START (quitter).
* **Core azahar**, **BizHawk** : raccourcis de RetroArch et de BizHawk.

Pour plus de détails, voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="337.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Azahar, Azahar Plus, core azahar : mémoire interne et carte SD</td><td><code>saves\3ds\azahar\nand</code>, <code>saves\3ds\azahar\sdmc</code> (communs aux trois)</td></tr><tr><td>Azahar : sauvegardes instantanées</td><td><code>saves\3ds\azahar\states</code> (Azahar Plus : <code>saves\3ds\azahar-plus\states</code>)</td></tr><tr><td>Core azahar : sauvegardes instantanées</td><td><code>saves\3ds\libretro.azahar</code></td></tr><tr><td>Mandarine</td><td><code>saves\3ds\mandarine\nand</code>, <code>saves\3ds\mandarine\sdmc</code></td></tr><tr><td>Citra</td><td><code>saves\3ds\Citra\nand</code>, <code>saves\3ds\Citra\sdmc</code></td></tr><tr><td>BizHawk</td><td><code>saves\3ds\bizhawk\user</code></td></tr><tr><td>Configuration (Azahar, Azahar Plus, Mandarine, Citra)</td><td><code>emulators\&#x3C;émulateur>\user\config\qt-config.ini</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots\azahar</code> (Azahar, Azahar Plus), <code>screenshots\mandarine</code>, <code>screenshots\citra</code></td></tr></tbody></table>

## Guides

### Lancer un jeu installé (.cia, eShop)

Un `.cia` s'installe dans la mémoire de la console émulée, puis le jeu installé se lance avec un fichier `.m3u` (Azahar, Azahar Plus, Mandarine, Citra).

1. Lancez l'émulateur depuis le dossier `emulators`, menu **File > Install CIA**, et choisissez le `.cia`.
2. Faites un clic droit sur le jeu installé, **Create Shortcut > Add to Desktop**.
3. Copiez le chemin du `.app` indiqué dans le raccourci (dernière partie de la cible, sans les guillemets) dans un fichier texte.
4. Enregistrez ce fichier avec l'extension `.m3u` dans `roms\3ds`, puis mettez à jour la liste des jeux.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (621).png" alt="" width="428"><figcaption></figcaption></figure></div>

### Textures personnalisées

1. Placez le pack de textures dans `emulators\<émulateur>\user\load\textures\<ID du jeu>` (core azahar : `saves\3ds\azahar\load\textures\<ID du jeu>`). L'ID du jeu s'obtient dans l'émulateur : clic droit sur le jeu, **Open Custom Texture Location**.
2. Activez **RENDU VISUEL > TEXTURES PERSONNALISÉES**, et si besoin **RENDU VISUEL > METTRE EN CACHE LES TEXTURES PERSONNALISÉES** (Azahar, Mandarine, Citra : charge tout le pack au démarrage).

### Disposition des écrans

**VIDÉO > POSITIONNEMENT DES ÉCRANS** choisit la disposition : HAUT-BAS (par défaut), UNIQUEMENT L'ÉCRAN PRINCIPAL, LARGE / PETIT, COTE À COTE, FENÊTRES SÉPARÉES et HYBRIDE (Azahar, Mandarine, Citra). **VIDÉO > INVERSER LES ÉCRANS** met l'écran du bas en avant.

Avec les décorations par défaut de RetroBat, Azahar place les deux écrans dans la décoration : la disposition choisie est alors ignorée.

### Région et langue

**ÉMULATION > RÉGION** force la région de la console (automatique par défaut, d'après le jeu). **ÉMULATION > LANGUE** change la langue de la console, utilisée par les jeux qui la proposent ; par défaut, celle de RetroBat.

## Problèmes connus

<table><thead><tr><th width="345.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Azahar affiche une erreur au lancement (jeu chiffré ou non pris en charge)</td><td>Le jeu doit être déchiffré. Essayez de renommer le <code>.3ds</code> en <code>.cci</code>, ou utilisez Azahar Plus.</td></tr><tr><td>Un <code>.cia</code> ne démarre pas</td><td>Installez-le d'abord dans l'émulateur (voir <a href="nintendo-3ds.md#lancer-un-jeu-installe-.cia-eshop"><strong>Guides</strong></a>).</td></tr><tr><td>Un jeu demande une New 3DS</td><td>Avec le core azahar, réglez <strong>ÉMULATION > MODÈLE DE CONSOLE</strong> sur NEW 3DS (valeur par défaut).</td></tr><tr><td>Le jeu saccade la première fois qu'un effet s'affiche</td><td>Laissez <strong>VIDÉO > COMPILATION DES SHADERS ASYNCHRONE</strong> activée (par défaut avec Azahar).</td></tr><tr><td>Une sauvegarde instantanée d'Azahar lancée depuis RetroBat ne se charge pas</td><td>Azahar ne charge pas de sauvegarde au lancement : RetroBat envoie la touche de chargement (<code>F4</code>) une fois le jeu démarré. Ne touchez pas au clavier pendant ce temps, ou chargez-la avec HOTKEY + NORD.</td></tr></tbody></table>
