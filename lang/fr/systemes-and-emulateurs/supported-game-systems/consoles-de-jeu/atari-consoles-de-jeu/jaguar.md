---
description: Atari
---

# Jaguar

<div align="left"><figure><img src="../../../../.gitbook/assets/image (546).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **Jaguar** est la dernière console d'Atari. Elle sort fin 1993 aux États-Unis, puis en 1994 en Europe et au Japon, et Atari la présente comme la première console « 64 bits ». Sa manette se reconnaît tout de suite : trois boutons d'action et un pavé de douze touches, sur lequel on glisse un cache en plastique propre à chaque jeu.

La machine est puissante mais difficile à programmer, et les éditeurs la délaissent vite au profit de la PlayStation et de la Saturn. Elle ne compte qu'une cinquantaine de jeux en cartouche, dont Tempest 2000, Alien vs Predator, Iron Soldier, Doom et Rayman, et se vend à moins de 250 000 exemplaires. Un lecteur de CD sort en 1995 (voir la page [**Jaguar CD**](jaguarcd.md)), puis Atari arrête les consoles en 1996.

{% embed url="https://fr.wikipedia.org/wiki/Jaguar_(console_de_jeux_vid%C3%A9o)" %}

## En bref

<table><thead><tr><th width="247.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\jaguar</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .cue .cdi .j64 .jag .rom .abs .cof .bin .prg .squashfs</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: virtualjaguar</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun obligatoire</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BigPEmu, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>[BIOS] Atari Jaguar (World).j64</code> (nécessaire à Phoenix)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="164">Émulateur</th><th width="164.25">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: virtualjaguar</strong> (défaut)</td><td>Tout le monde</td><td>Intégré à RetroArch : shaders, décorations, RetroAchievements, jeu en réseau. Résolution doublée, overclocking, Team Tap, manette Jaguar Pro.</td><td>Quelques jeux exigeants tournent mieux avec BigPEmu.</td></tr><tr><td><strong>bigpemu</strong></td><td>Ceux qui veulent la meilleure compatibilité</td><td>Très bonne compatibilité, sauvegardes instantanées, retour en arrière, jusqu'à 8 joueurs, tout le pavé numérique sur la manette.</td><td>Pas de RetroAchievements. Raccourcis sur L2 au lieu du bouton HOTKEY.</td></tr><tr><td><strong>bizhawk</strong> (Jaguar)</td><td>Speedrun assisté (TAS)</td><td>Outils d'enregistrement et d'analyse, RetroAchievements.</td><td>Peu d'options dans RetroBat.</td></tr><tr><td><strong>phoenix</strong></td><td>En dépannage</td><td>Une alternative quand les autres ne conviennent pas.</td><td>Demande le BIOS, pas de sauvegardes instantanées, un seul raccourci (quitter).</td></tr></tbody></table>

**En cas de doute, gardez libretro: virtualjaguar, et essayez BigPEmu si un jeu pose problème.**

## BIOS

Seul Phoenix a besoin d'un fichier BIOS. Les autres émulateurs l'intègrent ou s'en passent.

<table><thead><tr><th width="292.75">Fichier</th><th>MD5</th><th width="122.75">Emplacement</th><th width="97">Émulateur</th></tr></thead><tbody><tr><td><code>[BIOS] Atari Jaguar (World).j64</code></td><td><code>bcfe348c565d9dedb173822ee6850dea</code></td><td><code>bios</code></td><td>Phoenix</td></tr></tbody></table>

Avec libretro: virtualjaguar, l'option **ÉMULATION > DÉMARRER DEPUIS LE BIOS** affiche l'écran de démarrage de la console, que certains jeux exigent. Aucun fichier n'est à ajouter : le BIOS est inclus dans le core.

## Quel format de jeu ?

<table><thead><tr><th width="196.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.j64, .jag, .rom, .bin</strong></td><td>Copies de cartouches, le format courant.</td></tr><tr><td>.abs, .cof, .prg</td><td>Programmes amateurs (homebrew).</td></tr><tr><td>.zip, .7z</td><td>Le jeu compressé, accepté par tous les émulateurs.</td></tr><tr><td>.squashfs</td><td>BigPEmu uniquement.</td></tr><tr><td>.cue, .cdi</td><td>Jeux Jaguar CD : rangez-les plutôt dans <code>roms\jaguarcd</code> (voir la page <a href="jaguarcd.md"><strong>Jaguar CD</strong></a>).</td></tr></tbody></table>

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour tous les émulateurs. Les trois boutons d'action sont aux mêmes endroits partout ; le pavé numérique, lui, dépend de l'émulateur.

| Manette Jaguar | libretro: virtualjaguar, BizHawk | libretro avec **MAPPER LA MANETTE JAGUAR PRO** | BigPEmu                     |
| -------------- | -------------------------------- | ---------------------------------------------- | --------------------------- |
| A              | EST                              | EST                                            | EST                         |
| B              | SUD                              | SUD                                            | SUD                         |
| C              | OUEST                            | OUEST                                          | OUEST                       |
| Pause          | SELECT                           | SELECT                                         | SELECT                      |
| Option         | START                            | START                                          | START                       |
| 0              | NORD                             | Stick droit vers le bas                        | Stick droit vers le bas     |
| 1              | L1                               | Stick gauche vers la gauche                    | L1                          |
| 2              | R1                               | Stick gauche vers le haut                      | Stick gauche vers le haut   |
| 3              | L2                               | Stick gauche vers la droite                    | R1                          |
| 4              | R2                               | L2                                             | Stick gauche vers la gauche |
| 5              | L3                               | Stick droit vers le haut                       | Stick droit vers le haut    |
| 6              | R3                               | R2                                             | Stick gauche vers la droite |
| 7              | —                                | L1                                             | Stick droit vers la gauche  |
| 8              | —                                | NORD                                           | Stick gauche vers le bas    |
| 9              | —                                | R1                                             | Stick droit vers la droite  |
| \*             | —                                | L3                                             | L3                          |
| #              | —                                | R3                                             | R3                          |

| Libretro : VirtualJaguar                           | BigPEmu                                            |
| -------------------------------------------------- | -------------------------------------------------- |
| ![](<../../../../.gitbook/assets/image (547).png>) | ![](<../../../../.gitbook/assets/image (548).png>) |

Sur la manette Jaguar Pro, les boutons X, Y, Z, L et R doublent les touches 7, 8, 9, 4 et 6 : l'option **MAPPER LA MANETTE JAGUAR PRO** les place donc sur L1, NORD, R1, L2 et R2.

Options utiles, dans **CONTRÔLES** :

| Option                                  | Émulateur               | Effet                                                                                                              |
| --------------------------------------- | ----------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **TYPE DE CONTRÔLEUR JOUEUR 1** / **2** | libretro: virtualjaguar | Team Tap (3 ou 4 joueurs), contrôleur rotatif à la souris (Tempest 2000), souris, stick analogique (BattleSphere). |
| **ACTIVER LE MULTITAP**                 | BigPEmu                 | Team Tap sur le port 1, le port 2 ou les deux : jusqu'à 5 ou 8 manettes.                                           |
| **UTILISER LE STICK GAUCHE**            | BigPEmu                 | Le stick gauche remplace la croix directionnelle.                                                                  |

### Raccourcis

Avec BigPEmu, les raccourcis se font avec **L2** à la place du bouton HOTKEY, sauf pour quitter.

Libretro : virtualjaguar utilise les [raccourcis standard RetroArch](../../../../navigation/hotkeys.md).

| Action                          | BigPEmu        | BizHawk             | Clavier (BigPEmu, BizHawk) |
| ------------------------------- | -------------- | ------------------- | -------------------------- |
| **Quitter**                     | HOTKEY + START | HOTKEY + START      | ÉCHAP (BizHawk)            |
| Sauvegarde instantanée          | L2 + OUEST     | HOTKEY + OUEST      | F2                         |
| Chargement instantané           | L2 + NORD      | HOTKEY + NORD       | F4                         |
| Emplacement suivant / précédent | —              | HOTKEY + HAUT / BAS | F7 / F6 (BizHawk)          |
| Capture d'écran                 | L2 + R3        | HOTKEY + R3         | F8                         |
| Retour en arrière               | L2 + GAUCHE    | HOTKEY + GAUCHE     | RETOUR ARRIÈRE             |
| Avance rapide                   | L2 + DROITE    | HOTKEY + DROITE     | L                          |
| Menu de l'émulateur             | L2 + SUD       | —                   | F1 (BigPEmu)               |
| Pause                           | —              | HOTKEY + SUD        | P (BizHawk)                |
| Plein écran                     | —              | HOTKEY + L3         | F (BizHawk)                |

Phoenix n'a qu'un raccourci : **HOTKEY + START** pour quitter.

## Dossiers

<table><thead><tr><th width="361.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS (Phoenix)</td><td><code>bios</code></td></tr><tr><td>Sauvegardes des cores libretro</td><td><code>saves\jaguar</code></td></tr><tr><td>Sauvegardes de BizHawk</td><td><code>saves\jaguar\bizhawk</code></td></tr><tr><td>Sauvegardes instantanées des cores libretro</td><td><code>saves\jaguar\libretro.virtualjaguar</code></td></tr><tr><td>Sauvegardes instantanées de BigPEmu</td><td><code>saves\jaguar\bigpemu</code></td></tr><tr><td>Sauvegardes instantanées de BizHawk</td><td><code>saves\jaguar\bizhawk\sstates\Jaguar</code></td></tr><tr><td>Configuration et données de BigPEmu</td><td><code>emulators\bigpemu\userdata</code></td></tr><tr><td>Configuration de Phoenix</td><td><code>emulators\phoenix\phoenix.config.xml</code></td></tr><tr><td>Captures d'écran des cores libretro</td><td><code>screenshots</code></td></tr><tr><td>Captures d'écran de BizHawk</td><td><code>screenshots\bizhawk\jaguar</code></td></tr><tr><td>Codes de triche des cores libretro</td><td><code>cheats\retroarch</code></td></tr><tr><td>Codes de triche de BizHawk</td><td><code>cheats\bizhawk\jaguar</code></td></tr></tbody></table>

## Guides

### Jouer à 3 ou 4 avec le Team Tap

Quelques jeux acceptent plus de deux joueurs grâce à l'adaptateur Team Tap, par exemple White Men Can't Jump et NBA Jam Tournament Edition.

* **libretro: virtualjaguar** : réglez **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** sur **TEAM TAP**.
* **BigPEmu** : réglez **CONTRÔLES > ACTIVER LE MULTITAP** sur **SUR LE PORT 1**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (549).png" alt=""><figcaption></figcaption></figure></div>

### Tempest 2000 avec le contrôleur rotatif

Tempest 2000 se joue au mieux avec un contrôleur rotatif. Avec libretro: virtualjaguar, réglez **TYPE DE CONTRÔLEUR JOUEUR 1** sur **ROTATIF (SOURIS)** : la souris fait tourner le vaisseau.

### Régler BigPEmu directement

Pour accéder aux réglages que RetroBat ne propose pas, ouvrez BigPEmu depuis le système **RetroBat** de la liste des systèmes, ou lancez `emulators\bigpemu\Configure BigPEmu.bat`. Les réglages vidéo et les manettes sont réécrits par RetroBat à chaque lancement de jeu.

En jeu, **L2 + SUD** ouvre le menu de BigPEmu.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (550).png" alt=""><figcaption></figcaption></figure></div>

### Effets vidéo de BigPEmu

L'option **RENDU VISUEL > EFFET VIDÉO** applique un des filtres intégrés à BigPEmu (lignes de balayage, CRT…). Elle n'a d'effet que si aucun shader RetroBat n'est sélectionné.

Pour désactiver les shaders de RetroBat pour ce système, voir la page [**Configuration des systèmes et des jeux**](../../../../navigation/configuration-des-systemes-et-des-jeux.md).

## Problèmes connus

<table><thead><tr><th width="315.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Phoenix ne lance pas le jeu</td><td>Placez <code>[BIOS] Atari Jaguar (World).j64</code> dans <code>bios</code>.</td></tr><tr><td>Un jeu est lent ou affiche des défauts avec libretro: virtualjaguar</td><td>Essayez BigPEmu. Sur un PC modeste, l'option <strong>BLITTER RAPIDE</strong> accélère le core, au prix d'une moins bonne compatibilité.</td></tr><tr><td>Les raccourcis ne répondent pas avec BigPEmu</td><td>Ils se font avec <strong>L2</strong>, pas avec le bouton HOTKEY. Une manette sans gâchette L2 n'a donc pas de raccourcis.</td></tr><tr><td>Un jeu demande les touches 7, 8 ou 9</td><td>Avec libretro: virtualjaguar, activez <strong>MAPPER LA MANETTE JAGUAR PRO</strong>, ou utilisez BigPEmu qui place tout le pavé sur la manette.</td></tr><tr><td>Un fichier <code>.squashfs</code> ne se lance pas</td><td>Ce format n'est lu que par BigPEmu.</td></tr><tr><td>Un jeu prévu pour l'Europe ne tourne pas à la bonne vitesse</td><td>Activez <strong>MODE PAL</strong> (libretro: virtualjaguar, BigPEmu) ou <strong>FORCER PAL</strong> (BizHawk).</td></tr><tr><td><strong>EFFET VIDÉO</strong> ne change rien dans BigPEmu</td><td>Désactivez les shaders de RetroBat pour ce système.</td></tr></tbody></table>
