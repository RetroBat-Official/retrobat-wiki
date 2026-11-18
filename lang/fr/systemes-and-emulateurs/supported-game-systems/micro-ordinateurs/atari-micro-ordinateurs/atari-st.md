---
description: Atari
---

# Atari ST

<div align="left"><figure><img src="../../../../.gitbook/assets/image (647).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

L'**Atari ST** sort en 1985 (520 ST, puis 1040 ST). Il a un processeur Motorola 68000 et l'interface graphique GEM, avec une souris, et coûte bien moins cher que ses concurrents. Ses prises MIDI intégrées en font l'ordinateur des musiciens. En Europe, et surtout en France, c'est l'un des ordinateurs de jeu les plus populaires de la fin des années 1980. Viennent ensuite le Mega ST, le STE (1989 : plus de couleurs, son numérique, ports de manettes améliorés), le Mega STE, le TT et le Falcon.

Sa ludothèque est immense : Dungeon Master, Xenon 2, Populous, Captain Blood, Carrier Command, Starglider, Another World, Lemmings, Kick Off… La plupart des jeux sont sur disquette.

{% embed url="https://fr.wikipedia.org/wiki/Atari_ST" %}

## En bref

<table><thead><tr><th width="269"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\atarist</code></td></tr><tr><td><strong>Extensions</strong></td><td>.st .msa .stx .dim .ipf .ctr .gz .m3u .gem .gemdos .acsi .ahd .vhd .scsi .shd .ide .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: hatarib</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (TOS facultatif ; obligatoire pour hatari2014)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; Hatari par raccourcis (une par jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core libretro hatarib</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="139">Émulateur</th><th width="137.25">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: hatarib</strong> (défaut)</td><td>Tout le monde</td><td>hatariB, une version libretro récente de Hatari : EmuTOS intégré, clavier à l'écran, souris au stick droit, disques durs, sauvegardes instantanées, jeu en réseau.</td><td>—</td></tr><tr><td><strong>libretro: hatari2014</strong></td><td>Dépannage</td><td>Ancienne version libretro de Hatari (1.8).</td><td>Demande <code>tos.img</code>. Ni disques durs, ni <code>.ctr</code> / <code>.gz</code>.</td></tr><tr><td><strong>hatari</strong> (autonome)</td><td>Puristes</td><td>Hatari dans sa version d'origine, avec son menu complet : ST, Mega ST, STE, Mega STE, manettes Jaguar du STE, enregistrement vidéo.</td><td>Demande un TOS (voir <a href="atari-st.md#bios"><strong>BIOS</strong></a>). Une seule sauvegarde instantanée par jeu, par raccourcis.</td></tr></tbody></table>

**En cas de doute, gardez libretro: hatarib.**

## BIOS

Le système de l'Atari ST, le **TOS**, est dans la ROM de la machine. hatariB a **EmuTOS** intégré, un TOS libre compatible avec la plupart des jeux : aucun fichier n'est nécessaire. Un TOS d'origine reste plus compatible avec certains jeux.

<table><thead><tr><th width="219.5">Fichier</th><th width="174">Dossier</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>tos.img</code></td><td><code>bios</code></td><td>TOS par défaut : hatarib, hatari2014 (obligatoire), hatari</td></tr><tr><td><code>tos102.img</code>, <code>tos104.img</code>, <code>tos106.img</code>, <code>tos206.img</code></td><td><code>bios\hatari\tos</code></td><td>Choix de <strong>ÉMULATION > TOS</strong> (hatarib, hatari2014, hatari)</td></tr><tr><td><code>emutos.img</code></td><td><code>bios\hatari\tos</code></td><td>hatari, hatari2014 : EmuTOS</td></tr></tbody></table>

La vérification des BIOS de RetroBat les liste comme optionnels. Il existe plusieurs versions de chaque TOS (pays, révisions) : RetroBat ne vérifie pas le MD5. Les fichiers doivent porter exactement ces noms.

* **hatarib** : `tos.img` s'il est présent, sinon EmuTOS. Un TOS choisi dans **ÉMULATION > TOS** est copié automatiquement de `bios\hatari\tos` vers `bios\hatarib`, le dossier lu par le core.
* **hatari** : `tos.img`, sinon `emutos.img`. Sans l'un des deux, Hatari ne démarre pas (message « Missing TOS file »).
* **hatari2014** : `tos.img`, ou le TOS choisi dans **ÉMULATION > TOS**.

Quel TOS choisir ?

<table><thead><tr><th width="157">TOS</th><th width="161.25">Machines</th><th>Remarques</th></tr></thead><tbody><tr><td>1.00, 1.02, 1.04</td><td>ST, Mega ST</td><td>Le plus compatible avec les jeux sur disquette. 1.04 est conseillé pour les jeux installés sur disque dur.</td></tr><tr><td>1.06, 1.62</td><td>STE uniquement</td><td>Avec Hatari, RetroBat choisit alors la machine STE automatiquement.</td></tr><tr><td>2.06</td><td>ST et STE</td><td>Meilleure gestion des disques durs, moins compatible avec quelques vieux jeux.</td></tr><tr><td>EmuTOS</td><td>Toutes</td><td>Libre, gère les disques durs. Compatible avec la plupart des jeux, pas tous.</td></tr></tbody></table>

RetroBat évite les combinaisons qui ne marchent pas : le démarrage automatique et les disques durs GEMDOS demandent un TOS 1.04 ou plus récent, les images de disque dur demandent un pilote que seul EmuTOS a intégré. Dans ces cas, RetroBat prend un TOS compatible (TOS 1.04, 2.06 ou EmuTOS).

## Quel format de jeu ?

<table><thead><tr><th width="190.75">Type</th><th>Extensions</th><th>Remarques</th></tr></thead><tbody><tr><td>Disquette</td><td><code>.st</code>, <code>.msa</code></td><td>Les formats les plus courants.</td></tr><tr><td>Disquette protégée</td><td><code>.stx</code>, <code>.ipf</code>, <code>.ctr</code></td><td>Gardent les protections contre la copie. <code>.ipf</code> et <code>.ctr</code> se lisent avec la bibliothèque CAPS, fournie par RetroBat.</td></tr><tr><td>Disquette</td><td><code>.dim</code>, <code>.gz</code></td><td><code>.gz</code> : disquette compressée.</td></tr><tr><td>Plusieurs disquettes</td><td><code>.m3u</code></td><td>Liste des disquettes d'un jeu (voir <a href="atari-st.md#jeux-installes-sur-disque-dur-gemdos"><strong>Guides</strong></a>).</td></tr><tr><td>Disque dur (image)</td><td><code>.acsi</code>, <code>.ahd</code>, <code>.vhd</code>, <code>.scsi</code>, <code>.shd</code>, <code>.ide</code></td><td>Le type de disque dépend de l'extension. hatarib et hatari.</td></tr><tr><td>Disque dur (dossier)</td><td><code>.gem</code>, <code>.gemdos</code></td><td>Un dossier du PC vu comme un disque dur (GEMDOS, voir <a href="atari-st.md#jeux-installes-sur-disque-dur-gemdos"><strong>Guides</strong></a>).</td></tr></tbody></table>

Les fichiers peuvent être compressés en `.zip` ou `.7z`. Les formats de disque dur, `.ctr` et `.gz` ne marchent pas avec hatari2014.

## Contrôles

RetroBat configure automatiquement les manettes. Le joystick de l'Atari ST a un seul bouton. La souris du PC sert de souris Atari, et le clavier du PC de clavier Atari.

| Manette RetroBat     | libretro: hatarib              | libretro: hatari2014      | hatari                                     |
| -------------------- | ------------------------------ | ------------------------- | ------------------------------------------ |
| Croix directionnelle | Joystick                       | Joystick                  | Joystick                                   |
| Stick gauche         | Joystick                       | —                         | Joystick                                   |
| Stick droit          | Souris                         | —                         | —                                          |
| SUD                  | Tir                            | —                         | Tir                                        |
| EST                  | Tir automatique                | Tir                       | Barre espace ou saut (option **BOUTON 2**) |
| OUEST                | Clic gauche                    | Menu de l'émulateur       | Tir automatique                            |
| NORD                 | Clic droit                     | —                         | —                                          |
| SELECT               | Choix du lecteur A ou B        | Bascule souris / joystick | —                                          |
| START                | Écran d'aide                   | Clavier à l'écran         | —                                          |
| L1                   | Clavier à l'écran              | Numéro du joystick        | —                                          |
| R1                   | Clavier à l'écran (une touche) | Vitesse de la souris      | —                                          |
| L2                   | Souris lente                   | Affichage de l'état       | —                                          |
| R2                   | Souris rapide                  | —                         | —                                          |
| L3                   | Espace                         | —                         | —                                          |
| R3                   | Return                         | —                         | —                                          |

Le **clavier à l'écran** de hatarib : L1 l'affiche, choisissez une touche à la croix, L1 l'appuie, R1 ferme le clavier. R1 seul ouvre le clavier en mode « une touche » : le jeu est en pause jusqu'à l'appui. NORD déplace le clavier en haut ou en bas.

Avec hatari2014, le bouton OUEST ouvre le menu du core et SELECT bascule entre souris et joystick sur la croix.

Avec les cores libretro, appuyez sur `Arrêt défil` pour activer le **Game Focus** de RetroArch : toutes les touches du clavier vont à l'Atari. Pour mettre des touches du clavier sur la manette, voir la page [**Pad2Key**](../../../../controleurs/pad2key.md).

**OPTIONS AVANCÉES > CONTRÔLES** :

* **UTILISER LA SOURIS** (hatarib, activé par défaut) : souris branchée sur le port 1. Désactivez-la pour les jeux à deux joysticks.
* **ACTIVER JOYSTICK 2** (hatari2014, activé par défaut) : peut gêner la souris.
* **ACTIVER LE TIR AUTOMATIQUE**, **BOUTON 2**, **UTILISER LES JOYPADS JAGUAR (STE)** (hatari) : tir automatique, rôle du 2e bouton (**BARRE ESPACE**, pour Xenon 2, ou **SAUT (HAUT)**, pour les jeux de plateforme), manettes du STE.

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch. Hatari utilise les raccourcis communs de RetroBat :

<table><thead><tr><th width="205.75">Raccourci</th><th width="121">Touche</th><th>Hatari</th></tr></thead><tbody><tr><td>HOTKEY + SUD</td><td><code>F12</code></td><td>Menu de l'émulateur</td></tr><tr><td>HOTKEY + OUEST</td><td><code>F2</code></td><td>Sauvegarde instantanée</td></tr><tr><td>HOTKEY + NORD</td><td><code>F4</code></td><td>Chargement instantané</td></tr><tr><td>HOTKEY + R3</td><td><code>F8</code></td><td>Capture d'écran</td></tr><tr><td>HOTKEY + L3</td><td><code>F11</code></td><td>Plein écran</td></tr><tr><td>HOTKEY + START</td><td>—</td><td>Quitter</td></tr></tbody></table>

Au clavier : `AltGr` + `Q` quitte Hatari (`Échap` est une touche de l'Atari). `Pause` met en pause. Les touches `F1` à `F10` existent sur le clavier de l'Atari : avec **CONTRÔLES > TOUCHES DE FONCTION = CLAVIER ATARI**, `F2`, `F4` et `F8` vont au jeu, et les sauvegardes et captures passent sur `AltGr` + `K`, `L` et `G` (les raccourcis manette envoient toujours `F2`, `F4` et `F8`). Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

| Contenu                                         | Dossier                                                      |
| ----------------------------------------------- | ------------------------------------------------------------ |
| Jeux                                            | `roms\atarist`                                               |
| TOS                                             | `bios` (`tos.img`), `bios\hatari\tos`                        |
| hatarib : TOS copiés, NVRAM du TT et du Falcon  | `bios\hatarib`, `bios\hatarib.nvram`                         |
| hatarib : disquettes modifiées par les jeux     | `saves\atarist`                                              |
| Cores libretro : sauvegardes instantanées       | `saves\atarist\libretro.<core>`                              |
| Hatari : sauvegardes instantanées (une par jeu) | `saves\atarist\hatari` (`<jeu>.sav`, `<jeu>.auto.sav`)       |
| Hatari : captures d'écran                       | `screenshots`                                                |
| Hatari : vidéos                                 | `records\output\hatari`                                      |
| Hatari : configuration et journal               | `emulators\hatari\hatari.cfg`, `emulators\hatari\hatari.log` |

hatarib ne modifie jamais vos disquettes : il écrit une copie de la disquette modifiée dans `saves\atarist`, et la reprend au lancement suivant. Supprimez cette copie pour revenir à la disquette d'origine. Hatari autonome écrit directement dans la disquette.

## Guides

### Jeux sur plusieurs disquettes : le fichier m3u

Créez un fichier `.m3u` qui liste les disquettes, une par ligne, puis lancez le `.m3u`. hatarib et Hatari lisent le même format. Lignes facultatives :

<table><thead><tr><th width="275.25">Ligne</th><th>Effet</th></tr></thead><tbody><tr><td><code>#AUTO:C:\JEU\JEU.PRG</code></td><td>Lance ce programme au démarrage (TOS 1.04 ou plus récent).</td></tr><tr><td><code>#RES:low</code>, <code>#RES:med</code>, <code>#RES:high</code></td><td>Résolution au démarrage.</td></tr><tr><td><code>#BOOTA:2</code>, <code>#BOOTB:0</code></td><td>Disquette mise dans le lecteur A ou B au démarrage (1 = première de la liste, 0 = lecteur vide).</td></tr></tbody></table>

Exemple :

```
Jeu (Disk 1).st
Jeu (Disk 2).st
```

Avec hatarib, changez de disquette dans le menu de RetroArch (**Contrôle du disque**) ; SELECT choisit le lecteur A ou B. Avec Hatari, changez de disquette dans son menu (HOTKEY + SUD).

### Jeux installés sur disque dur (GEMDOS)

Beaucoup de jeux existent en version « installée », dans un dossier (versions adaptées au disque dur). Le dossier est vu comme un disque dur par l'Atari :

1. Placez le dossier du jeu dans `roms\atarist`, par exemple `roms\atarist\Jeu`.
2. Créez à côté un fichier vide du même nom, avec l'extension `.gem` : `roms\atarist\Jeu.gem`.
3. Pour lancer le jeu automatiquement, créez un fichier `Jeu.m3u` qui contient :

```
#AUTO:C:\JEU.PRG
Jeu.gem
```

en remplaçant `JEU.PRG` par le programme du jeu, avec son chemin dans le dossier.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (649).png" alt=""><figcaption></figcaption></figure></div>

4. Lancez le `.m3u` (ou le `.gem` sans démarrage automatique).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (648).png" alt=""><figcaption></figcaption></figure></div>

Avec Hatari autonome, vous pouvez aussi nommer le dossier `Jeu.gemdos`, ou mettre un fichier `Jeu.autorun` à côté du jeu, avec le programme à lancer (`C:\JEU.PRG`).

Avec hatarib, **ÉMULATION > DÉMARRAGE SUR DISQUE DUR** est automatique : la machine démarre sur le disque dur quand le jeu a un disque dur et pas de disquette.

### Choisir la machine

Par défaut, RetroBat émule un **ST** avec 1 Mo de mémoire. Quelques jeux demandent un **STE** (jeux STE « enhanced », manettes Jaguar) : **ÉMULATION > MACHINE ÉMULÉE**. Avec Hatari, choisir TOS 1.06 ou les manettes Jaguar passe automatiquement en STE (4 Mo). **ÉMULATION > TAILLE DE LA MÉMOIRE** (hatarib) ou **TAILLE DE LA MÉMOIRE RAM** (hatari) change la mémoire.

### Jeux en haute résolution

Les programmes en haute résolution (640 × 400, noir et blanc) demandent le moniteur monochrome d'Atari : **RENDU VISUEL > TYPE DE MONITEUR > MONOCHROME HAUTE RÉSOLUTION** (hatarib) ou **VIDÉO > TYPE DE MONITEUR > MONOCHROME** (hatari).

### Autres options utiles

<table><thead><tr><th width="119.5">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>hatarib</td><td><strong>ÉMULATION > ACCÈS DISQUETTE RAPIDE</strong></td><td>Chargements plus rapides (activé par défaut). Désactivez-le pour un jeu protégé qui ne démarre pas.</td></tr><tr><td>hatarib</td><td><strong>ÉMULATION > CYCLE EXACT</strong></td><td>Émulation exacte, nécessaire à certaines démos et jeux (activé par défaut).</td></tr><tr><td>hatarib</td><td><strong>ÉMULATION > RÉGION EMUTOS</strong>, <strong>FRÉQUENCE D'AFFICHAGE EMUTOS</strong></td><td>Langue d'EmuTOS, 50 Hz ou 60 Hz.</td></tr><tr><td>hatarib</td><td><strong>VIDÉO > BORDURES DE L'ÉCRAN</strong></td><td>Taille des bordures, ou image rognée en 720p / 1080p.</td></tr><tr><td>hatarib</td><td><strong>VIDÉO > RATIO D'ASPECT DES PIXELS</strong></td><td>Pixels carrés (défaut) ou forme d'origine (moniteur Atari, téléviseur).</td></tr><tr><td>hatarib</td><td><strong>INTERFACE UTILISATEUR > AFFICHER LA BARRE DE STATUT</strong></td><td>Barre d'état de Hatari, ou seulement la LED du lecteur.</td></tr><tr><td>hatari</td><td><strong>ÉMULATION > DÉMARRAGE RAPIDE</strong></td><td>Démarrage plus rapide du TOS.</td></tr><tr><td>hatari</td><td><strong>ÉMULATION > SAUVEGARDE AUTOMATIQUE</strong></td><td>Sauvegarde la partie en quittant et la reprend au lancement suivant.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="350.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Hatari affiche « Missing TOS file »</td><td>Ajoutez <code>tos.img</code> dans <code>bios</code>, ou <code>emutos.img</code> dans <code>bios\hatari\tos</code>. Ou utilisez hatarib, qui a EmuTOS intégré.</td></tr><tr><td>Message « Panic » au démarrage, ou le jeu s'arrête sur le bureau GEM</td><td>Le jeu n'est pas compatible avec EmuTOS : ajoutez un TOS d'origine (<code>tos.img</code>, de préférence TOS 1.02 ou 1.04).</td></tr><tr><td>Un jeu protégé <code>.st</code> ne démarre pas</td><td>Désactivez <strong>ACCÈS DISQUETTE RAPIDE</strong>, ou utilisez la version <code>.stx</code> / <code>.ipf</code> du jeu.</td></tr><tr><td>Le jeu demande la disquette 2</td><td>Utilisez un fichier <code>.m3u</code> (voir <a href="atari-st.md#jeux-sur-plusieurs-disquettes-le-fichier-m3u"><strong>Guides</strong></a>), puis changez de disquette.</td></tr><tr><td>Le joystick ne répond pas, la souris bouge à la place</td><td>Le jeu lit le joystick sur le port 1 (port de la souris) : désactivez <strong>UTILISER LA SOURIS</strong> (hatarib).</td></tr><tr><td>Les touches F1 à F10 ne répondent pas dans un jeu (Hatari)</td><td>Réglez <strong>TOUCHES DE FONCTION</strong> sur <strong>CLAVIER ATARI</strong>.</td></tr><tr><td>Écran noir avec un programme en haute résolution</td><td>Choisissez le moniteur monochrome (voir <a href="atari-st.md#jeux-en-haute-resolution"><strong>Jeux en haute résolution</strong></a>).</td></tr></tbody></table>
