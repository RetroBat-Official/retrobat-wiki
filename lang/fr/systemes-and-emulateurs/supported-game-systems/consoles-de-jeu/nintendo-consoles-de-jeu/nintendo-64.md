---
description: Nintendo
---

# Nintendo 64

<div align="left"><figure><img src="../../../../.gitbook/assets/image (673).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **Nintendo 64** est la console de salon 64 bits de Nintendo, sortie au Japon en juin 1996, en Amérique du Nord en septembre 1996 et en Europe en mars 1997. Elle reste sur cartouches et introduit une manette à stick analogique, quatre ports manette, le Rumble Pak (vibrations) et l'Expansion Pak (mémoire supplémentaire).

Sa ludothèque compte Super Mario 64, The Legend of Zelda: Ocarina of Time et Majora's Mask, Mario Kart 64, GoldenEye 007, Perfect Dark, Banjo-Kazooie, Donkey Kong 64, Super Smash Bros., Pokémon Stadium, F-Zero X…

Les jeux du lecteur de disques **64DD** (Japon uniquement) ont leur propre système dans RetroBat, [**Nintendo 64 Disk Drive**](nintendo-64-disk-drive.md) (`roms\n64dd`).

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_64" %}

## En bref

<table><thead><tr><th width="282.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\n64</code></td></tr><tr><td><strong>Extensions</strong></td><td>.v64 .z64 .n64 .zip .7z .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: mupen64plus_next</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, RMG, Gopher64, BizHawk ; Project64 et ares par raccourcis ; Simple64 par son menu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, Gopher64, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                                | Pour qui ?                               | Points forts                                                                                                                               | Limites                                                            |
| ---------------------------------------- | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------ |
| **libretro: mupen64plus\_next** (défaut) | Tout le monde                            | Très compatible, trois moteurs graphiques (GLideN64, ParaLLEl-RDP, Angrylion), textures HD, écran large, RetroAchievements, jeu en réseau. | —                                                                  |
| **libretro: parallel\_n64**              | Utilisateurs de cartes graphiques Vulkan | Rendu ParaLLEl-RDP précis par défaut, Transfer Pak simple à utiliser, RetroAchievements, jeu en réseau.                                    | Vulkan conseillé.                                                  |
| **mupen64** (RMG)                        | Utilisateurs de Mupen64Plus              | Rosalie's Mupen GUI : GLideN64, ParaLLEl ou Angrylion, textures HD, Transfer Pak, adaptateurs Raphnet et GameCube.                         | Pas de RetroAchievements.                                          |
| **gopher64**                             | Curieux                                  | Émulateur récent et précis, RetroAchievements, VRU (Hey You, Pikachu!).                                                                    | —                                                                  |
| **simple64**                             | Utilisateurs de Simple64                 | Rendu ParaLLEl précis, adaptateur Raphnet.                                                                                                 | Pas de RetroAchievements. Seul le raccourci Quitter est configuré. |
| **ares**                                 | Puristes                                 | Émulation très précise.                                                                                                                    | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis. |
| **bizhawk: Ares64**, **Mupen64Plus**     | Utilisateurs de BizHawk                  | Deux émulations au choix, RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.                                            | —                                                                  |
| **project64**                            | Utilisateurs de Project64                | Émulateur historique de Windows, textures HD, adaptateur Raphnet.                                                                          | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis. |

**En cas de doute, gardez libretro: mupen64plus\_next.**

## BIOS

La Nintendo 64 n'a pas de BIOS : aucun fichier n'est nécessaire.

## Quel format de jeu ?

<table><thead><tr><th width="197.75">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.z64</strong></td><td>Image d'une cartouche, dans l'ordre d'origine des octets.</td></tr><tr><td><strong>.v64</strong>, <strong>.n64</strong></td><td>Même contenu, avec les octets dans un autre ordre (copieurs de l'époque) : les émulateurs les lisent aussi.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive).</td></tr><tr><td><strong>.decomp</strong></td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

## Contrôles

RetroBat configure automatiquement les manettes pour tous les émulateurs, jusqu'à quatre joueurs. Disposition par défaut :

<table><thead><tr><th width="284">Manette RetroBat</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Stick</td></tr><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>SUD</td><td>A</td></tr><tr><td>OUEST</td><td>B</td></tr><tr><td>L2</td><td>Z</td></tr><tr><td>L1 / R1</td><td>L / R</td></tr><tr><td>Stick droit</td><td>Boutons C</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

Avec une manette sans gâchettes (L2 / R2), Z passe sur L1 (cores libretro).

Chaque émulateur propose plusieurs dispositions :

| Émulateurs                         | Option                                                 | Dispositions                                                                                                                                                                                |
| ---------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| cores libretro                     | **CONTRÔLES > DISPOSITION DES BOUTONS**                | **STANDARD** (défaut), **XBOX**                                                                                                                                                             |
| ares, BizHawk                      | **CONTRÔLES > DISPOSITION DES BOUTONS**                | **Z=GÂCHETTE GAUCHE** (défaut), **Z=GÂCHETTE DROITE**, **XBOX**                                                                                                                             |
| RMG, Project64, Simple64, Gopher64 | **CONTRÔLES > DISPOSITION DES BOUTONS JOUEUR 1** (à 4) | **BOUTONS C=STICK DROIT Z=GÂCHETTE GAUCHE** (défaut), **BOUTONS C=FAÇADE Z=GÂCHETTE GAUCHE**, **BOUTONS C=STICK DROIT Z=GÂCHETTE DROITE**, **BOUTONS C=FAÇADE Z=GÂCHETTE DROITE**, **XBOX** |

| Disposition                                                         | Schéma                                                                                                                                              |
| ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Cores libretro, **STANDARD**                                        | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64.png?raw=true" alt="" data-size="original">                    |
| Autres émulateurs, disposition par défaut                           | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" data-size="original">         |
| **Z=GÂCHETTE DROITE** / **BOUTONS C=STICK DROIT Z=GÂCHETTE DROITE** | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_zr.png?raw=true" alt="" data-size="original">      |
| **BOUTONS C=FAÇADE Z=GÂCHETTE GAUCHE**                              | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_face_zl.png?raw=true" alt="" data-size="original"> |
| **BOUTONS C=FAÇADE Z=GÂCHETTE DROITE**                              | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_face_zr.png?raw=true" alt="" data-size="original"> |
| **XBOX** (tous les émulateurs)                                      | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64_xbox.png?raw=true" alt="" data-size="original">               |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (675).png" alt=""><figcaption></figcaption></figure></div>

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

ares, BizHawk et Project64 utilisent les raccourcis de RetroBat :

| Action                          | Manette             | Clavier          |
| ------------------------------- | ------------------- | ---------------- |
| Quitter                         | HOTKEY + START      | `Échap`          |
| Pause                           | HOTKEY + SUD        | `P`              |
| Sauvegarde instantanée          | HOTKEY + OUEST      | `F2`             |
| Chargement                      | HOTKEY + NORD       | `F4`             |
| Emplacement précédent / suivant | HOTKEY + Bas / Haut | `F6` / `F7`      |
| Rembobiner (si activé)          | HOTKEY + Gauche     | `Retour arrière` |
| Avance rapide (maintenir)       | HOTKEY + Droite     | `L`              |
| Capture d'écran                 | HOTKEY + R3         | `F8`             |
| Plein écran                     | HOTKEY + L3         | `F`              |

Project64 n'a pas de raccourci pour changer d'emplacement.

RMG (mupen64) a ses propres raccourcis, sur le bouton SELECT :

| Action                          | Manette                       | Clavier |
| ------------------------------- | ----------------------------- | ------- |
| Quitter                         | SELECT + START                | `Échap` |
| Pause                           | SELECT + SUD                  | `P`     |
| Sauvegarde instantanée          | SELECT + OUEST                | `F2`    |
| Chargement                      | SELECT + NORD                 | `F4`    |
| Emplacement précédent / suivant | SELECT + Bas / Haut           |         |
| Vitesse 50 % / 100 % / 250 %    | SELECT + Gauche / L1 / Droite |         |
| Capture d'écran                 | SELECT + R3                   | `F8`    |
| Plein écran                     | SELECT + L3                   |         |

Gopher64 :

| Action                               | Manette         | Clavier               |
| ------------------------------------ | --------------- | --------------------- |
| Quitter                              | HOTKEY + START  | `Échap` (plein écran) |
| Pause                                | HOTKEY + SUD    | `Alt` + `P`           |
| Sauvegarde instantanée               | HOTKEY + OUEST  | `F5`                  |
| Chargement                           | HOTKEY + NORD   | `F7`                  |
| Rembobiner (si activé)               | HOTKEY + Gauche | `F6`                  |
| Avance rapide (activer / désactiver) | HOTKEY + Droite | `Alt` + `F`           |

Avec Simple64, seul HOTKEY + START (quitter) est configuré : les sauvegardes instantanées se font depuis son menu.

## Dossiers

<table><thead><tr><th width="306.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Cores libretro : sauvegardes des jeux</td><td><code>saves\n64</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><p><code>saves\n64\libretro.&#x3C;core></code> </p><p>(ex. <code>saves\n64\libretro.mupen64plus_next</code>)</p></td></tr><tr><td>RMG, Simple64 : sauvegardes des jeux</td><td><code>saves\n64\sram</code></td></tr><tr><td>RMG : sauvegardes instantanées</td><td><code>saves\n64\mupen64</code></td></tr><tr><td>Simple64 : sauvegardes instantanées</td><td><code>saves\n64\state</code></td></tr><tr><td>Gopher64 : sauvegardes des jeux et instantanées</td><td><code>saves\n64\gopher64</code></td></tr><tr><td>Project64 : sauvegardes des jeux et instantanées</td><td><p><code>saves\n64\project64</code></p><p><code>saves\n64\project64\sstates</code></p></td></tr><tr><td>ares : sauvegardes des jeux et instantanées</td><td><code>saves\n64\ares</code></td></tr><tr><td>BizHawk : sauvegardes des jeux</td><td><code>saves\n64\bizhawk</code></td></tr><tr><td>Textures HD</td><td><p><code>bios\Mupen64plus\hires_texture</code> et <code>bios\Mupen64plus\cache</code> (core mupen64plus_next, RMG)</p><p><code>saves\n64\project64\hires_texture</code> (Project64)</p></td></tr><tr><td>Manettes N64 reconnues</td><td><code>system\resources\inputmapping\n64Controllers.json</code></td></tr><tr><td>Captures d'écran</td><td><p><code>screenshots\mupen64</code></p><p><code>screenshots\Simple64</code></p><p><code>screenshots\project64</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\n64</code></p></td></tr></tbody></table>

## Guides

### Utiliser une manette N64

RetroBat reconnaît ces manettes et leur applique une disposition adaptée (cores libretro, RMG, Simple64, ares, BizHawk) :

* manette N64 Nintendo Switch Online ;
* manette 8BitDo N64 ;
* manette d'origine avec l'adaptateur Mayflash ou Raphnet ;
* manettes USB de style N64 reconnues comme « SWITCH CO.LTD. Usb Controller ».

Si la disposition n'est pas appliquée, activez **CONTRÔLES > UTILISER UNE MANETTE DE TYPE N64**. Pour une manette à deux gâchettes, **CONTRÔLEURS SPÉCIAUX > INVERSER LA GÂCHETTE Z (N64)** place Z sur la gâchette droite.

{% hint style="info" %}
Avec l'adaptateur Mayflash, branchez les manettes de droite à gauche : la manette 1 est celle du port 4 (ou du port 2 sur un adaptateur deux manettes).
{% endhint %}

Une autre manette peut être ajoutée dans `n64Controllers.json`.

**Adaptateur Raphnet en accès direct** (la manette d'origine est lue sans conversion) :

<table><thead><tr><th width="244">Émulateur</th><th>Option</th></tr></thead><tbody><tr><td>RMG</td><td><strong>PILOTES > MANETTES > ADAPTATEUR RAPHNET</strong></td></tr><tr><td>Simple64</td><td><strong>PILOTES > MANETTES > ADAPTATEUR RAPHNET</strong></td></tr><tr><td>Project64</td><td><strong>PILOTES > UTILISER L'ADAPTATEUR RAPHNET</strong></td></tr></tbody></table>

RMG accepte aussi l'adaptateur GameCube officiel : **PILOTES > MANETTES > ADAPTATEUR GAMECUBE**.

### Extensions de la manette (Controller Pak, Rumble Pak, Transfer Pak)

La manette N64 accueille une extension : carte mémoire (Controller Pak), vibrations (Rumble Pak) ou Transfer Pak, qui lit une cartouche Game Boy (Pokémon Stadium 1 et 2, Mario Golf, Mario Tennis, Perfect Dark). Choisissez-la par joueur :

<table><thead><tr><th width="213.25">Émulateur</th><th>Option</th><th>Choix</th></tr></thead><tbody><tr><td>core mupen64plus_next</td><td><strong>ÉMULATION > EXTENSION MANETTE 1</strong> (à 4)</td><td><strong>MÉMOIRE</strong> (défaut joueur 1), <strong>VIBRATION</strong>, <strong>TRANSFER</strong></td></tr><tr><td>core parallel_n64</td><td><strong>CONTRÔLES > EXTENSION MANETTE 1</strong> (à 4)</td><td><strong>MÉMOIRE</strong>, <strong>RUMBLE PAK</strong>, <strong>TRANSFER</strong>, <strong>CAPTEUR BIO</strong> (joueur 1)</td></tr><tr><td>RMG</td><td><strong>CONTRÔLES > EXTENSION MANETTE 1</strong> (à 4)</td><td><strong>MEMORY PAK</strong>, <strong>RUMBLE PAK</strong>, <strong>TRANSFER PAK</strong> (joueur 1)</td></tr><tr><td>Simple64</td><td><strong>CONTRÔLES > EXTENSION MANETTE 1</strong> (à 4)</td><td><strong>MÉMOIRE</strong> (défaut), <strong>RUMBLE PAK</strong>, <strong>TRANSFER PAK</strong></td></tr><tr><td>BizHawk</td><td><strong>CONTRÔLES > EXTENSION MANETTE 1</strong> (à 4)</td><td><strong>MÉMOIRE</strong>, <strong>RUMBLE PAK</strong></td></tr></tbody></table>

**Transfer Pak :**

* **core parallel\_n64** : placez la cartouche Game Boy (`.gb` ou `.gbc`) et sa sauvegarde (`.sav`) à côté du jeu N64, sous le même nom.
* **RMG** : choisissez **TRANSFER PAK** pour le joueur 1, puis **SYSTÈME POUR TRANSFER PACK** (GB ou GBC). Dans **ROM POUR TRANSFER PACK** et **SAUVEGARDE POUR TRANSFER PACK**, tapez le début du nom de la cartouche (cherchée dans `roms\gb` ou `roms\gbc`) et de sa sauvegarde (cherchée dans `saves\gb` ou `saves\gbc`).

### Expansion Pak

L'Expansion Pak double la mémoire de la console. Donkey Kong 64 et The Legend of Zelda: Majora's Mask l'exigent, d'autres jeux l'utilisent pour une meilleure image. Il est actif par défaut. Ne le désactivez que si un jeu le demande : **ÉMULATION > DÉSACTIVER L'EXPANSION PAK** (Gopher64), **DÉSACTIVER L'EXTENSION RAM 4MB** (Simple64), **ACTIVER L'EXTENSION RAM 4MB** (ares).

### Moteur graphique et résolution

| Émulateur                | Option                                                                                     | Effet                                                                                                                                                                       |
| ------------------------ | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| core mupen64plus\_next   | **ÉMULATION > PLUGIN GRAPHIQUE**                                                           | **GLIDEN64 (HLE)** : rapide, améliorations (résolution, textures HD) ; **PARALLEL-RDP (LLE)** : précis, demande Vulkan ; **ANGRYLION (LOGICIEL)** : très précis, très lent. |
| core mupen64plus\_next   | **PLUGIN GLIDE > RÉSOLUTION INTERNE**, **PLUGIN PARALLEL > RÉSOLUTION INTERNE (PARALLEL)** | Résolution de rendu de chaque moteur.                                                                                                                                       |
| core parallel\_n64       | **VIDÉO > PLUGIN GRAPHIQUE**                                                               | ParaLLEl-RDP par défaut (Vulkan) ; GLideN64, Angrylion, Glide64, glN64, Rice.                                                                                               |
| RMG                      | **PILOTES > PLUGIN GRAPHIQUE** et **RÉSOLUTION INTERNE**                                   | GLideN64, ParaLLEl ou Angrylion.                                                                                                                                            |
| Gopher64, Simple64, ares | **RÉSOLUTION INTERNE** / **VIDÉO > QUALITÉ**                                               | Résolution de rendu.                                                                                                                                                        |

### Écran large

Certains jeux s'affichent en 16:9 grâce à un hack (images déformées dans les jeux en 2D) :

<table><thead><tr><th width="250.25">Émulateur</th><th>Option</th></tr></thead><tbody><tr><td>core mupen64plus_next</td><td><strong>RENDU VISUEL > HACK ÉCRAN LARGE</strong> (<strong>AJUSTÉ (16:9)</strong> ou <strong>ÉTIRÉ (16:9)</strong>)</td></tr><tr><td>core parallel_n64</td><td><strong>VIDÉO > HACK ÉCRAN LARGE</strong></td></tr><tr><td>RMG</td><td><strong>RAPPORT D'ASPECT > 16:9</strong></td></tr><tr><td>Gopher64, Simple64</td><td><strong>VIDÉO > ÉTIRER POUR REMPLIR L'ÉCRAN</strong></td></tr></tbody></table>

Les bezels sont désactivés avec ces réglages (core mupen64plus\_next, RMG).

### Textures HD

Les packs de textures remplacent les textures d'origine.

| Émulateur              | Dossier                                                                                                 | Option                                                                                                          |
| ---------------------- | ------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| core mupen64plus\_next | `bios\Mupen64plus\cache` (packs `.htc` / `.hts`), `bios\Mupen64plus\hires_texture` (dossiers de `.png`) | **RENDU VISUEL > TEXTURES PERSONNALISÉES** : **RICE** pour `.htc` / `.hts`, **CACHE** pour un dossier de `.png` |
| RMG                    | `bios\Mupen64plus\hires_texture`                                                                        | **RENDU VISUEL > TEXTURES PERSONNALISÉES**                                                                      |
| Project64              | `saves\n64\project64\hires_texture`                                                                     | **RENDU VISUEL > TEXTURES PERSONNALISÉES**                                                                      |

Le pack porte le nom interne du jeu : par exemple `MARIOKART64_HIRESTEXTURES.htc`, ou un dossier `MARIOKART64`. Avec mupen64plus\_next, un pack en dossier est converti en `.hts` dans `cache` au premier lancement : choisissez ensuite **RICE**, le jeu démarre plus vite.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (674).png" alt=""><figcaption></figcaption></figure></div>

### Autres options utiles

| Émulateur                   | Option                                 | Effet                                                      |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- |
| core mupen64plus\_next      | **ÉMULATION > MODE PERFORMANCE**       | Plus rapide, mais moins précis et avec plus de latence.    |
| core mupen64plus\_next, RMG | **RENDU VISUEL > ROGNER LES BORDURES** | Masque les bandes noires autour de l'image (selon le jeu). |
| Gopher64                    | **CONTRÔLES > ÉMULER LE VRU**          | Micro de Hey You, Pikachu! et Densha de GO! 64.            |
| Gopher64                    | **ÉMULATION > OVERCLOCK DU CPU**       | Plus fluide dans les jeux qui ralentissent.                |

## Problèmes connus

| Problème                                       | Solution                                                                                                                                                                     |
| ---------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Écran noir ou plantage avec ParaLLEl-RDP       | Ce moteur demande une carte graphique compatible Vulkan : choisissez GLideN64.                                                                                               |
| Donkey Kong 64 ou Majora's Mask ne démarre pas | Vérifiez que l'Expansion Pak n'est pas désactivé.                                                                                                                            |
| Pas de vibrations                              | Choisissez le Rumble Pak dans **EXTENSION MANETTE 1** (voir [**Extensions de la manette**](nintendo-64.md#extensions-de-la-manette-controller-pak-rumble-pak-transfer-pak)). |
| La manette N64 n'a pas la bonne disposition    | Voir [**Utiliser une manette N64**](nintendo-64.md#utiliser-une-manette-n64).                                                                                                |
| Un jeu `.ndd` n'apparaît pas                   | Les jeux 64DD se rangent dans `roms\n64dd`.                                                                                                                                  |
