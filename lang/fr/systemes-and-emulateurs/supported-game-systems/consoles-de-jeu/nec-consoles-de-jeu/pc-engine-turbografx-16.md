---
description: NEC
---

# PC Engine/TurboGrafx-16

<div align="left"><figure><img src="../../../../.gitbook/assets/image (697).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **PC Engine** est une console de salon de NEC, conçue avec Hudson Soft et sortie au Japon en octobre 1987. Ses jeux tiennent sur des **HuCard**, des cartes au format d'une carte de crédit. Son processeur 8 bits (HuC6280) est associé à un processeur graphique 16 bits : en Amérique du Nord, elle sort en 1989 sous le nom de **TurboGrafx-16**.

Très populaire au Japon, où elle rivalise avec la Famicom puis la Super Famicom, elle est réputée pour ses shoot'em up et ses adaptations de jeux d'arcade : R-Type, Bomberman, PC Genjin (Bonk's Adventure), Gunhed (Blazing Lazers), Splatterhouse, Soldier Blade, Parasol Stars… Elle n'a qu'une prise manette : pour jouer à plusieurs, il faut un multitap (le TurboTap), jusqu'à 5 joueurs.

La console a connu de nombreux modèles (CoreGrafx, Shuttle, portable PC Engine GT, PC Engine Duo…) et des extensions. Dans RetroBat, les jeux sur CD ont leur propre système ([**PC Engine CD**](pc-engine-cd-rom-turbografx-cd.md)), comme les jeux de la [**SuperGrafx**](supergrafx.md), une version améliorée de la console.

{% embed url="https://fr.wikipedia.org/wiki/PC-Engine" %}

## En bref

<table><thead><tr><th width="270.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\pcengine</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pce .bin .zip .7z .wad .squashfs</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: mednafen_pce</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk ; Mednafen, Mesen et ares par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores mednafen et geargrafx, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="187.75">Émulateur</th><th width="144">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: mednafen_pce</strong> (défaut)</td><td>Tout le monde</td><td>Beetle PCE, l'émulation PC Engine complète de Mednafen : très précise, manette 6 boutons, souris, multitap, jeux SuperGrafx, RetroAchievements, jeu en réseau.</td><td>—</td></tr><tr><td><strong>libretro: mednafen_pce_fast</strong></td><td>Petites configurations</td><td>Version allégée de Beetle PCE, plus rapide.</td><td>Moins précis. N'émule pas la SuperGrafx.</td></tr><tr><td><strong>libretro: geargrafx</strong></td><td>Curieux</td><td>Émulateur récent et précis : choix du modèle de console, manettes Avenue Pad 3 et 6, palettes de couleurs.</td><td>—</td></tr><tr><td><strong>libretro: fbneo</strong></td><td>Utilisateurs de FBNeo</td><td>Mêmes réglages que les jeux d'arcade de FBNeo.</td><td>Jeux en <code>.zip</code> ou <code>.7z</code> nommés comme les sets PC Engine de FBNeo uniquement.</td></tr><tr><td><strong>mednafen</strong> (autonome)</td><td>Utilisateurs de Mednafen</td><td>Même émulation que le core mednafen_pce.</td><td>Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr><tr><td><strong>mesen</strong></td><td>Utilisateurs de Mesen</td><td>Mesen 2 : émulation précise et outils de débogage.</td><td>Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr><tr><td><strong>ares</strong></td><td>Puristes</td><td>Émulation très précise.</td><td>Un seul joueur. Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr><tr><td><strong>bizhawk: HyperNyma</strong>, <strong>PCEHawk</strong>, <strong>TurboNyma</strong></td><td>Utilisateurs de BizHawk</td><td>HyperNyma et TurboNyma reprennent Mednafen (pce_fast et pce), PCEHawk est le core maison de BizHawk. RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.</td><td>—</td></tr><tr><td><strong>magicengine</strong></td><td>Nostalgiques</td><td>Émulateur PC Engine historique, rendu haute résolution et scanlines.</td><td>Pas de RetroAchievements. Sauvegardes instantanées non gérées par RetroBat. Un seul raccourci : quitter.</td></tr></tbody></table>

**En cas de doute, gardez libretro: mednafen\_pce.**

## BIOS

Aucun BIOS n'est nécessaire pour les jeux HuCard. Les BIOS des jeux sur CD (System Card) sont décrits sur la page [**PC Engine CD**](https://app.gitbook.com/s/exdzL60ZuqPLldz2AYta/systems-and-emulators/supported-game-systems/game-consoles/nec-consoles/pc-engine-cd-rom-turbografx-cd).

## Quel format de jeu ?

<table><thead><tr><th width="181.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.pce</strong></td><td>Image d'une HuCard. Lue par tous les émulateurs, sauf FBNeo. Les jeux japonais et américains (TurboGrafx-16) vont dans le même dossier.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu <code>.pce</code> compressé (un jeu par archive).</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong> (FBNeo)</td><td>FBNeo ne lit que les archives qui portent le nom de ses sets PC Engine (voir la liste des jeux de FBNeo).</td></tr></tbody></table>

Les jeux SuperGrafx se rangent dans `roms\supergrafx`, les jeux sur CD dans `roms\pcenginecd`.

## Contrôles

RetroBat configure automatiquement les manettes pour tous les émulateurs. La manette PC Engine a une croix, deux boutons **I** et **II**, un bouton **SELECT** et un bouton **RUN**. Quelques jeux de combat utilisent une manette à 6 boutons (Avenue Pad 6, boutons **III** à **VI**), comme Street Fighter II' Champion Edition.

<table><thead><tr><th width="219">Manette RetroBat</th><th>PC Engine</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>EST</td><td>I</td></tr><tr><td>SUD</td><td>II</td></tr><tr><td>OUEST</td><td>III (manette 6 boutons)</td></tr><tr><td>NORD</td><td>IV (manette 6 boutons)</td></tr><tr><td>L1</td><td>V (manette 6 boutons)</td></tr><tr><td>R1</td><td>VI (manette 6 boutons)</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>RUN</td></tr><tr><td>L2</td><td>Passage 2 / 6 boutons (cores mednafen, Mednafen) ; manette 2 boutons (BizHawk)</td></tr><tr><td>R2</td><td>Manette 6 boutons (BizHawk)</td></tr></tbody></table>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/pcengine_simple_6buttons.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

Mednafen, Mesen, ares et BizHawk utilisent les raccourcis de RetroBat :

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

Avec MagicEngine, seul HOTKEY + START (ou `Échap`) est disponible, pour quitter.

## Dossiers

<table><thead><tr><th width="342.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Cores libretro, Mednafen, Mesen : sauvegardes des jeux</td><td><code>saves\pcengine</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><p><code>saves\pcengine\libretro.&#x3C;core></code></p><p>(ex. <code>saves\pcengine\libretro.mednafen_pce</code>)</p></td></tr><tr><td>Mednafen : sauvegardes instantanées</td><td><code>saves\pcengine\mednafen\sstates</code></td></tr><tr><td>Mesen : sauvegardes instantanées</td><td><code>saves\pcengine\mesen\SaveStates</code></td></tr><tr><td>ares : sauvegardes des jeux et instantanées</td><td><code>saves\pcengine\ares</code></td></tr><tr><td>BizHawk : sauvegardes des jeux</td><td><code>saves\pcengine\bizhawk</code></td></tr><tr><td>BizHawk : sauvegardes instantanées</td><td><code>saves\pcengine\bizhawk\sstates\&#x3C;core></code></td></tr><tr><td>MagicEngine : sauvegardes</td><td><code>saves\pcengine\magicengine</code></td></tr><tr><td>Codes de triche</td><td><p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\bizhawk\pcengine</code> (BizHawk)</p><p><code>cheats\magicengine\pcengine</code> (MagicEngine)</p></td></tr><tr><td>Captures d'écran</td><td><p><code>screenshots\mednafen</code></p><p><code>screenshots\mesen</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\pcengine</code></p><p><code>screenshots\magicengine</code></p></td></tr></tbody></table>

## Guides

### Jouer à plusieurs (multitap)

La PC Engine n'a qu'une prise manette : à partir de 2 joueurs, le multitap (TurboTap) est nécessaire. RetroBat le branche pour vous, jusqu'à 5 joueurs :

<table><thead><tr><th width="236.5">Émulateur</th><th>Multitap</th></tr></thead><tbody><tr><td>core mednafen_pce</td><td>Branché dès qu'une 2e manette est connectée (<strong>CONTRÔLES > ACTIVER LE MULTITAP</strong> pour le forcer)</td></tr><tr><td>core mednafen_pce_fast</td><td>Toujours branché</td></tr><tr><td>core geargrafx</td><td>Branché dès qu'une 2e manette est connectée (<strong>CONTRÔLES > UTILISER LE TURBO-TAP</strong> pour le forcer)</td></tr><tr><td>Mednafen</td><td>Branché dès qu'une 2e manette est connectée (<strong>CONTRÔLES > ADAPTATEUR MULTIJOUEURS</strong> pour le forcer)</td></tr><tr><td>Mesen</td><td>Branché dès qu'une 2e manette est connectée (<strong>CONTRÔLES > ADAPTATEUR MULTIJOUEURS</strong> pour le forcer)</td></tr><tr><td>BizHawk</td><td>Géré automatiquement</td></tr><tr><td>ares</td><td>Un seul joueur</td></tr></tbody></table>

Quelques jeux fonctionnent mal avec le multitap branché, comme Cho Aniki (PC Engine CD) : pour y jouer avec plusieurs manettes connectées, réglez l'option du multitap sur **NON**. mednafen\_pce\_fast ne permet pas de le retirer.

### Manette 6 boutons

Pour les jeux qui l'utilisent (Street Fighter II' Champion Edition…), activez la manette 6 boutons :

<table><thead><tr><th width="315.25">Émulateur</th><th>Réglage</th></tr></thead><tbody><tr><td>cores mednafen_pce, mednafen_pce_fast</td><td><strong>CONTRÔLES > UTILISER LA MANETTE 6 BOUTONS</strong>, ou L2 en jeu</td></tr><tr><td>core geargrafx</td><td><strong>CONTRÔLES > TYPE DE CONTRÔLEUR > AVENUE PAD 6</strong></td></tr><tr><td>Mednafen</td><td>L2 en jeu</td></tr><tr><td>Mesen</td><td><strong>CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1 > MANETTE 6 BOUTONS</strong></td></tr><tr><td>ares</td><td><strong>CONTRÔLES > UTILISER LA MANETTE 6 BOUTONS</strong></td></tr><tr><td>BizHawk (HyperNyma, TurboNyma)</td><td>R2 en jeu (L2 pour revenir à 2 boutons)</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (698).png" alt=""><figcaption></figcaption></figure></div>

### Souris

Quelques jeux utilisent la souris PC Engine. Avec les cores mednafen, choisissez **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1 > SOURIS**.

### Autres options utiles

| Émulateur                                | Option                                      | Effet                                                                                                              |
| ---------------------------------------- | ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| core mednafen\_pce                       | **VIDÉO > TYPE DE SIGNAL ÉMULÉ**            | **COMPOSITE** (défaut dans RetroBat) recrée la sortie d'origine de la console, **RGB** donne une image plus nette. |
| cores mednafen, Mesen                    | **VIDÉO > DÉSACTIVER LA LIMITE DE SPRITES** | Supprime les clignotements quand beaucoup d'objets sont à l'écran (core geargrafx : dans **ÉMULATION**).           |
| core mednafen\_pce                       | **ÉMULATION > OVERCLOCKING CPU**            | Réduit les ralentissements, mais peut causer des bugs.                                                             |
| core geargrafx                           | **ÉMULATION > TYPE DE CONSOLE**             | **PC ENGINE (JP)**, **SUPERGRAFX (JP)** ou **TURBOGRAFX-16 (US)**. Par défaut, le core choisit d'après le jeu.     |
| core geargrafx                           | **RENDU VISUEL > PALETTE**                  | **STANDARD RGB**, **TURBOXRAY** ou **KITRINX**.                                                                    |
| Mesen                                    | **ÉMULATION > TYPE DE CONSOLE**             | Même choix que geargrafx.                                                                                          |
| cores mednafen\_pce, mednafen\_pce\_fast | **TURBO**                                   | Tir automatique de RetroArch.                                                                                      |

## Problèmes connus

<table><thead><tr><th width="351.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le joueur 2 ne répond pas</td><td>Le multitap est nécessaire : voir <a href="pc-engine-turbografx-16.md#jouer-a-plusieurs-multitap"><strong>Jouer à plusieurs (multitap)</strong></a>. Vérifiez qu'il n'a pas été désactivé dans les options. ares n'émule qu'un joueur.</td></tr><tr><td>Les boutons III à VI ne répondent pas</td><td>Activez la manette 6 boutons : voir <a href="pc-engine-turbografx-16.md#manette-6-boutons"><strong>Manette 6 boutons</strong></a>.</td></tr><tr><td>Un jeu ne démarre pas avec FBNeo</td><td>FBNeo ne lit que les archives nommées comme ses sets PC Engine. Utilisez un autre core.</td></tr><tr><td>Un jeu SuperGrafx a des graphismes cassés</td><td>mednafen_pce_fast n'émule pas la SuperGrafx : rangez le jeu dans <code>roms\supergrafx</code>.</td></tr><tr><td>Un jeu sur CD ne démarre pas</td><td>Les jeux CD se rangent dans <code>roms\pcenginecd</code>.</td></tr></tbody></table>



