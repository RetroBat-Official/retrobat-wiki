---
description: Atari
---

# Jaguar CD

<div align="left"><figure><img src="../../../../.gitbook/assets/image (581).png" alt="" width="298"><figcaption></figcaption></figure></div>

## Présentation

Le **Jaguar CD** est le lecteur de CD-ROM de la Jaguar (voir la page [**Jaguar**](jaguar.md)). Il sort en septembre 1995 aux États-Unis et se pose sur le dessus de la console, à la place de la cartouche. Son lecteur double vitesse lit les jeux sur CD et les CD audio, accompagnés d'effets visuels : la Virtual Light Machine de Jeff Minter.

Les parties se sauvegardent sur une cartouche à part, la Memory Track, branchée sur le dessus du lecteur. Arrivé tard, alors que la PlayStation et la Saturn occupent le marché, le Jaguar CD ne reçoit qu'une douzaine de jeux, dont Myst, Battlemorph, Highlander, Blue Lightning, Primal Rage, Baldies, Dragon's Lair et Space Ace. Atari arrête la Jaguar l'année suivante.

{% embed url="https://fr.wikipedia.org/wiki/Jaguar_CD" %}

## En bref

<table><thead><tr><th width="242.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\jaguarcd</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .cdi .bigpimg .zip .7z .squashfs</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>bigpemu</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun obligatoire</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BigPEmu, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>[BIOS] Atari Jaguar CD (World).j64</code> (libretro: virtualjaguar, avec <strong>DÉMARRER DEPUIS LE BIOS</strong>)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="141.5">Émulateur</th><th width="180">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>bigpemu</strong> (défaut)</td><td>Tout le monde</td><td>Fait tourner tous les jeux du Jaguar CD. Memory Track branchée automatiquement, sauvegardes instantanées, retour en arrière, tout le pavé numérique sur la manette. Lit aussi les images <code>.bigpimg</code>.</td><td>Pas de RetroAchievements. Raccourcis sur L2 au lieu du bouton HOTKEY.</td></tr><tr><td><strong>libretro: virtualjaguar</strong></td><td>Ceux qui veulent les RetroAchievements ou le jeu en réseau</td><td>Intégré à RetroArch : shaders, décorations, RetroAchievements, jeu en réseau. BIOS du CD inclus dans le core, vitesse de lecture du CD réglable.</td><td>Ne lit pas les jeux <code>.cue</code> compressés (<code>.zip</code>, <code>.7z</code>, <code>.squashfs</code>) ni les <code>.bigpimg</code>.</td></tr><tr><td><strong>bizhawk</strong> (Jaguar)</td><td>Speedrun assisté (TAS)</td><td>Outils d'enregistrement et d'analyse, RetroAchievements.</td><td>Compatibilité CD plus faible. Ne lit pas les <code>.cdi</code> ni les <code>.bigpimg</code>.</td></tr></tbody></table>

**En cas de doute, gardez BigPEmu. Passez à libretro: virtualjaguar pour les RetroAchievements.**

## BIOS

Aucun fichier n'est nécessaire : BigPEmu et BizHawk s'en passent, et libretro: virtualjaguar inclut le BIOS du lecteur CD.

| Fichier                                          | MD5                                | Emplacement | Émulateur               |
| ------------------------------------------------ | ---------------------------------- | ----------- | ----------------------- |
| `[BIOS] Atari Jaguar CD (World).j64` (optionnel) | `77cd95c7ad06a39f4c59995094aa10f9` | `bios`      | libretro: virtualjaguar |

Avec libretro: virtualjaguar, l'option **ÉMULATION > DÉMARRER DEPUIS LE BIOS** démarre le jeu par le vrai BIOS du lecteur et son animation. Le core utilise alors `[BIOS] Atari Jaguar CD (World).j64` s'il est présent dans `bios`, sinon sa copie intégrée.

## Quel format de jeu ?

<table><thead><tr><th width="186.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.cue</strong> (+ .bin)</td><td>Le format conseillé (copies Redump). Accepté par tous les émulateurs.</td></tr><tr><td>.cdi</td><td>Accepté par BigPEmu et libretro: virtualjaguar, pas par BizHawk. Certaines copies <code>.cdi</code> sont mal faites : en cas de souci, préférez la version <code>.cue</code>.</td></tr><tr><td>.bigpimg</td><td>Format propre à BigPEmu, lu par lui seul.</td></tr><tr><td>.zip, .7z, .squashfs</td><td>Le jeu compressé. BigPEmu et BizHawk le décompressent. libretro: virtualjaguar n'accepte qu'un <code>.cdi</code> compressé en <code>.zip</code> ou <code>.7z</code>.</td></tr></tbody></table>

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour tous les émulateurs, exactement comme pour la Jaguar : les boutons A, B, C, Pause, Option et le pavé numérique sont placés de la même façon. Le tableau complet et les options (Team Tap, manette Jaguar Pro, stick gauche) sont sur la page [**Jaguar**](jaguar.md#controles).

### Raccourcis

Le core libretro virtualjaguar utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)). Avec BigPEmu, les raccourcis se font avec **L2** à la place du bouton HOTKEY, sauf pour quitter (**HOTKEY + START**). Les raccourcis de BigPEmu et de BizHawk sont détaillés sur la page [**Jaguar**](jaguar.md#raccourcis).

## Dossiers

| Contenu                                                    | Dossier                                 |
| ---------------------------------------------------------- | --------------------------------------- |
| BIOS du CD (optionnel, libretro: virtualjaguar)            | `bios`                                  |
| Sauvegardes des cores libretro (Memory Track)              | `saves\jaguarcd`                        |
| Sauvegardes de BizHawk                                     | `saves\jaguarcd\bizhawk`                |
| Sauvegardes instantanées des cores libretro                | `saves\jaguarcd\libretro.virtualjaguar` |
| Sauvegardes instantanées de BigPEmu                        | `saves\jaguarcd\bigpemu`                |
| Sauvegardes instantanées de BizHawk                        | `saves\jaguarcd\bizhawk\sstates\Jaguar` |
| Configuration et données de BigPEmu (dont la Memory Track) | `emulators\bigpemu\userdata`            |
| Captures d'écran des cores libretro                        | `screenshots`                           |
| Captures d'écran de BizHawk                                | `screenshots\bizhawk\jaguarcd`          |
| Codes de triche des cores libretro                         | `cheats\retroarch`                      |
| Codes de triche de BizHawk                                 | `cheats\bizhawk\jaguarcd`               |

## Guides

### Sauvegarder ses parties (Memory Track)

Les jeux du Jaguar CD sauvegardent sur la cartouche Memory Track. Vous n'avez rien à faire :

* **BigPEmu** : RetroBat branche le lecteur CD et la Memory Track à chaque lancement d'un jeu du système Jaguar CD (ou d'un fichier `.cue`).
* **libretro: virtualjaguar** : le core émule la Memory Track et range les sauvegardes dans `saves\jaguarcd`.

### Réduire les temps de chargement

Le vrai lecteur est un double vitesse, et les chargements peuvent être longs. Avec libretro: virtualjaguar, l'option **ÉMULATION > VITESSE DE LECTURE CD** accélère la lecture (**4X**, **8X** ou **INSTANT**). Une vitesse trop élevée peut faire planter certains jeux : revenez à **AUTO** (double vitesse) en cas de problème.

## Problèmes connus

| Problème                                                                                          | Solution                                                                                                                           |
| ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| Un jeu `.cue` compressé (`.zip`, `.7z`, `.squashfs`) ne se lance pas avec libretro: virtualjaguar | Décompressez-le dans `roms\jaguarcd`, ou utilisez BigPEmu.                                                                         |
| Un jeu `.cdi` ne se lance pas ou s'arrête sur l'écran de choix (World Tour Racing par exemple)    | La copie est souvent mauvaise : utilisez la version `.cue` (Redump). BizHawk ne lit pas du tout les `.cdi`.                        |
| Un fichier `.bigpimg` ne se lance pas                                                             | Ce format n'est lu que par BigPEmu.                                                                                                |
| Les chargements sont longs                                                                        | Avec libretro: virtualjaguar, augmentez **VITESSE DE LECTURE CD**.                                                                 |
| Les raccourcis ne répondent pas avec BigPEmu                                                      | Ils se font avec **L2**, pas avec le bouton HOTKEY.                                                                                |
| Un jeu demande les touches 7, 8 ou 9 du pavé                                                      | Avec libretro: virtualjaguar, activez **MAPPER LA MANETTE JAGUAR PRO**, ou utilisez BigPEmu qui place tout le pavé sur la manette. |
