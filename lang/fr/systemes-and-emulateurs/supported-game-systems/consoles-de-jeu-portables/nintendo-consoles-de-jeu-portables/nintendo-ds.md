---
description: Nintendo
---

# Nintendo DS

<div align="left"><figure><img src="../../../../.gitbook/assets/image (2).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

La **Nintendo DS** est une console portable de Nintendo, sortie en 2004. Elle a deux écrans : celui du bas est tactile et se joue au stylet. Elle a aussi un microphone et une liaison sans fil (jeu à plusieurs, Téléchargement DS, Nintendo Wi-Fi Connection). Suivent la **DS Lite** (2006) et la **DSi** (2008), qui ajoute des caméras, une boutique en ligne (**DSiWare**) et quelques jeux qui ne fonctionnent que sur ce modèle.

Parmi ses jeux : **New Super Mario Bros.**, **Mario Kart DS**, **Pokémon Diamant / Perle**, **Pokémon Or HeartGold / Argent SoulSilver**, **Pokémon Noir / Blanc**, **The Legend of Zelda: Phantom Hourglass**, **Professeur Layton**, **Phoenix Wright: Ace Attorney**, **Animal Crossing: Wild World**, **Nintendogs**, **Chrono Trigger**, **Dragon Quest IX**.

RetroBat propose plusieurs émulateurs : le core libretro **melondsds** (par défaut), les cores **desmume**, **desmume2015**, **melonds** et **noods**, **melonDS**, **DeSmuME** et **BizHawk** (core melonDS).

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_DS" %}

## En bref

<table><thead><tr><th width="245.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\nds</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nds .bin .zip .7z .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: melondsds</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun obligatoire (DSi : voir plus bas)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, DeSmuME, BizHawk ; melonDS par raccourcis (non gérées par RetroBat)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores desmume, desmume2015</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>bios7.bin</code>, <code>bios9.bin</code>, <code>firmware.bin</code> (DS) ; <code>dsi_bios7.bin</code>, <code>dsi_bios9.bin</code>, <code>dsi_firmware.bin</code>, <code>dsi_nand.bin</code> (DSi), dans <code>bios</code></td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                        | Points forts                                                                                                                                                                                                                       | Limites                                                                      |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| **libretro: melondsds** (défaut) | Suit l'émulateur melonDS au plus près. Résolution augmentée (OpenGL), deux dispositions d'écrans à alterner en jeu, DSi automatique pour les jeux qui l'exigent, DSiWare, micro réel, sauvegardes instantanées, RetroAchievements. | Ne lance pas un fichier NAND `.bin`.                                         |
| **libretro: desmume**            | Jeu en réseau, sauvegardes instantanées, RetroAchievements, résolution augmentée.                                                                                                                                                  | Émulation moins précise que melonDS. Pas de mode DSi.                        |
| **libretro: desmume2015**        | Ancienne version de DeSmuME, plus légère, pour les PC modestes.                                                                                                                                                                    | Peu d'options. Pas de mode DSi.                                              |
| **libretro: melonds**            | Ancien core melonDS.                                                                                                                                                                                                               | N'évolue plus, remplacé par melondsds. Pas de fichier NAND `.bin`.           |
| **libretro: noods**              | Émulateur récent et léger.                                                                                                                                                                                                         | Pas de fichier NAND `.bin`.                                                  |
| **melonds**                      | Dernière version de melonDS. Lance un fichier NAND `.bin` et gère les titres installés dans la NAND.                                                                                                                               | Sauvegardes instantanées non gérées par RetroBat. Écran tactile à la souris. |
| **desmume**                      | Sauvegardes instantanées gérées par RetroBat, filtres d'image.                                                                                                                                                                     | Écran tactile à la souris. Pas de mode DSi.                                  |
| **bizhawk** (melonDS)            | Outils de BizHawk (enregistrement, TAS), stylet au stick droit ou à la souris, RetroAchievements.                                                                                                                                  | Plus lourd que les autres.                                                   |

## BIOS

Aucun BIOS n'est nécessaire pour les jeux DS : les émulateurs ont un BIOS intégré. Les fichiers de la console restent utiles pour démarrer sur le menu de la DS (**ÉMULATION > DÉMARRER DANS LE BIOS**) et pour le **Téléchargement DS**.

**DS** :

| Fichier        | Dossier |
| -------------- | ------- |
| `bios7.bin`    | `bios`  |
| `bios9.bin`    | `bios`  |
| `firmware.bin` | `bios`  |

* **Core melondsds** : les fichiers sont utilisés s'ils sont présents ; **ÉMULATION > UTILISER LE BIOS INTERNE** force le BIOS intégré.
* **melonDS, core desmume, DeSmuME, BizHawk** : activez **ÉMULATION > UTILISER LE BIOS EXTERNE** (DeSmuME : aussi **ÉMULATION > UTILISER LE FIRMWARE EXTERNE**).

**DSi** (jeux DSi, DSiWare, menu de la DSi) :

<table><thead><tr><th width="225.25">Fichier</th><th>Dossier</th></tr></thead><tbody><tr><td><code>dsi_bios7.bin</code></td><td><code>bios</code></td></tr><tr><td><code>dsi_bios9.bin</code></td><td><code>bios</code></td></tr><tr><td><code>dsi_firmware.bin</code></td><td><code>bios</code></td></tr><tr><td><code>dsi_nand.bin</code></td><td><code>bios</code></td></tr></tbody></table>

Plusieurs NAND peuvent cohabiter : ajoutez la région au nom du fichier (`dsi_nand_EUR.bin`, `dsi_nand_USA.bin`, `dsi_nand_JPN.bin`, `KOR`, `AUS`, `CHN`), puis choisissez-la avec **ÉMULATION > RÉGION DE LA NAND DSI** (core melondsds, melonDS). Avec le core melondsds, AUTO choisit la NAND d'après la région du jeu.

## Quel format de jeu ?

<table><thead><tr><th width="171.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.nds</strong></td><td>Copie d'une cartouche DS ou DSi, ou d'un DSiWare.</td></tr><tr><td><strong>.bin</strong></td><td>Fichier NAND d'une DSi : lance le menu de la console et ses titres installés (voir <a href="nintendo-ds.md#lancer-le-menu-dune-nand-dsi-.bin"><strong>Guides</strong></a>). Seulement avec melonDS et BizHawk.</td></tr><tr><td><strong>.zip</strong> / <strong>.7z</strong></td><td>Archive contenant un <code>.nds</code>.</td></tr><tr><td><strong>.decomp</strong></td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

## Contrôles

### Configuration automatique

Les boutons sont associés par position, comme sur la console :

| Manette RetroBat         | DS                   |
| ------------------------ | -------------------- |
| EST / SUD / NORD / OUEST | A / B / X / Y        |
| Croix directionnelle     | Croix directionnelle |
| L1 / R1                  | L / R                |
| START / SELECT           | START / SELECT       |

Les fonctions propres à la DS (stylet, micro, couvercle, écrans) changent selon l'émulateur :

| Émulateur                      | Stylet                                   | Micro | Couvercle | Écrans                    |
| ------------------------------ | ---------------------------------------- | ----- | --------- | ------------------------- |
| **Core melondsds**             | Stick droit, R3 pour toucher             | L2    | L3        | R2 : disposition suivante |
| **Core melonds**               | Stick droit, R3 pour toucher             | L2    | L3        | R2 : inverser             |
| **Cores desmume, desmume2015** | Stick droit, R2 pour toucher             | L3    | L2        | R3 : inverser             |
| **Core noods**                 | Stick droit, R3 pour toucher             | L2    | —         | R2 : inverser             |
| **melonDS**                    | Souris                                   | L2    | L3        | R2 : inverser             |
| **DeSmuME**                    | Souris                                   | —     | —         | —                         |
| **BizHawk**                    | Stick droit, R2 pour toucher (ou souris) | L2    | —         | —                         |

| Émulateur                  | Tatouage                                                                                                                                               |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Core melondsds             | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melondsds.png?raw=true" alt="" data-size="original">             |
| Cores desmume, desmume2015 | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds.png?raw=true" alt="" data-size="original">                       |
| Core melonds               | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds.png?raw=true" alt="" data-size="original">               |
| Core noods                 | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_noods.png?raw=true" alt="" data-size="original">                 |
| melonDS                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds_standalone.png?raw=true" alt="" data-size="original">    |
| melonDS (stick gauche)     | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds_standalone_ls.png?raw=true" alt="" data-size="original"> |
| BizHawk                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_bizhawk.png?raw=true" alt="" data-size="original">               |
| BizHawk (souris)           | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_bizhawk_mouse.png?raw=true" alt="" data-size="original">         |

### Options de contrôle

* **Core melondsds** : **CONTRÔLES > ÉMULATION DE L'ÉCRAN TACTILE** (POINTEUR : souris ; JOYSTICK : stick droit), **CONTRÔLES > MODE D'AFFICHAGE DU CURSEUR**, **CONTRÔLES > ÉMULATION DU MICROPHONE** (micro réel, souffle, bruit, silence) et **CONTRÔLES > MODE DU BOUTON MICROPHONE**.
* **Core melonds** : **CONTRÔLES > ÉMULATION DE L'ÉCRAN TACTILE** (JOYSTICK par défaut) et **CONTRÔLES > ÉMULATION DU MICROPHONE**.
* **Cores desmume, desmume2015** : **CONTRÔLES > ÉMULER LE STYLET AVEC LE STICK DROIT** (activé par défaut).
* **Core noods** : **CONTRÔLES > ÉMULATION DE L'ÉCRAN TACTILE**, **CONTRÔLES > AFFICHER LE POINTEUR**, **CONTRÔLES > MODE DU BOUTON D'INVERSION DES ÉCRANS**.
* **melonDS** : **CONTRÔLES > UTILISER LE STICK ANALOGIQUE** (stick gauche à la place de la croix), **CONTRÔLES > DISPOSITION XBOX** (boutons d'après leur nom sur une manette Xbox), **CONTRÔLES > ÉMULATION DU MICROPHONE**.
* **DeSmuME** : **CONTRÔLES > UTILISER LE STICK ANALOGIQUE**, **CONTRÔLES > INVERSER LES BOUTONS A/B/X/Y**.
* **BizHawk** : **CONTRÔLES > UTILISER LA SOURIS** (stylet à la souris au lieu du stick droit).

### Raccourcis

melonDS, DeSmuME et BizHawk utilisent les raccourcis de RetroBat (par PadToKey) :

| Action                                   | Manette             | melonDS       | DeSmuME, BizHawk |
| ---------------------------------------- | ------------------- | ------------- | ---------------- |
| Quitter                                  | HOTKEY + START      | oui           | oui              |
| Pause                                    | HOTKEY + SUD        | oui           | oui              |
| Sauvegarde instantanée                   | HOTKEY + OUEST      | emplacement 1 | oui              |
| Chargement                               | HOTKEY + NORD       | emplacement 1 | oui              |
| Emplacement précédent / suivant          | HOTKEY + Bas / Haut | —             | oui              |
| Ralenti (melonDS) / rembobiner (BizHawk) | HOTKEY + Gauche     | oui           | BizHawk          |
| Avance rapide (maintenir)                | HOTKEY + Droite     | oui           | oui              |
| Capture d'écran                          | HOTKEY + R3         | —             | oui              |
| Plein écran                              | HOTKEY + L3         | oui           | BizHawk          |

Les cores libretro utilisent les raccourcis de RetroArch.

Pour plus de détails, voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="317.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Cores libretro, melonDS : sauvegardes</td><td><code>saves\nds</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><code>saves\nds\libretro.&#x3C;core></code></td></tr><tr><td>melonDS : sauvegardes instantanées</td><td><code>saves\nds\melonds\sstates</code></td></tr><tr><td>DeSmuME : sauvegardes</td><td><code>saves\nds\DeSmuME</code> (sauvegardes instantanées : <code>saves\nds\DeSmuME\stateslots</code>)</td></tr><tr><td>BizHawk : sauvegardes</td><td><code>saves\nds\bizhawk</code> (sauvegardes instantanées : <code>saves\nds\bizhawk\sstates\melonDS</code>)</td></tr><tr><td>Codes de triche</td><td><code>cheats\melonds</code> (melonDS), <code>cheats\desmume</code> (DeSmuME)</td></tr><tr><td>DeSmuME : captures d'écran</td><td><code>screenshots\DeSmuME</code></td></tr></tbody></table>

## Guides

### Jouer aux jeux DSi et aux DSiWare

1. Placez les fichiers DSi dans `bios` (voir **BIOS**).
2. **Core melondsds** : laissez **ÉMULATION > TYPE DE CONSOLE** sur AUTO, la DSi est choisie pour les jeux qui l'exigent. Pour un DSiWare, choisissez DSI pour ce jeu.
3. **melonDS** : choisissez **ÉMULATION > TYPE DE CONSOLE** DSi pour ce jeu.

### Lancer le menu d'une NAND DSi (.bin)

Un fichier NAND contient le menu de la DSi et les titres installés dans sa mémoire (DSiWare). Placez-le dans `roms\nds`, avec l'extension `.bin`, puis lancez-le avec **melonDS** (le plus simple) ou **BizHawk** : la console démarre sur son menu. La NAND est utilisée telle quelle : les sauvegardes de DSiWare et les titres installés y restent.

* Les fichiers DSi (`dsi_bios7.bin`, `dsi_bios9.bin`, `dsi_firmware.bin`) doivent être dans `bios`.
* Au moins un jeu `.nds` doit être présent : dans `roms\nds` pour melonDS, dans le même dossier que la NAND pour BizHawk (la console démarre avec cette cartouche insérée).
* Les cores libretro ne lancent pas les NAND : RetroBat le signale au lancement, choisissez melonDS ou BizHawk pour ce fichier.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (638).png" alt="" width="544"><figcaption></figcaption></figure></div>

### Ajouter des titres dans une NAND

Seul melonDS peut ajouter ou supprimer des titres dans une NAND :

1. Lancez melonDS depuis le dossier `emulators\melonds`.
2. Menu **Config > Emu settings**, onglet **DSi mode** : choisissez la NAND à modifier avec **Browse…**, puis **OK**.
3. Menu **System > Manage DSi titles** : **Import title…**, choisissez le DSiWare à installer, puis **OK**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (637).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="danger" %}
Une NAND se corrompt facilement en cas de mauvaise manipulation, et sa taille est limitée : gardez une copie. Si melonDS affiche un écran noir au lancement d'une NAND, elle n'est pas valide.
{% endhint %}

### Dispositions des écrans

* **Core melondsds** : **VIDÉO > POSITIONNEMENT DES ÉCRANS 1** et **VIDÉO > POSITIONNEMENT DES ÉCRANS 2** définissent deux dispositions (haut-bas et droite-gauche par défaut) ; R2 passe de l'une à l'autre en jeu.
* **Autres émulateurs** : **VIDÉO > POSITIONNEMENT DES ÉCRANS** et **VIDÉO > INVERSER LES ÉCRANS**.

## Problèmes connus

<table><thead><tr><th width="359">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>RetroBat signale que l'émulateur ne prend pas en charge ce format au lancement d'un <code>.bin</code></td><td>Les NAND ne se lancent qu'avec melonDS ou BizHawk : choisissez l'un d'eux pour ce fichier.</td></tr><tr><td>melonDS refuse de lancer un jeu en mode DSi (« dsi bios files are missing »)</td><td>Placez <code>dsi_bios7.bin</code>, <code>dsi_bios9.bin</code>, <code>dsi_firmware.bin</code> et la NAND dans <code>bios</code>.</td></tr><tr><td>melonDS refuse de lancer une NAND (aucun jeu <code>.nds</code> trouvé)</td><td>Ajoutez au moins un jeu <code>.nds</code> (voir <a href="nintendo-ds.md#lancer-le-menu-dune-nand-dsi-.bin"><strong>Lancer le menu d'une NAND DSi</strong></a>).</td></tr><tr><td><strong>ÉMULATION > DÉMARRER DANS LE BIOS</strong> n'a pas d'effet</td><td>Placez <code>bios7.bin</code>, <code>bios9.bin</code> et <code>firmware.bin</code> dans <code>bios</code>, et activez <strong>ÉMULATION > UTILISER LE BIOS EXTERNE</strong> (melonDS, DeSmuME, BizHawk).</td></tr><tr><td>Le stylet ne répond pas à la manette avec melonDS ou DeSmuME</td><td>Ces émulateurs utilisent la souris : utilisez un core libretro ou BizHawk pour jouer au stick droit.</td></tr></tbody></table>
