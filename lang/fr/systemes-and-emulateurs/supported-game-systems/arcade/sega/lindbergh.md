---
description: Sega
---

# Lindbergh

<div align="left"><img src="https://images.gitbook.com/__img/dpr=2,width=760,onerror=redirect,format=auto,signature=1065403660/https%3A%2F%2Fraw.githubusercontent.com%2FRetroBat-Official%2Fes-theme-carbon%2F801d816fdf5f7286d8b717acd351964eda457a71%2Fart%2Flogos%2Flindbergh.svg" alt="" height="67" width="300"></div>

## Présentation

La **Lindbergh** est une carte d'arcade de Sega, sortie en 2005. C'est un véritable PC (processeur Intel Pentium 4 puis Celeron, carte graphique NVIDIA GeForce) qui fait tourner ses jeux sous Linux. Elle remplace la Naomi 2 et le Chihiro chez Sega, et reçoit une trentaine de jeux jusqu'en 2010.

Parmi ses jeux : **The House of the Dead 4** (et Special, EX), **Virtua Fighter 5**, **Outrun 2 SP SDX**, **Initial D Arcade Stage 4** et **5**, **After Burner Climax**, **Virtua Tennis 3**, **Let's Go Jungle!**, **2 Spicy**, **Ghost Squad Evolution**, **Rambo**, **Primeval Hunt**, **Sega Race TV**, **R-Tuned**, **Hummer**, **Harley-Davidson: King of the Road**.

RetroBat propose deux émulateurs : **Linuxloader** (par défaut), qui lance les programmes Linux des jeux sous Windows, et **TeknoParrot**.

{% embed url="https://fr.wikipedia.org/wiki/Lindbergh_(syst%C3%A8me_d'arcade)" %}

## En bref

<table><thead><tr><th width="269"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\lindbergh</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>linuxloader</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs (mappage par type de jeu pour Linuxloader)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>Linuxloader (1 pistolet, 4 avec DemulShooter), TeknoParrot</td></tr><tr><td><strong>Volants</strong></td><td>Linuxloader, TeknoParrot</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="150.75">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>linuxloader</strong> (défaut)</td><td>Lance les jeux directement, sans profil à installer. Manettes, volants et pistolets configurés automatiquement, dispositions arcade, bordure blanche pour les pistolets Sinden, corrections propres à certains jeux.</td><td>Un seul pistolet sans DemulShooter.</td></tr><tr><td><strong>teknoparrot</strong></td><td>Interface et profils de TeknoParrot, nombreux jeux d'autres cartes.</td><td>Demande un profil TeknoParrot pour chaque jeu (voir la page <a href="../teknoparrot.md"><strong>TeknoParrot</strong></a>).</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire : les jeux Lindbergh contiennent tout ce dont ils ont besoin.

## Quel format de jeu ?

Un jeu Lindbergh est un dossier, qui contient le plus souvent un dossier `disk0`. RetroBat le reconnaît de deux façons :

<table><thead><tr><th width="142.75">Méthode</th><th>Comment faire</th></tr></thead><tbody><tr><td><strong>Dossier <code>.game</code></strong></td><td>Renommez le dossier du jeu avec l'extension <code>.game</code> (par exemple <code>hotd4.game</code>). RetroBat cherche le programme du jeu dans <code>disk0</code> s'il existe, sinon directement dans le dossier, et dans le bon sous-dossier pour les jeux connus (voir ci-dessous).</td></tr><tr><td><strong>Fichier <code>.game</code></strong></td><td>Créez un fichier vide avec l'extension <code>.game</code> (par exemple <code>hummerxt.game</code>) à côté du programme du jeu (le fichier <code>elf</code>). Le dossier du jeu ne doit pas porter l'extension <code>.game</code>.</td></tr></tbody></table>

<table><thead><tr><th width="450.25">Exemple</th><th>Explication</th></tr></thead><tbody><tr><td>roms\lindbergh\hotd4.game\disk0\elf\hod4M.elf</td><td>dossier .game avec disk0</td></tr><tr><td>roms\lindbergh\hummerxt.game\hummer_master.elf</td><td>dossier .game sans disk0</td></tr><tr><td>roms\lindbergh\hummerxt\hummerxt.game</td><td>fichier .game à côté du fichier elf</td></tr></tbody></table>

Donnez au dossier ou au fichier `.game` le nom court du jeu : il permet à DemulShooter de reconnaître le jeu et, pour un dossier, à RetroBat de trouver le programme quand il est dans un sous-dossier (par exemple `disk0\elf`).

<details>

<summary>Noms de jeux reconnus</summary>

| Jeu                                           | Nom du dossier      |
| --------------------------------------------- | ------------------- |
| 2 Spicy                                       | `2spicy`            |
| After Burner Climax (SDX)                     | `abclisdx`          |
| Ghost Squad Evolution                         | `gsevo`             |
| Harley-Davidson: King of the Road             | `hdkotr`            |
| The House of the Dead 4 (Rev A)               | `hotd4`             |
| The House of the Dead 4 Special               | `hotd4sp`           |
| The House of the Dead EX                      | `hotdex`            |
| Hummer                                        | `hummer`            |
| Hummer Extreme Edition                        | `hummerxt`          |
| Initial D Arcade Stage 4 (Rev B)              | `initiad4b`         |
| Initial D 4 Export (Rev D)                    | `initiad4ex`        |
| Initial D 5 Export (2.0)                      | `initiad5exa`       |
| Let's Go Jungle!                              | `lgj`               |
| Let's Go Jungle! Special                      | `lgjsp`             |
| Outrun 2 SP SDX (Rev A)                       | `outr2sdx`          |
| Outrun 2 SP SDX (bootleg)                     | `outr2sdxg`         |
| Primeval Hunt                                 | `primevah`          |
| R-Tuned: Ultimate Street Racing               | `rtuned`            |
| Rambo (Export)                                | `rambo`             |
| Sega Race TV (Export)                         | `segartv`           |
| Virtua Fighter 5                              | `vf5`               |
| Virtua Fighter 5 (Rev E, ver C)               | `vf5e`              |
| Virtua Fighter 5 Final Showdown (Rev A, v2.0) | `vf5fsa2`           |
| Virtua Fighter 5 R (Rev G)                    | `vf5r`              |
| Virtua Tennis 3 (Rev C)                       | `vt3` ou `vtennis3` |

</details>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (635).png" alt=""><figcaption></figcaption></figure></div>

## Contrôles

### Configuration automatique (Linuxloader)

RetroBat écrit le fichier `controls.ini` de Linuxloader à chaque lancement, pour 2 joueurs (jeux à boutons) ou 1 joueur (conduite, vol). La position des boutons vient de `linuxloader.yml`, avec une section par type de jeu.

**Commandes communes**

<table><thead><tr><th width="157">Borne</th><th width="242.5">Manette</th><th>Clavier</th></tr></thead><tbody><tr><td>Start</td><td>START</td><td><code>1</code> / <code>2</code></td></tr><tr><td>Crédit</td><td>SELECT</td><td><code>5</code> / <code>6</code></td></tr><tr><td>Test</td><td>R3 (avec <strong>MODE TEST</strong>)</td><td><code>0</code></td></tr><tr><td>Service</td><td>L3 (avec <strong>MODE TEST</strong>)</td><td><code>9</code></td></tr><tr><td>Quitter le jeu</td><td>START + SELECT</td><td>Échap</td></tr></tbody></table>

**Jeux à boutons** (Virtua Fighter 5, Virtua Tennis 3…)

| Borne      | Manette             | Clavier joueur 1 | Clavier joueur 2 |
| ---------- | ------------------- | ---------------- | ---------------- |
| Directions | Croix, stick gauche | Flèches          | `R` `F` `D` `G`  |
| Bouton 1   | SUD                 | Ctrl gauche      | `A`              |
| Bouton 2   | EST                 | Alt gauche       | `S`              |
| Bouton 3   | OUEST               | Espace           | `Q`              |
| Carte      | GUIDE               | `F7`             | `F8`             |

**Jeux de conduite** (Outrun 2, Initial D, Sega Race TV…)

| Borne                           | Manette      | Clavier                  |
| ------------------------------- | ------------ | ------------------------ |
| Volant                          | Stick gauche | Flèches gauche / droite  |
| Accélérateur / frein            | R2 / L2      | Flèches haut / bas       |
| Changement de vue               | NORD         | Maj gauche               |
| Boost / boost droit             | SUD / EST    | Ctrl gauche / Alt gauche |
| Vitesse supérieure / inférieure | R1 / L1      | `X` / `Z`                |
| Changement de musique           | OUEST        | Espace                   |
| Boutons de sélection            | Croix        | `R` `F` `D` `G`          |
| Carte                           | GUIDE        | `F7`                     |

**Jeux de vol** (After Burner Climax)

| Borne                | Manette                         | Clavier                  |
| -------------------- | ------------------------------- | ------------------------ |
| Manche               | Stick gauche, croix             | Flèches                  |
| Manette des gaz      | Stick droit (vertical), R2 / L2 | —                        |
| Accélérer / ralentir | R1 / L1                         | `X` / `Z`                |
| Tir / missile        | SUD / EST                       | Ctrl gauche / Alt gauche |
| Climax               | NORD                            | Maj gauche               |

* **CONTRÔLES > DISPOSITION DES BOUTONS** place les boutons pour un stick arcade (6 ou 8 boutons) : volant et pédales passent alors sur la croix et les boutons. Voir la page [**Guide Arcade**](../../../arcade-guide.md).
* **CONTRÔLES > INVERSER J1 ET J2** échange les deux manettes. **ZONE MORTE DE LA DIRECTION**, **ZONE MORTE ACCÉLÉRATEUR/FREIN** et **ZONE MORTE DU MANCHE DE VOL** règlent les zones mortes.
* **CONTRÔLES > FICHIER INI DE CONTRÔLES PERSONNALISÉ** utilise votre propre fichier `controls.ini` à la place de celui de RetroBat.
* Les jeux de mahjong se jouent au clavier.

### Pistolets

Les jeux au pistolet (**The House of the Dead 4**, **Let's Go Jungle!**, **2 Spicy**, **Ghost Squad Evolution**, **Rambo**, **Primeval Hunt**…) se jouent au pistolet ou à la souris (**PISTOLETS > ACTIVER LES PISTOLETS**) :

<table><thead><tr><th width="225.25">Borne</th><th>Pistolet / souris</th></tr></thead><tbody><tr><td>Gâchette</td><td>Clic gauche</td></tr><tr><td>Recharger</td><td>Clic droit (<strong>MAPPING DU RECHARGEMENT</strong>)</td></tr><tr><td>Bouton du pistolet</td><td>Clic du milieu (<strong>MAPPING DU BOUTON DU PISTOLET</strong>)</td></tr><tr><td>Bouton d'action</td><td>Start (<strong>MAPPING DU BOUTON D'ACTION</strong>)</td></tr><tr><td>Pédales gauche / droite</td><td>Flèches gauche / droite</td></tr></tbody></table>

Linuxloader ne gère qu'un pistolet. Pour jouer à plusieurs, activez **PISTOLETS > UTILISER DEMULSHOOTER** (DemulShooter s'installe depuis le menu de téléchargement de RetroBat) : le nom du dossier ou du fichier `.game` doit alors être celui de la liste (`hotd4`, `lgj`, `2spicy`…). Avec un pistolet Sinden, RetroBat active la bordure blanche de Linuxloader (**ACTIVER LA BORDURE BLANCHE**). Pour plus de détails, voir la page [**Contrôle des pistolets**](../../../../controleurs/pistolets_controles.md).

### Volants

Avec **VOLANTS DE COURSE > ACTIVER LES VOLANTS**, le volant DirectInput est configuré d'après `linuxloader_wheels.yml` (volant, pédales, vitesses, boutons). Les volants XInput, vus comme des manettes, utilisent le mappage des manettes. Pour les volants pris en charge, voir la page [**Volants**](../../../../controleurs/supported-controllers/volants.md).

### Raccourcis

<table><thead><tr><th width="235.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="259">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Configuration</td><td><code>emulators\linuxloader\linuxloader.ini</code></td></tr><tr><td>Contrôles (écrits par RetroBat)</td><td><code>emulators\linuxloader\controls.ini</code></td></tr><tr><td>Cibles des pistolets</td><td><code>emulators\linuxloader\cross</code></td></tr><tr><td>Position des boutons</td><td><code>system\resources\inputmapping\linuxloader.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr><tr><td>Volants</td><td><code>system\resources\inputmapping\wheels\linuxloader_wheels.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr><tr><td>Noms de jeux reconnus</td><td><code>system\tools\linuxloaderconfig.yml</code></td></tr></tbody></table>

## Guides

### Menu de test

Le menu de test de la borne permet de calibrer les pistolets, de choisir la difficulté ou de vérifier les commandes. Activez **ÉMULATION > MODE TEST** : le jeu démarre directement dans le menu de test, et R3 / L3 deviennent Test / Service (`0` / `9` au clavier).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (636).png" alt="" width="387"><figcaption></figcaption></figure></div>

### Corrections propres à certains jeux

<table><thead><tr><th width="352.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>ÉMULATION > FRÉQUENCE DU PROCESSEUR</strong></td><td>The House of the Dead 4 : fréquence du processeur en GHz (par exemple <code>4.3</code>) si le jeu tourne trop vite ou trop lentement. Détectée automatiquement par défaut.</td></tr><tr><td><strong>CORRECTIFS > CORRECTION DU SCINTILLEMENT HUMMER</strong></td><td>Supprime le scintillement de l'image dans Hummer.</td></tr><tr><td><strong>CORRECTIFS > MODE D'ÉCRAN PRIMEVAL HUNT</strong></td><td>Affichage du second écran (tactile) de Primeval Hunt : côte à côte (par défaut), sans écran tactile, modes 3DS.</td></tr><tr><td><strong>CORRECTIFS > OUTRUN IGNORER LA VÉRIF. DE LA BORNE</strong></td><td>Outrun 2 SP SDX démarre sans la carte de pilotage ni la tour de la borne.</td></tr><tr><td><strong>CORRECTIFS > RAMBO INVERSER LES PISTOLETS</strong></td><td>Change l'affichage des armes dans Rambo.</td></tr></tbody></table>

### Autres options utiles

<table><thead><tr><th width="345.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>ÉMULATION > RÉGION</strong></td><td>Export, US ou Japon.</td></tr><tr><td><strong>ÉMULATION > JEU GRATUIT</strong></td><td>Joue sans crédits.</td></tr><tr><td><strong>MAINTENIR LE RATIO D'AFFICHAGE</strong></td><td>Garde le format de l'image au lieu de l'étirer (activé par défaut).</td></tr><tr><td><strong>VIDÉO > AUGMENTER LA RÉSOLUTION DE RENDU</strong></td><td>Rendu dans la résolution de l'écran (activé par défaut).</td></tr><tr><td><strong>VIDÉO > LIMITER LES FPS</strong>, <strong>FPS CIBLE</strong></td><td>Limite à 60 ou 30 images par seconde.</td></tr><tr><td><strong>PISTOLETS > ACTIVER LE VISEUR INTERNE</strong></td><td>Affiche un viseur à l'écran ; <strong>CHEMIN DU VISEUR J1</strong> / <strong>J2</strong> choisit l'image.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="279">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu revient aussitôt à la liste des jeux</td><td>Vérifiez que le dossier ou le fichier <code>.game</code> porte le nom court du jeu. Si le programme du jeu est dans un sous-dossier inhabituel, placez un fichier <code>.game</code> à côté de lui. Voir la section <a href="lindbergh.md#quel-format-de-jeu"><strong>Quel format de jeu ?</strong></a>.</td></tr><tr><td>The House of the Dead 4 tourne trop vite</td><td>Réglez <strong>ÉMULATION > FRÉQUENCE DU PROCESSEUR</strong>.</td></tr><tr><td>DemulShooter ne reconnaît pas le jeu</td><td>Renommez le dossier ou le fichier <code>.game</code> avec le nom attendu (<code>hotd4</code>, <code>lgj</code>, <code>rambo</code>…).</td></tr><tr><td>Les joueurs 1 et 2 sont inversés</td><td>Activez <strong>CONTRÔLES > INVERSER J1 ET J2</strong>.</td></tr><tr><td>Outrun 2 SP SDX s'arrête sur une erreur de borne</td><td>Activez <strong>CORRECTIFS > OUTRUN IGNORER LA VÉRIF. DE LA BORNE</strong>.</td></tr></tbody></table>
