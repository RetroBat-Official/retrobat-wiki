---
description: Sega
---

# Mega-CD - Sega-CD

| <p></p><p><img src="../../../../.gitbook/assets/image (507).png" alt="" data-size="original"></p> | <p></p><p><img src="../../../../.gitbook/assets/image (508).png" alt="" data-size="original"></p> |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |

Le **Mega-CD** (appelé **Sega CD** en Amérique du Nord) est un lecteur CD-ROM qui se branche sous la MegaDrive. Il est sorti au Japon en décembre 1991, en Amérique du Nord en 1992 et en Europe en 1993. Il ajoute un second processeur 68000 plus rapide, une puce capable d'agrandir et de faire tourner les images, de la mémoire supplémentaire et un son de qualité CD. Ses CD contenaient bien plus de données qu'une cartouche : vidéos, voix et musiques CD.

Environ 200 jeux sont sortis sur Mega-CD : _Sonic CD_, _Snatcher_, _Lunar: The Silver Star_, _Popful Mail_, _Silpheed_, _Robo Aleste_, _Final Fight CD_, _Shining Force CD_, ainsi que des jeux vidéo filmés comme _Night Trap_ ou _Sewer Shark_.

Le Mega-CD lit aussi les cartouches MegaDrive, mais placez-les dans le système MegaDrive : voir la [page Megadrive - Genesis](megadrive-genesis.md).

{% embed url="https://fr.wikipedia.org/wiki/Mega-CD" %}

## En bref

<table><thead><tr><th width="296.5"></th><th></th></tr></thead><tbody><tr><td>Dossier des jeux</td><td>📁 roms \ 📂 megacd</td></tr><tr><td>Extensions</td><td>.chd .cue .iso .m3u .zip .7z</td></tr><tr><td>Émulateur par défaut</td><td>libretro: genesis_plus_gx</td></tr><tr><td>BIOS</td><td>BIOS Mega-CD de la région de vos jeux obligatoire</td></tr><tr><td>Configuration des manettes</td><td>Automatique, tous les émulateurs</td></tr><tr><td>RetroAchievements</td><td>cores libretro</td></tr><tr><td>Jeu en réseau</td><td>cores libretro</td></tr><tr><td>Gestionnaire de sauvegardes ES</td><td>cores libretro, BlastEm, Jgenesis</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                                | Points forts                                                                                    | Limites                                                   |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| **libretro: genesis\_plus\_gx** (défaut) | Précis et complet : tous les formats, changement de disque, pistolets, adaptateurs multijoueurs |                                                           |
| libretro: genesis\_plus\_gx\_wide        | Le même, en écran large (16:9)                                                                  | Défauts graphiques sur les côtés dans certains jeux       |
| libretro: picodrive                      | Très rapide, pour les PC modestes. Le seul qui lance les jeux Mega-CD 32X                       | Moins précis, pas de cartouche de sauvegarde              |
| jgenesis                                 | Récent et précis, cartouche de sauvegarde, chargement du disque en mémoire                      | .chd et .cue uniquement, premier disque seulement en .m3u |
| blastem                                  | Très précis                                                                                     | .cue et .iso, pas de .m3u                                 |
| ares                                     | Émulateur multi-systèmes précis, lance aussi les jeux Mega-CD 32X (core MegaCD32X)              | Premier disque seulement en .m3u                          |
| kega-fusion                              | Émulateur historique, léger                                                                     | .cue et .iso uniquement, n'est plus maintenu              |

## BIOS

Le Mega-CD a besoin de son BIOS, différent selon la région. Copiez-les dans le dossier `bios` :

<table><thead><tr><th width="155.75">Fichier</th><th width="251">Console</th><th>MD5</th></tr></thead><tbody><tr><td>bios_CD_E.bin</td><td>Mega-CD (Europe)</td><td>e66fa1dc5820d254611fdcdba0662372</td></tr><tr><td>bios_CD_U.bin</td><td>Sega CD (Amérique du Nord)</td><td>854b9150240a198070150e4566ae1290</td></tr><tr><td>bios_CD_J.bin</td><td>Mega-CD (Japon)</td><td>278a9397d192149e84e820ac621a8edd</td></tr></tbody></table>

{% hint style="info" %}
Chaque jeu démarre avec le BIOS de sa région : un jeu européen demande bios\_CD\_E.bin, un jeu américain bios\_CD\_U.bin, un jeu japonais bios\_CD\_J.bin. Copiez les trois fichiers si vous avez des jeux de plusieurs régions. RetroBat vérifie qu'au moins un des trois est présent et indique les autres comme OPTIONAL.
{% endhint %}

Tous les émulateurs utilisent les mêmes noms de fichiers.

### Région des jeux

La région du jeu décide du BIOS utilisé et de la vitesse (50 ou 60 Hz). Tous les émulateurs la détectent automatiquement. Pour la forcer, utilisez RÉGION DE LA CONSOLE (lr-genesis\_plus\_gx, Kega Fusion), RÉGION (lr-picodrive), FORCER LA RÉGION (BlastEm, Jgenesis) ou RÉGION PRÉFÉRÉE (Ares) : le BIOS de la région forcée est alors nécessaire.

## Quel format pour les jeux ?

<table><thead><tr><th width="164">Format</th><th>Description</th></tr></thead><tbody><tr><td>.chd</td><td>Image CD compressée, un seul fichier par jeu, avec les pistes audio. <strong>Recommandé</strong> (cores libretro, Jgenesis, Ares)</td></tr><tr><td>.cue (+ .bin)</td><td>Image CD avec ses pistes audio, lue par tous les émulateurs</td></tr><tr><td>.iso</td><td>Image CD sans les pistes audio : la musique CD manque. Pas lue par Jgenesis</td></tr><tr><td>.m3u</td><td>Jeu sur plusieurs disques</td></tr><tr><td>.zip / .7z</td><td>Image CD compressée, cores libretro et Jgenesis uniquement. Préférez le .chd</td></tr></tbody></table>

{% hint style="success" %}
Les jeux Mega-CD utilisent beaucoup la musique CD : évitez le .iso et préférez le **.chd**. Pour convertir un jeu .cue/.bin : `chdman createcd -i "jeu.cue" -o "jeu.chd"`.
{% endhint %}

### Jeux sur plusieurs disques

Certains jeux tiennent sur plusieurs CD (_Night Trap_…). Créez un fichier .m3u dans `roms\megacd`, par exemple `Night Trap.m3u` :

```
Night Trap (Disc 1).chd
Night Trap (Disc 2).chd
```

* **cores libretro** : changez de disque avec HOTKEY + L1 (éjecter/insérer) et HOTKEY + L2/R2 (disque précédent/suivant).
* **Jgenesis, Ares** : seul le premier disque démarre.
* **BlastEm, Kega Fusion** : pas de .m3u, lancez chaque disque séparément.

## Contrôles

Le Mega-CD utilise la manette MegaDrive : configuration automatique, dispositions, manette 3 boutons, manettes de type Mega Drive et adaptateurs multijoueurs fonctionnent comme pour la MegaDrive. Voir la [page Megadrive - Genesis](megadrive-genesis.md) pour le détail.

<table><thead><tr><th width="225.75">Émulateur</th><th width="153.25">Configuration auto</th><th>Joueurs</th></tr></thead><tbody><tr><td>lr-genesis_plus_gx, lr-genesis_plus_gx_wide</td><td>Oui</td><td>2, jusqu'à 8 avec un adaptateur (TYPE DE CONTRÔLEUR)</td></tr><tr><td>lr-picodrive</td><td>Oui</td><td>2</td></tr><tr><td>Jgenesis</td><td>Oui</td><td>2</td></tr><tr><td>BlastEm</td><td>Oui</td><td>2, jusqu'à 8 (ADAPTATEUR MULTIJOUEURS)</td></tr><tr><td>Ares</td><td>Oui</td><td>2</td></tr><tr><td>Kega Fusion</td><td>Oui</td><td>2, jusqu'à 8 (ADAPTATEUR MULTIJOUEURS)</td></tr></tbody></table>

### Disposition par défaut (manette 6 boutons)

<table><thead><tr><th width="128">Mega Drive</th><th width="102.25">Manette</th><th width="191.75"></th><th width="123.75">Mega Drive</th><th width="150.75">Manette</th></tr></thead><tbody><tr><td>A</td><td>OUEST</td><td></td><td>X</td><td>L1</td></tr><tr><td>B</td><td>SUD</td><td></td><td>Y</td><td>NORD</td></tr><tr><td>C</td><td>EST</td><td></td><td>Z</td><td>R1</td></tr><tr><td>START</td><td>START</td><td></td><td>MODE</td><td>SELECT</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (494).png" alt="" width="225"><figcaption></figcaption></figure></div>

Les options **DISPOSITION DES BOUTONS**, **MANETTE 3-BOUTONS** (TYPE DE CONTRÔLEUR avec lr-genesis\_plus\_gx) et **UTILISER UNE MANETTE DE TYPE MEGADRIVE** (sous-menu CONTRÔLES) fonctionnent comme pour la [MegaDrive](megadrive-genesis.md#controles). Pour la 8BitDo M30, voir la page [Contrôleurs spéciaux](../../../../controleurs/supported-controllers/gamepads/controleurs-speciaux.md).

### Pistolets

Plusieurs jeux Mega-CD se jouent au pistolet, comme _Lethal Enforcers_ ou _Snatcher_ (Justifier). Avec les cores Genesis Plus GX, activez les pistolets (sous-menu PISTOLETS) et choisissez le TYPE DE PISTOLET : **Justifier** ou **Menacer**. Voir la [page Pistolets](../../../../controleurs/supported-controllers/lightguns/).

### Raccourcis

**Cores libretro** : [raccourcis standards de RetroBat](../../../../navigation/hotkeys.md).

| Raccourci      | BlastEm            | Jgenesis           | Ares               | Kega Fusion |
| -------------- | ------------------ | ------------------ | ------------------ | ----------- |
| HOTKEY + START | Quitter            | Quitter            | Quitter            | Quitter     |
| HOTKEY + OUEST | Sauvegarder l'état | Sauvegarder l'état | Sauvegarder l'état |             |
| HOTKEY + NORD  | Charger l'état     | Charger l'état     | Charger l'état     |             |

## Dossiers

<table><thead><tr><th width="197">Émulateur</th><th width="245">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>libretro</td><td>Sauvegardes (mémoire interne, cartouche)</td><td><code>saves\megacd</code></td></tr><tr><td>libretro</td><td>Sauvegardes d'état</td><td><code>saves\megacd\libretro.&#x3C;core></code></td></tr><tr><td>BlastEm</td><td>Sauvegardes et sauvegardes d'état</td><td><code>saves\megacd\blastem\&#x3C;jeu></code></td></tr><tr><td>Jgenesis</td><td>Sauvegardes</td><td><code>saves\megacd\jgenesis</code></td></tr><tr><td>Ares</td><td>Sauvegardes</td><td><code>saves\megacd\ares</code></td></tr><tr><td>Kega Fusion</td><td>Sauvegardes / sauvegardes d'état</td><td><code>saves\megacd</code> / <code>saves\megacd\kega-fusion\sstates</code></td></tr><tr><td>Captures d'écran</td><td></td><td><code>screenshots</code> (un sous-dossier par émulateur)</td></tr></tbody></table>

## Guides

### Jeux Mega-CD 32X

Quelques jeux demandent à la fois le Mega-CD et le 32X, comme les versions 32X de _Night Trap_, _Corpse Killer_, _Slam City_ ou _Fahrenheit_. Placez-les dans `roms\megacd` et, dans les options du jeu, choisissez **libretro: picodrive** ou **ares: MegaCD32X** : les autres émulateurs n'émulent pas le 32X en plus du Mega-CD. Le BIOS Mega-CD est nécessaire, pas ceux du 32X.

### Sauvegardes et cartouche de sauvegarde

Les jeux Mega-CD sauvegardent dans la mémoire interne de la console, petite et partagée entre tous les jeux. Une **cartouche de sauvegarde** (RAM cartridge) optionnelle ajoutait de la place. Avec Jgenesis, l'option **RAM CART** (sous-menu ÉMULATION, activée par défaut) l'émule. Si un jeu indique que la mémoire est pleine, effacez d'anciennes sauvegardes dans le gestionnaire de mémoire du BIOS : lancez l'émulateur sans jeu, ou appuyez sur START sur l'écran du BIOS.

### Charger le disque en mémoire

Avec Jgenesis, **LOAD GAME TO RAM** copie tout le disque en mémoire au démarrage : le jeu démarre un peu plus tard, mais les lectures sont ensuite plus rapides.

## Problèmes connus

<table><thead><tr><th width="314">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Écran noir ou « BIOS introuvable »</td><td>Copiez le BIOS de la région du jeu (bios_CD_E/U/J.bin) dans le dossier bios.</td></tr><tr><td>Pas de musique dans le jeu</td><td>Le format .iso n'a pas l'audio CD : utilisez une image .cue/.bin ou .chd.</td></tr><tr><td>Un jeu .chd ne démarre pas avec Kega Fusion ou BlastEm</td><td>Utilisez lr-genesis_plus_gx, Jgenesis ou Ares, ou une image .cue/.bin.</td></tr><tr><td>Un jeu .iso ne démarre pas avec Jgenesis</td><td>Jgenesis ne lit que les .chd et .cue : convertissez le jeu en .chd.</td></tr><tr><td>Le second disque ne démarre pas</td><td>Utilisez un fichier .m3u avec un core libretro et changez de disque avec HOTKEY + L1 / L2 / R2.</td></tr><tr><td>Le jeu indique que la mémoire est pleine</td><td>Effacez d'anciennes sauvegardes dans le gestionnaire de mémoire du BIOS, ou activez RAM CART avec Jgenesis.</td></tr><tr><td>Les boutons ne sont pas où je les attends</td><td>Changez la DISPOSITION DES BOUTONS. Voir la <a href="megadrive-genesis.md#controles">page Megadrive - Genesis</a>.</td></tr><tr><td>Un jeu Mega-CD 32X reste sur un écran noir</td><td>Utilisez libretro: picodrive ou ares: MegaCD32X pour ce jeu.</td></tr></tbody></table>
