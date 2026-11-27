---
description: Nintendo
---

# Game Boy Color

<div align="left"><figure><img src="../../../../.gitbook/assets/image (774).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

Le **Game Boy Color** est le successeur du Game Boy, sorti au Japon en octobre 1998, puis en Amérique du Nord et en Europe en novembre 1998. Son écran affiche jusqu'à 56 couleurs à la fois, son processeur peut tourner deux fois plus vite et un port infrarouge permet d'échanger des données entre deux consoles. Il lit aussi tous les jeux Game Boy.

Deux sortes de cartouches existent : les **cartouches noires**, qui fonctionnent aussi sur Game Boy (en noir et blanc), et les **cartouches transparentes**, réservées au Game Boy Color. Parmi ses jeux : Pokémon Or, Argent et Cristal, The Legend of Zelda: Link's Awakening DX et Oracle of Seasons / Ages, Wario Land 3, Shantae, Kirby Tilt 'n' Tumble…

Les jeux se jouent comme les jeux Game Boy : les contrôles, les raccourcis et la plupart des options sont décrits sur la page [**Game Boy**](game-boy.md). Les parties à deux par câble Game Link ont leur propre système, [**Game Boy Color 2 Players**](game-boy-color-2-players.md).

{% embed url="https://fr.wikipedia.org/wiki/Game_Boy_Color" %}

## En bref

<table><thead><tr><th width="286.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\gbc</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gbc .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: gambatte</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (<code>gbc_bios.bin</code> optionnel, pour l'écran de démarrage)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk, jgenesis ; Mesen, Mednafen et ares par raccourcis ; mGBA par son menu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (sauf tgbdual et DoubleCherryGB), BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro (sauf DoubleCherryGB)</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                                      | Pour qui ?               | Points forts                                                                                                           | Limites                                                                 |
| ---------------------------------------------- | ------------------------ | ---------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| **libretro: gambatte** (défaut)                | Tout le monde            | Très précis et léger, correction des couleurs, RetroAchievements, jeu en réseau.                                       | —                                                                       |
| **libretro: tgbdual**                          | Joueurs à deux           | Conçu pour relier deux Game Boy Color : voir [**Game Boy Color 2 Players**](game-boy-color-2-players.md).              | Pas de RetroAchievements. Aucun intérêt pour un jeu à un joueur.        |
| **libretro: sameboy**                          | Puristes                 | Émulation très précise, choix de la révision du Game Boy Color, plusieurs corrections des couleurs, RetroAchievements. | —                                                                       |
| **libretro: DoubleCherryGB**                   | Joueurs à plusieurs      | Relie jusqu'à quatre consoles (voir la page [**Game Boy Color 2 Players**](game-boy-color-2-players.md)).              | Pas de RetroAchievements ni de jeu en réseau.                           |
| **libretro: gearboy**                          | Curieux                  | Émulateur récent, **capteur d'inclinaison** (Kirby Tilt 'n' Tumble), RetroAchievements.                                | —                                                                       |
| **mesen**                                      | Utilisateurs de Mesen    | Mesen 2 : émulation précise, outils de débogage, boutons turbo.                                                        | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.      |
| **jgenesis**                                   | Curieux                  | Émulateur multi-systèmes récent, mode 60 images par seconde.                                                           | Pas de RetroAchievements.                                               |
| **mgba** (autonome)                            | Utilisateurs de mGBA     | mGBA pour Windows : filtres d'image.                                                                                   | Pas de RetroAchievements. Sauvegardes instantanées par le menu de mGBA. |
| **mednafen**                                   | Utilisateurs de Mednafen | Émulation précise, boutons turbo.                                                                                      | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.      |
| **ares**                                       | Puristes                 | Émulation très précise.                                                                                                | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.      |
| **bizhawk: Gambatte**, **GBHawk**, **SameBoy** | Utilisateurs de BizHawk  | Trois émulations au choix, RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.                       | —                                                                       |

**En cas de doute, gardez libretro: gambatte.**

## BIOS

Aucun fichier n'est nécessaire : tous les émulateurs démarrent les jeux sans BIOS.

Le BIOS du Game Boy Color ne sert qu'à afficher l'écran de démarrage d'origine (logo Game Boy animé). Il est utilisé par gambatte et gearboy quand **ÉMULATION > DÉMARRER DEPUIS LE BIOS** est activé, par mGBA (sauf avec **ÉMULATION > SAUTER LE BIOS**) et par BizHawk.

<table><thead><tr><th width="132.75">Fichier</th><th width="216.75">Description</th><th width="77.25">Dossier</th><th>md5</th></tr></thead><tbody><tr><td><code>gbc_bios.bin</code></td><td>BIOS du Game Boy Color</td><td><code>bios</code></td><td>dbfce9db9deaa2567f6a84fde55f9680</td></tr></tbody></table>

Ce fichier est optionnel et contrôlé par RetroBat.

## Quel format de jeu ?

<table><thead><tr><th width="155.25">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gbc</strong></td><td>Image d'une cartouche Game Boy Color (cartouche noire ou transparente).</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive).</td></tr></tbody></table>

Les jeux Game Boy (`.gb`) se rangent dans `roms\gb`.

## Contrôles

RetroBat configure automatiquement les manettes. Les boutons, les options **INVERSER LES BOUTONS A/B/X/Y** et **REMAPPER SELECT SUR** et les raccourcis sont les mêmes que sur la page [**Game Boy**](game-boy.md#controles).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (775).png" alt="" width="338"><figcaption></figcaption></figure></div>

## Dossiers

| Contenu                                                      | Dossier                                                                                                                                                                                          |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Cores libretro, Mesen, Mednafen, mGBA : sauvegardes des jeux | `saves\gbc`                                                                                                                                                                                      |
| Cores libretro : sauvegardes instantanées                    | <p><code>saves\gbc\libretro.&#x3C;core></code></p><p>(ex. <code>saves\gbc\libretro.gambatte</code>)</p>                                                                                          |
| Mesen : sauvegardes instantanées                             | `saves\gbc\mesen\SaveStates`                                                                                                                                                                     |
| Mednafen : sauvegardes instantanées                          | `saves\gbc\mednafen\sstates`                                                                                                                                                                     |
| mGBA : sauvegardes instantanées                              | `saves\gbc\mgba\sstates`                                                                                                                                                                         |
| ares : sauvegardes des jeux et instantanées                  | `saves\gbc\ares`                                                                                                                                                                                 |
| jgenesis : sauvegardes des jeux                              | `saves\gbc\jgenesis`                                                                                                                                                                             |
| BizHawk : sauvegardes des jeux                               | `saves\gbc\bizhawk`                                                                                                                                                                              |
| BIOS                                                         | `bios`                                                                                                                                                                                           |
| Codes de triche                                              | <p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\mgba</code> (mGBA)</p><p><code>cheats\jgenesis</code> (jgenesis)</p><p><code>cheats\bizhawk\gbc</code> (BizHawk)</p>               |
| Captures d'écran                                             | <p><code>screenshots\mesen</code></p><p><code>screenshots\mednafen</code></p><p><code>screenshots\mgba</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\gbc</code></p> |

## Guides

### Couleurs de l'écran

L'écran du Game Boy Color n'était pas rétroéclairé : les jeux utilisent des couleurs très vives, qui paraissent criardes sur un écran moderne. Plusieurs émulateurs les corrigent :

<table><thead><tr><th width="184.5">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>core gambatte</td><td><strong>RENDU VISUEL > CORRECTION DES COULEURS</strong></td><td><strong>GBC UNIQUEMENT</strong>, <strong>TOUJOURS</strong> ou <strong>DÉSACTIVÉ</strong>.</td></tr><tr><td>core sameboy</td><td><strong>RENDU VISUEL > MODE DE CORRECTION DES COULEURS</strong></td><td><strong>MODERNE ÉQUILIBRÉ</strong>, <strong>MODERNE PRÉCIS</strong>, <strong>MODERNE CONTRASTE RENFORCÉ</strong>, <strong>RÉDUIRE LA LUMINOSITÉ</strong>, <strong>CORRIGER LES COURBES DE COULEUR</strong>, <strong>RÉALITÉ BRUTE</strong> ou <strong>DÉSACTIVÉ</strong>.</td></tr><tr><td>core gearboy</td><td><strong>RENDU VISUEL > CORRECTION DES COULEURS</strong></td><td>Active ou non la correction.</td></tr><tr><td>jgenesis</td><td><strong>RENDU VISUEL > CORRECTION DES COULEURS</strong></td><td><strong>LCD GAMEBOY COLOR</strong>, <strong>LCD GAMEBOY ADVANCE</strong> ou <strong>AUCUN</strong>.</td></tr></tbody></table>

### Kirby Tilt 'n' Tumble (capteur d'inclinaison)

Kirby Tilt 'n' Tumble se joue en inclinant la console. Avec le core gearboy, choisissez ce qui remplace l'inclinaison dans **CONTRÔLES > CONTRÔLE D'INCLINAISON** : **STICK ANALOGIQUE** (défaut) ou **SOURIS**.

### Bonus Game Boy Advance

Quelques jeux Game Boy Color débloquent des bonus quand ils sont lancés sur une Game Boy Advance (comme la boutique secrète de The Legend of Zelda: Oracle of Seasons / Ages). Pour les obtenir :

<table><thead><tr><th width="186.5">Émulateur</th><th>Option</th></tr></thead><tbody><tr><td>core gambatte</td><td><strong>ÉMULATION > FORCER LE TYPE DE CONSOLE > GBA</strong></td></tr><tr><td>core gearboy</td><td><strong>ÉMULATION > FORCER LE TYPE DE CONSOLE > GBA</strong></td></tr><tr><td>jgenesis</td><td><strong>ÉMULATION > ÉMULER UNE GBA</strong></td></tr></tbody></table>

### Autres options utiles

<table><thead><tr><th width="168.25">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>core sameboy</td><td><strong>ÉMULATION > MODÈLE DE GAME BOY</strong></td><td>Game Boy Color CGB-E (défaut) ou CGB-D, ou un autre modèle.</td></tr><tr><td>core gambatte</td><td><strong>RENDU VISUEL > MÉLANGE INTER-IMAGE</strong></td><td>Reproduit la rémanence de l'écran (transparences par clignotement) : <strong>PRÉCIS</strong> par défaut.</td></tr><tr><td>jgenesis</td><td><strong>ÉMULATION > FORCER LE MODE GB</strong></td><td>Lance une cartouche noire en mode Game Boy (noir et blanc).</td></tr><tr><td>jgenesis</td><td><strong>ÉMULATION > VISER 60 FPS</strong></td><td>Fait tourner les jeux à 60 images par seconde.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="309">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Un jeu <code>.gb</code> n'apparaît pas</td><td>Les jeux Game Boy se rangent dans <code>roms\gb</code>.</td></tr><tr><td>Les couleurs sont trop vives</td><td>Voir <a href="game-boy-color.md#couleurs-de-lecran"><strong>Couleurs de l'écran</strong></a>.</td></tr><tr><td>Kirby Tilt 'n' Tumble ne réagit pas</td><td>Utilisez le core gearboy : voir <a href="game-boy-color.md#kirby-tilt-n-tumble-capteur-dinclinaison"><strong>Kirby Tilt 'n' Tumble</strong></a>.</td></tr><tr><td>Le jeu à deux ne fonctionne pas</td><td>Rangez le jeu dans <code>roms\gbc2players</code>.</td></tr></tbody></table>
