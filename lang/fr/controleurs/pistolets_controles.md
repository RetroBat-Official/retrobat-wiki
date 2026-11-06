---
description: Bang Bang !
---

# Contrôle des pistolets

Cette page liste les systèmes et émulateurs dans lesquels RetroBat configure les pistolets, et le mappage des boutons. Pour brancher un pistolet, l'activer et régler les options communes, voir [Pistolets](supported-controllers/lightguns/).

## Comment RetroBat configure un pistolet

Un pistolet fonctionne comme une souris (visée et boutons), souvent avec un clavier pour ses boutons supplémentaires. Dans chaque émulateur, RetroBat les affecte au pistolet émulé selon la même logique :

<table><thead><tr><th width="386.5">Bouton du pistolet</th><th>Mappage par défaut</th></tr></thead><tbody><tr><td>Gâchette</td><td>Clic gauche</td></tr><tr><td>Deuxième bouton (recharge, A, curseur…, selon le pistolet)</td><td>Clic droit</td></tr><tr><td>Troisième bouton</td><td>Clic milieu</td></tr><tr><td>Start</td><td>Touche 1 (J1), 2 (J2), 3 (J3), 4 (J4)</td></tr><tr><td>Crédit / Select</td><td>Touche 5 (J1), 6 (J2), 7 (J3), 8 (J4)</td></tr></tbody></table>

* **Recharge** : dans la plupart des jeux, on recharge en tirant hors de l'écran. Si votre pistolet ne peut pas tirer hors de l'écran, activez **BOUTON POUR RECHARGER**.
* **INVERSER GÂCHETTE ET RECHARGE** inverse les clics gauche et droit (ex. Wii Zapper).
* **Wiimote avec DolphinBar** : les boutons envoient d'autres touches, RetroBat adapte le mappage (croix droite = Start, croix gauche = Crédit). Voir [Wiimote & DolphinBar](supported-controllers/lightguns/wiimotedolphinbar.md).
* **RetroArch** : les boutons de votre manette restent aussi affectés aux boutons du pistolet (Start, Select, boutons auxiliaires, croix), vous pouvez donc utiliser une manette en plus du pistolet.

## Activer les pistolets

Pour les jeux de tir, les pistolets sont activés automatiquement (voir [Pistolets](supported-controllers/lightguns/)). Exceptions :

* **RPCS3** : choisissez le type de pistolet avec **ACTIVER LES PISTOLETS** (**SOURIS BRUTE** pour le GunCon 3, **PS EYE** pour les jeux PlayStation Move). Il n'est jamais activé automatiquement.
* **Hypseus** et **Singe 2** : le pistolet fonctionne toujours comme une souris, il n'y a pas d'option à activer.
* **Wii** : les Wiimotes sont utilisées comme de vraies Wiimotes, voir la page [Wii](../systemes-and-emulateurs/supported-game-systems/consoles-de-jeu/nintendo-consoles-de-jeu/wii.md).

## Systèmes et émulateurs compatibles

La colonne **Pistolets** donne le nombre de pistolets que RetroBat peut configurer en même temps. Le jeu doit aussi gérer plusieurs joueurs.

| Système                       | Émulateur                                              | Pistolets                 | Remarques                                                                   |
| ----------------------------- | ------------------------------------------------------ | ------------------------- | --------------------------------------------------------------------------- |
| Arcade                        | lr-fbneo                                               | Jusqu'à 4                 |                                                                             |
|                               | lr-mame, lr-mame2003\_plus, lr-mame2016                | Jusqu'à 4                 |                                                                             |
|                               | MAME (mame64, groovymame)                              | Jusqu'à 4                 |                                                                             |
| 3DO                           | lr-opera                                               | Jusqu'à 4                 |                                                                             |
| ActionMax, Daphne, Singe      | hypseus                                                | Plusieurs                 | Une souris par pistolet (sauf avec **UN SEUL PISTOLET**)                    |
|                               | singe2                                                 | 1                         |                                                                             |
| Amiga                         | amiberry                                               | 2                         | Crayon optique ou Trojan Phazer (**TYPE DE PISTOLET**)                      |
| Amstrad CPC, GX4000           | lr-cap32                                               | Jusqu'à 4                 | Phaser ou Gunstick (**LIGHTGUN MODE**)                                      |
| Atari 2600                    | lr-stella                                              | Jusqu'à 4                 |                                                                             |
| Atomiswave, Naomi, Naomi 2    | lr-flycast                                             | Jusqu'à 4                 |                                                                             |
|                               | flycast                                                | 2 (4 avec DemulShooter)   |                                                                             |
|                               | demul                                                  | 1 (2 avec DemulShooter)   |                                                                             |
| Commodore 64                  | lr-vice                                                | 1                         |                                                                             |
| Dreamcast                     | lr-flycast                                             | Jusqu'à 4                 |                                                                             |
|                               | flycast                                                | 2 (4 avec DemulShooter)   |                                                                             |
|                               | demul                                                  | 1 (2 avec DemulShooter)   |                                                                             |
| Lindbergh                     | linuxloader                                            | 1 (4 avec DemulShooter)   |                                                                             |
|                               | teknoparrot                                            | Jusqu'à 4                 |                                                                             |
| Master System                 | lr-genesis\_plus\_gx, lr-genesis\_plus\_gx\_wide       | Jusqu'à 4                 |                                                                             |
|                               | lr-gearsystem                                          | Jusqu'à 4                 |                                                                             |
|                               | mesen                                                  | 1                         |                                                                             |
|                               | bizhawk (SMSHawk)                                      | 1                         |                                                                             |
| Mega Drive / Genesis, Mega-CD | lr-genesis\_plus\_gx, lr-genesis\_plus\_gx\_wide       | 1                         | Menacer ou Justifier (**TYPE DE PISTOLET**)                                 |
| Model 2                       | m2emulator                                             | 2                         | DemulShooter démarre automatiquement avec 2 pistolets                       |
| Model 3                       | supermodel                                             | 2                         | 2 pistolets nécessitent **MULTI-PISTOLETS (RAW INPUT)** (activé par défaut) |
|                               | lr-supermodel                                          | Jusqu'à 4                 |                                                                             |
| Namco System 246/256          | pcsx2x6                                                | 2                         |                                                                             |
|                               | teknoparrot                                            | Jusqu'à 4                 |                                                                             |
| NES / Famicom                 | lr-fceumm, lr-mesen, lr-nestopia                       | 1                         |                                                                             |
|                               | mesen, mednafen, jgenesis, bizhawk (NesHawk)           | 1                         |                                                                             |
| PlayStation                   | lr-mednafen\_psx\_hw, lr-pcsx\_rearmed, lr-swanstation | Jusqu'à 4                 | GunCon ou Justifier (**TYPE DE PISTOLET**, lr-mednafen\_psx\_hw)            |
|                               | duckstation                                            | 2                         |                                                                             |
|                               | mednafen                                               | 1                         |                                                                             |
| PlayStation 2                 | pcsx2                                                  | 1                         |                                                                             |
| PlayStation 3                 | rpcs3                                                  | 2 (GunCon 3), 1 (PS Move) |                                                                             |
| PSX Arcade                    | arcadeduck                                             | Plusieurs                 |                                                                             |
| Saturn                        | lr-kronos, lr-mednafen\_saturn, lr-ymir                | Jusqu'à 4                 |                                                                             |
|                               | kronos, mednafen, bizhawk (Saturnus)                   | 1                         |                                                                             |
| Sega Chihiro                  | xemu-chihiro                                           | 2                         |                                                                             |
|                               | cxbx, chihiro, chihiro-gun                             | 1 (2 avec DemulShooter)   |                                                                             |
|                               | teknoparrot                                            | Jusqu'à 4                 |                                                                             |
| Super Nintendo                | lr-snes9x                                              | 1 (2 avec Justifiers)     | Superscope, Justifier, M.A.C.S. Rifle ou Justifiers (**TYPE DE PISTOLET**)  |
|                               | lr-bsnes, lr-bsnes-jg, lr-mesen-s                      | 1                         |                                                                             |
|                               | snes9x                                                 | 1 (2 avec 2 Justifiers)   |                                                                             |
|                               | mesen, mednafen, jgenesis, bizhawk (BSNES, Snes9x)     | 1                         |                                                                             |
| TeknoParrot                   | teknoparrot                                            | Jusqu'à 4                 |                                                                             |
| Wii                           | dolphin                                                | 1                         |                                                                             |
| Windows                       | Jeux compatibles DemulShooter                          | Jusqu'à 4                 | DemulShooter démarre automatiquement à partir de 2 pistolets                |
| Xbox                          | cxbx                                                   | 1                         |                                                                             |

### DemulShooter

DemulShooter ajoute la gestion de plusieurs pistolets (et des sorties comme le recul) aux jeux et émulateurs qui ne savent pas gérer plusieurs pistolets seuls. Il est fourni avec RetroBat dans `system\tools\demulshooter`.

* **Model 2 (m2emulator)** et **jeux Windows** : DemulShooter démarre automatiquement quand 2 pistolets ou plus sont branchés. Réglez **UTILISER DEMULSHOOTER** sur **NON** pour le désactiver.
* **Flycast, Demul, TeknoParrot, Linuxloader, Chihiro (Cxbx)** : réglez **UTILISER DEMULSHOOTER** sur **OUI** dans les options **PISTOLETS** du système ou du jeu.

Pour les sorties (recul, lumières) avec MAME, Flycast, Demul, Model 2, Supermodel, TeknoParrot et les jeux Windows, voir aussi l'option **UTILISER MAMEHOOKER**.

## Mappage des boutons par émulateur

### RetroArch

<table><thead><tr><th width="390.25">Cores</th><th>Clic gauche</th><th>Clic droit</th><th>Clic milieu</th></tr></thead><tbody><tr><td>lr-cap32, lr-fceumm, lr-kronos, lr-mame, lr-mame2003_plus, lr-mame2016, lr-mednafen_saturn, lr-mesen, lr-opera, lr-stella, lr-supermodel, lr-vice, lr-ymir</td><td>Gâchette</td><td>Recharge</td><td>Start</td></tr><tr><td>lr-bsnes, lr-bsnes-jg, lr-gearsystem, lr-genesis_plus_gx, lr-genesis_plus_gx_wide, lr-mednafen_psx_hw, lr-mesen-s, lr-pcsx_rearmed, lr-snes9x, lr-swanstation</td><td>Gâchette</td><td>Aux A</td><td>Aux B</td></tr><tr><td>lr-fbneo, lr-flycast</td><td>Gâchette</td><td>Aux A</td><td>Start</td></tr><tr><td>lr-nestopia</td><td>Gâchette</td><td>Aux B</td><td>–</td></tr></tbody></table>

* Clavier (joueur 1) : Start = **1**, Select = **5**, croix = flèches. Joueur 2 : **2** / **6**, etc.
* **BOUTON POUR RECHARGER** : la recharge passe sur le clic droit, et le bouton du clic droit passe sur le clic milieu.
* **MAPPING DES BOUTONS A/B** > **MANETTE GAUCHE/DROITE** : Aux A et Aux B sur les flèches gauche et droite (croix d'une Wiimote).

### Autres émulateurs

<table><thead><tr><th width="214">Émulateur</th><th>Mappage</th></tr></thead><tbody><tr><td>MAME (mame64, groovymame)</td><td>Bouton 1 : clic gauche, Bouton 2 : clic droit, Bouton 3 : clic milieu. Start : 1 à 4, Crédit : 5 à 8</td></tr><tr><td>flycast</td><td>Gâchette : clic gauche, Recharge : clic droit, Start : clic milieu. Certains jeux Naomi/Atomiswave utilisent d'autres boutons (fichier <code>flycast_Arcade.yml</code>, option <strong>MAPPING DE LA SOURIS</strong>)</td></tr><tr><td>demul</td><td>Mappage de l'émulateur</td></tr><tr><td>m2emulator</td><td>Voir <a href="configuration-des-touches-specifique-par-emulateur/configuration-des-touches-model2.md">Configuration des touches Model 2</a></td></tr><tr><td>supermodel</td><td>Gâchette : clic gauche, Tir hors écran (recharge) : clic droit</td></tr><tr><td>teknoparrot</td><td>Par jeu, dans le fichier <code>teknoparrot.yml</code> (voir plus bas)</td></tr><tr><td>linuxloader</td><td>Gâchette : clic gauche, Recharge : clic droit, Bouton du pistolet : clic milieu, Action : touche 1. À modifier avec <strong>MAPPING DU RECHARGEMENT</strong>, <strong>MAPPING DU BOUTON DU PISTOLET</strong> et <strong>MAPPING DU BOUTON D'ACTION</strong></td></tr><tr><td>xemu-chihiro</td><td>Gâchette : clic gauche, deuxième bouton : clic droit, troisième bouton : clic milieu, recharge en tirant hors de l'écran. Start : 1 / 2, Crédit : 5 / 6</td></tr><tr><td>cxbx (Xbox, Chihiro)</td><td>Gâchette : clic gauche, Grip : clic droit, A : S, B : D, Start : 1, Back : 5</td></tr><tr><td>arcadeduck</td><td>Gâchette : clic gauche, Recharge : clic droit</td></tr><tr><td>pcsx2 (PS2)</td><td>Gâchette : clic gauche, Tir hors écran : clic droit, Recalibrage : clic milieu, A : 1, B : 2, C : 3, Start : Entrée, Select : Retour arrière. À modifier avec <strong>MAPPING DES BOUTONS GUNCON</strong> et <strong>BOUTON DE CALIBRATION</strong></td></tr><tr><td>pcsx2x6 (Namco 246/256)</td><td>Gâchette : clic gauche, A : clic droit, Start : 1 / 2, Crédit : 5 / 6</td></tr><tr><td>rpcs3</td><td>GunCon 3 : Gâchette : clic gauche. PS Move (PS EYE) : mappage souris standard de RPCS3 ; le clic milieu est nécessaire pour passer l'écran de calibration (R1 peut aussi être utilisé)</td></tr><tr><td>duckstation</td><td>Gâchette : clic gauche, A : clic droit, B : clic milieu, Tir hors écran : 1 (J1) / 2 (J2). A/B à modifier avec <strong>MAPPING DES BOUTONS A/B</strong></td></tr><tr><td>mednafen</td><td>NES Zapper : Gâchette : clic gauche, Tir loin : clic droit. PSX GunCon : Gâchette : clic gauche, A : clic droit, B : clic milieu, Tir hors écran : Espace. PSX Justifier : Gâchette : clic gauche, O : clic droit, Start : clic milieu, Tir hors écran : Espace. SNES Super Scope : Gâchette : clic gauche, Curseur : clic droit, Turbo : clic milieu, Tir hors écran : Espace. Saturn : Gâchette : clic gauche, Tir hors écran : clic droit, Start : clic milieu</td></tr><tr><td>mesen</td><td>NES Zapper et SMS Light Phaser : Tir : clic gauche, Tir hors écran : clic droit. SNES Super Scope : Tir : clic gauche, Curseur : clic droit, Turbo : clic milieu</td></tr><tr><td>jgenesis</td><td>NES Zapper : Tir : clic gauche, Tir hors écran : clic droit. SNES Super Scope : Tir : clic gauche, Curseur : clic droit, Pause : clic milieu</td></tr><tr><td>bizhawk</td><td>NES Zapper et SMS Light Phaser : Gâchette : clic gauche. SNES Super Scope : Gâchette : clic gauche, Curseur : clic milieu, Turbo : clic droit. Saturn : Gâchette : clic gauche, Tir hors écran : clic droit, Start : clic milieu</td></tr><tr><td>snes9x</td><td>Mappage de l'émulateur pour le Super Scope / Justifier</td></tr><tr><td>kronos</td><td>Gâchette : clic gauche, Start : clic droit</td></tr><tr><td>amiberry</td><td>Bouton du crayon optique : clic gauche</td></tr><tr><td>dolphin (Wii)</td><td>B : clic gauche, A : clic droit, Secouer : clic milieu, 1 : touche 1, 2 : touche 5, + : Entrée, − : Retour arrière. Certains jeux utilisent un autre mappage, défini dans <code>gamesdb.xml</code></td></tr></tbody></table>

### Fichier de mappage TeknoParrot

Le mappage pistolet de chaque jeu TeknoParrot est défini dans `system\resources\inputmapping\teknoparrot.yml`. Pour le modifier, copiez le fichier dans `user\inputmapping\teknoparrot.yml` et modifiez la copie : elle est lue en priorité et n'est pas écrasée par les mises à jour de RetroBat.

Dans ce fichier, les boutons du pistolet sont déclarés avec `mouseleft`, `mousemiddle`, `mouseright`, `button4`, `button5`, et les touches du clavier avec `kb_` suivi de la touche (ex. `kb_5`).
