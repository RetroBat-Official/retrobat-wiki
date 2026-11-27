---
description: Nintendo
---

# Game Boy

<div align="left"><figure><img src="../../../../.gitbook/assets/image (770).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

Le **Game Boy** est la console portable de Nintendo conçue par l'équipe de Gunpei Yokoi, sortie au Japon en avril 1989, en Amérique du Nord la même année et en Europe en 1990. Son écran affiche quatre niveaux de gris-vert et quatre piles AA lui donnent une trentaine d'heures d'autonomie. Avec le Game Boy Color, il s'est vendu à près de 120 millions d'exemplaires.

Livré avec Tetris, il a reçu Super Mario Land, The Legend of Zelda: Link's Awakening, Kirby's Dream Land, Metroid II, Wario Land et surtout Pokémon Rouge et Bleu. Le **câble Game Link** relie deux consoles pour jouer à deux ou échanger des Pokémon : ces parties ont leur propre système dans RetroBat, [**Game Boy 2 Players**](game-boy-2-players.md). Les jeux Game Boy Color et les jeux sur Super Game Boy ont aussi leur système.

{% embed url="https://fr.wikipedia.org/wiki/Game_Boy" %}

## En bref

<table><thead><tr><th width="277.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\gb</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gb .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: gambatte</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (<code>gb_bios.bin</code> optionnel, pour l'écran de démarrage)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk, jgenesis ; Mesen, Mednafen et ares par raccourcis ; mGBA par son menu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (sauf tgbdual et DoubleCherryGB), BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro (sauf DoubleCherryGB)</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                                      | Pour qui ?               | Points forts                                                                                                                                   | Limites                                                                 |
| ---------------------------------------------- | ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| **libretro: gambatte** (défaut)                | Tout le monde            | Très précis et léger, nombreuses palettes, colorisation des jeux comme sur Game Boy Color ou Super Game Boy, RetroAchievements, jeu en réseau. | —                                                                       |
| **libretro: mesen-s**                          | Puristes                 | Émulation précise de Mesen-S.                                                                                                                  | Peu d'options pour le Game Boy.                                         |
| **libretro: tgbdual**                          | Joueurs à deux           | Conçu pour relier deux Game Boy : voir [**Game Boy 2 Players**](game-boy-2-players.md).                                                        | Pas de RetroAchievements. Aucun intérêt pour un jeu à un joueur.        |
| **libretro: sameboy**                          | Puristes                 | Émulation très précise, choix du modèle (Game Boy, Game Boy Pocket…), RetroAchievements.                                                       | —                                                                       |
| **libretro: DoubleCherryGB**                   | Joueurs à plusieurs      | Relie jusqu'à quatre Game Boy (voir [**Jouer à plusieurs**](game-boy.md#jouer-a-plusieurs)).                                                   | Pas de RetroAchievements ni de jeu en réseau.                           |
| **libretro: gearboy**                          | Curieux                  | Émulateur récent, palettes, suppression de la limite de sprites, RetroAchievements.                                                            | —                                                                       |
| **mesen**                                      | Utilisateurs de Mesen    | Mesen 2 : émulation précise, outils de débogage, boutons turbo.                                                                                | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.      |
| **jgenesis**                                   | Curieux                  | Émulateur multi-systèmes récent, mode 60 images par seconde.                                                                                   | Pas de RetroAchievements.                                               |
| **mgba** (autonome)                            | Utilisateurs de mGBA     | mGBA pour Windows : filtres d'image.                                                                                                           | Pas de RetroAchievements. Sauvegardes instantanées par le menu de mGBA. |
| **mednafen**                                   | Utilisateurs de Mednafen | Émulation précise, boutons turbo.                                                                                                              | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.      |
| **ares**                                       | Puristes                 | Émulation très précise.                                                                                                                        | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.      |
| **bizhawk: Gambatte**, **GBHawk**, **SameBoy** | Utilisateurs de BizHawk  | Trois émulations au choix, RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.                                               | —                                                                       |

**En cas de doute, gardez libretro: gambatte.**

## BIOS

Aucun fichier n'est nécessaire : tous les émulateurs démarrent les jeux sans BIOS.

Le BIOS du Game Boy ne sert qu'à afficher l'écran de démarrage d'origine (le logo Nintendo qui descend). Il est utilisé par gambatte et gearboy quand **ÉMULATION > DÉMARRER DEPUIS LE BIOS** est activé, par mGBA (sauf avec **ÉMULATION > SAUTER LE BIOS**) et par BizHawk.

<table><thead><tr><th width="124">Fichier</th><th width="171">Description</th><th width="107.25">Dossier</th><th>md5</th></tr></thead><tbody><tr><td><code>gb_bios.bin</code></td><td>BIOS du Game Boy (DMG)</td><td><code>bios</code></td><td>32fbbd84168d3482956eb3c5051637f5</td></tr></tbody></table>

Ce fichier est optionnel et contrôlé par RetroBat.

## Quel format de jeu ?

<table><thead><tr><th width="176.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gb</strong></td><td>Image d'une cartouche Game Boy.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive).</td></tr></tbody></table>

Les jeux Game Boy Color (`.gbc`), y compris ceux qui fonctionnent aussi sur Game Boy (cartouches noires), se rangent dans `roms\gbc`. Pour jouer avec les bordures et les couleurs du Super Game Boy, rangez les jeux dans `roms\sgb`.

## Contrôles

RetroBat configure automatiquement les manettes pour tous les émulateurs. Les boutons gardent la place qu'ils ont sur la manette Super Nintendo :

<table><thead><tr><th width="221.5">Manette RetroBat</th><th>Game Boy</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>SUD</td><td>B</td></tr><tr><td>EST</td><td>A</td></tr><tr><td>OUEST</td><td>TURBO B (core gambatte, Mesen, Mednafen)</td></tr><tr><td>NORD</td><td>TURBO A (core gambatte, Mesen, Mednafen)</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (771).png" alt="" width="338"><figcaption></figcaption></figure></div>

Core gambatte :

<div align="left"><figure><img src="../../../../.gitbook/assets/image (772).png" alt="" width="338"><figcaption></figcaption></figure></div>

Mesen et Mednafen :

<div align="left"><figure><img src="../../../../.gitbook/assets/image (773).png" alt="" width="338"><figcaption></figcaption></figure></div>

Deux options de **CONTRÔLES** sont proposées pour tous les émulateurs (sauf **REMAPPER SELECT SUR** avec BizHawk) :

<table><thead><tr><th width="310.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>INVERSER LES BOUTONS A/B/X/Y</strong></td><td>Place A sur SUD et B sur EST (lettres d'une manette Xbox), turbos compris.</td></tr><tr><td><strong>REMAPPER SELECT SUR</strong></td><td>Met SELECT sur une autre touche (L1, R1, L2, R2, L3 ou R3), pratique quand SELECT sert aussi de touche HOTKEY.</td></tr></tbody></table>

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

Mesen, Mednafen, ares, jgenesis et BizHawk utilisent les raccourcis de RetroBat :

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

jgenesis n'a pas de raccourci pour la capture d'écran. Avec mGBA, seul HOTKEY + START (quitter) est configuré : les sauvegardes instantanées se font depuis son menu.

## Dossiers

<table><thead><tr><th width="362.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Cores libretro, Mesen, Mednafen, mGBA : sauvegardes des jeux</td><td><code>saves\gb</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><p><code>saves\gb\libretro.&#x3C;core></code></p><p>(ex. <code>saves\gb\libretro.gambatte</code>)</p></td></tr><tr><td>Mesen : sauvegardes instantanées</td><td><code>saves\gb\mesen\SaveStates</code></td></tr><tr><td>Mednafen : sauvegardes instantanées</td><td><code>saves\gb\mednafen\sstates</code></td></tr><tr><td>mGBA : sauvegardes instantanées</td><td><code>saves\gb\mgba\sstates</code></td></tr><tr><td>ares : sauvegardes des jeux et instantanées</td><td><code>saves\gb\ares</code></td></tr><tr><td>jgenesis : sauvegardes des jeux</td><td><code>saves\gb\jgenesis</code></td></tr><tr><td>BizHawk : sauvegardes des jeux</td><td><code>saves\gb\bizhawk</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>Codes de triche</td><td><p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\mgba</code> (mGBA)</p><p><code>cheats\jgenesis</code> (jgenesis)</p><p><code>cheats\bizhawk\gb</code> (BizHawk)</p></td></tr><tr><td>Captures d'écran</td><td><p><code>screenshots\mesen</code></p><p><code>screenshots\mednafen</code></p><p><code>screenshots\mgba</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\gb</code></p></td></tr></tbody></table>

## Guides

### Couleurs et palettes

Sur un vrai Game Boy, l'image est en quatre teintes de vert. Plusieurs émulateurs proposent d'autres couleurs :

<table><thead><tr><th width="167">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>core gambatte</td><td><strong>RENDU VISUEL > COLORISATION</strong></td><td><strong>AUTOMATIQUE</strong> : la palette que le Game Boy Color ou le Super Game Boy donne au jeu ; <strong>GAMEBOY COLOR</strong> ou <strong>SUPER GAMEBOY</strong> : palettes de ces consoles ; <strong>INTERNE</strong> : palette choisie dans <strong>PALETTE</strong>.</td></tr><tr><td>core gambatte</td><td><strong>RENDU VISUEL > PALETTE</strong></td><td>Palettes du Game Boy (DMG, Pocket, Light), du Game Boy Color et de nombreuses palettes d'amateurs (TWB64, PixelShift).</td></tr><tr><td>core sameboy</td><td><strong>RENDU VISUEL > PALETTE</strong></td><td>Niveaux de gris, citron vert, olive ou bleu sarcelle.</td></tr><tr><td>core gearboy</td><td><strong>RENDU VISUEL > PALETTE</strong></td><td>Original, net, noir/blanc, automne, doux, slime.</td></tr><tr><td>jgenesis</td><td><strong>RENDU VISUEL > PALETTE</strong></td><td>Palettes du Game Boy.</td></tr></tbody></table>

### Écran du Game Boy (rémanence)

L'écran du Game Boy est lent : certains jeux font clignoter des objets pour simuler la transparence (vagues, fantômes…). Sur un écran moderne, ce clignotement devient visible. Le core gambatte reproduit l'écran d'origine par défaut (**RENDU VISUEL > MÉLANGE INTER-IMAGE > PRÉCIS**). Avec un autre émulateur, utilisez gambatte.

### Jouer à plusieurs

Les jeux à deux joueurs par câble Game Link (Tetris, F-1 Race, Pokémon…) se jouent dans le système [**Game Boy 2 Players**](game-boy-2-players.md) (`roms\gb2players`), qui affiche les deux consoles côte à côte : voir sa page.

Le core DoubleCherryGB relie aussi plusieurs Game Boy dans ce système, avec **ÉMULATION > NOMBRE DE JOUEURS** (jusqu'à 4) et **ÉMULATION > TYPE DE CÂBLE MULTIJOUEURS** (adaptateur 4 joueurs pour F-1 Race, câble en anneau de Faceball 2000…).

### Autres options utiles

| Émulateur                   | Option                                                  | Effet                                                                                        |
| --------------------------- | ------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| core sameboy                | **ÉMULATION > MODÈLE DE GAME BOY**                      | Game Boy (défaut), Game Boy Pocket/Light ou Game Boy Color.                                  |
| core gambatte, core gearboy | **ÉMULATION > FORCER LE TYPE DE CONSOLE**               | Fait tourner le jeu sur une autre console : Game Boy Color ou GBA (gambatte), GBA (gearboy). |
| core gearboy                | **RENDU VISUEL > DÉSACTIVER LA LIMITE DE SPRITES**      | Supprime les clignotements quand beaucoup d'objets sont à l'écran.                           |
| jgenesis                    | **ÉMULATION > VISER 60 FPS**                            | Fait tourner les jeux à 60 images par seconde (le Game Boy en affiche un peu moins de 60).   |
| Mesen                       | **RÉDUCTION DE LA LATENCE > NOMBRE D'IMAGES EN AVANCE** | Réduit le délai entre l'appui sur un bouton et l'action à l'écran.                           |

## Problèmes connus

| Problème                                       | Solution                                                                                                       |
| ---------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| Un jeu `.gbc` n'apparaît pas                   | Les jeux Game Boy Color se rangent dans `roms\gbc`.                                                            |
| Des objets clignotent (transparences)          | Utilisez le core gambatte : voir [**Écran du Game Boy (rémanence)**](game-boy.md#ecran-du-game-boy-remanence). |
| Pas de bordure Super Game Boy                  | Rangez le jeu dans `roms\sgb`.                                                                                 |
| Le logo Nintendo ne s'affiche pas au démarrage | Ajoutez `gb_bios.bin` dans `bios` et activez **DÉMARRER DEPUIS LE BIOS** (gambatte, gearboy).                  |
| Le jeu à deux ne fonctionne pas                | Rangez le jeu dans `roms\gb2players`.                                                                          |
