---
description: Sega
---

# Sega 32X

| <p></p><p><img src="../../../../.gitbook/assets/image (509).png" alt="" data-size="original"></p> | <p></p><p><img src="../../../../.gitbook/assets/image (510).png" alt="" data-size="original"></p> |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |

## Présentation

Le **32X** est une extension qui se branche dans le port cartouche de la MegaDrive. Sega l'a lancé fin 1994 pour prolonger la vie de sa console en attendant la Saturn. Il ajoute deux processeurs Hitachi SH-2 (la même famille que dans la Saturn) et une nouvelle puce vidéo : plus de couleurs et des graphismes 3D, affichés par-dessus l'image de la MegaDrive.

Sorti quelques mois seulement avant la Saturn, le 32X a reçu une quarantaine de jeux, dont _Virtua Racing Deluxe_, _Star Wars Arcade_, _Doom_, _Knuckles' Chaotix_, _Virtua Fighter_, _Kolibri_, _Space Harrier_ et _After Burner Complete_.

Les quelques jeux qui demandent à la fois le Mega-CD et le 32X (Mega-CD 32X), comme les versions 32X de _Night Trap_ ou _Corpse Killer_, sont des jeux sur CD : placez-les dans le système Mega-CD et lancez-les avec **libretro: picodrive** ou **ares: MegaCD32X** (voir la [page Mega-CD](mega-cd-sega-cd.md)).

{% embed url="https://fr.wikipedia.org/wiki/32X" %}

## En bref

<table><thead><tr><th width="270.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\sega32x</code></td></tr><tr><td><strong>Extensions</strong></td><td>.32x .smd .bin .md .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: picodrive</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun obligatoire</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BlastEm, Jgenesis, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                        | Points forts                                                  | Limites                                       |
| -------------------------------- | ------------------------------------------------------------- | --------------------------------------------- |
| **libretro: picodrive** (défaut) | Rapide et compatible, sans BIOS, RetroAchievements            |                                               |
| jgenesis                         | Récent et précis, sans BIOS                                   | Demande un PC plus puissant                   |
| blastem                          | Très précis, adaptateur multijoueurs                          | BIOS 32X obligatoires, demande un PC puissant |
| ares                             | Émulateur multi-systèmes précis, sans BIOS                    | Demande un PC plus puissant                   |
| kega-fusion                      | Émulateur historique, léger, adaptateur multijoueurs          | N'est plus maintenu                           |
| bizhawk: PicoDrive               | PicoDrive avec les outils de BizHawk (TAS, RetroAchievements) |                                               |

## BIOS

La plupart des émulateurs n'ont besoin d'aucun BIOS pour le 32X. **BlastEm** demande les trois BIOS du 32X, et Kega-Fusion les utilise s'ils sont présents. Copiez-les dans le dossier `bios` :

<table><thead><tr><th width="173.25">Fichier</th><th width="233.25">Processeur</th><th>MD5</th></tr></thead><tbody><tr><td>32X_G_BIOS.BIN</td><td>68000 (côté Mega Drive)</td><td>6a5433f6a132a2b683635819a6dcf085</td></tr><tr><td>32X_M_BIOS.BIN</td><td>SH-2 maître</td><td>f88354ec482be09aeccd76a97bb75868</td></tr><tr><td>32X_S_BIOS.BIN</td><td>SH-2 esclave</td><td>7f041b6a55cd7423a6c08a219335269e</td></tr></tbody></table>

{% hint style="info" %}
RetroBat indique ces fichiers comme OPTIONAL : ils ne sont nécessaires qu'avec BlastEm.
{% endhint %}

### Région des jeux

La région décide quelle version d'un jeu tourne et sa vitesse (50 ou 60 Hz). Tous les émulateurs la détectent automatiquement. Pour la forcer, utilisez RÉGION (lr-picodrive), FORCER LA RÉGION (BlastEm, Jgenesis), RÉGION PRÉFÉRÉE (Ares) ou RÉGION DE LA CONSOLE (Kega Fusion, BizHawk).

## Quel format pour les jeux ?

<table><thead><tr><th width="220.25">Format</th><th>Description</th></tr></thead><tbody><tr><td>.32x</td><td>Copie de cartouche 32X (format habituel)</td></tr><tr><td>.bin / .md / .smd</td><td>Autres formats de cartouche</td></tr><tr><td>.zip / .7z</td><td>Jeux compressés</td></tr></tbody></table>

## Contrôles

Le 32X utilise la manette Mega Drive : configuration automatique, dispositions, manette 3 boutons, manettes de type Mega Drive et adaptateurs multijoueurs fonctionnent comme pour la MegaDrive. Voir la[ page Megadrive - Genesis](megadrive-genesis.md) pour le détail.

| Émulateur    | Configuration auto | Joueurs                                |
| ------------ | ------------------ | -------------------------------------- |
| lr-picodrive | Oui                | 2                                      |
| Jgenesis     | Oui                | 2                                      |
| BlastEm      | Oui                | 2, jusqu'à 8 (ADAPTATEUR MULTIJOUEURS) |
| Ares         | Oui                | 2                                      |
| Kega Fusion  | Oui                | 2, jusqu'à 8 (ADAPTATEUR MULTIJOUEURS) |
| BizHawk      | Oui                | 2                                      |

### Disposition par défaut (manette 6 boutons)

| Mega Drive | Manette |   | Mega Drive | Manette |
| ---------- | ------- | - | ---------- | ------- |
| A          | OUEST   |   | X          | L1      |
| B          | SUD     |   | Y          | NORD    |
| C          | EST     |   | Z          | R1      |
| START      | START   |   | MODE       | SELECT  |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (494).png" alt="" width="225"><figcaption></figcaption></figure></div>

L'option **DISPOSITION DES BOUTONS** (sous-menu CONTRÔLES) est disponible avec tous les émulateurs. **MANETTE 3-BOUTONS** existe avec lr-picodrive, Jgenesis et BlastEm, et **UTILISER UNE MANETTE DE TYPE MEGADRIVE** avec tous les émulateurs. Pour la 8BitDo M30, voir la page [Contrôleurs spéciaux](../../../../controleurs/supported-controllers/gamepads/controleurs-speciaux.md).

### Raccourcis

**Core libretro** : [raccourcis standards de RetroBat.](../../../../navigation/hotkeys.md)

<table><thead><tr><th>Raccourci</th><th width="123">BlastEm</th><th width="123">Jgenesis</th><th width="124.25">Ares</th><th width="121.5">BizHawk</th><th>Kega Fusion</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td><td>Quitter</td><td>Quitter</td><td>Quitter</td><td>Quitter</td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarder l'état</td><td>Sauvegarder l'état</td><td>Sauvegarder l'état</td><td>Sauvegarder l'état</td><td></td></tr><tr><td>HOTKEY + NORD</td><td>Charger l'état</td><td>Charger l'état</td><td>Charger l'état</td><td>Charger l'état</td><td></td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="175.75">Émulateur</th><th width="226">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>lr-picodrive</td><td>Sauvegardes</td><td><code>saves\sega32x</code></td></tr><tr><td>lr-picodrive</td><td>Sauvegardes d'état</td><td><code>saves\sega32x\libretro.picodrive</code></td></tr><tr><td>BlastEm</td><td>Sauvegardes et sauvegardes d'état</td><td><code>saves\sega32x\blastem\&#x3C;jeu></code></td></tr><tr><td>Jgenesis</td><td>Sauvegardes</td><td><code>saves\sega32x\jgenesis</code></td></tr><tr><td>Ares</td><td>Sauvegardes</td><td><code>saves\sega32x\ares</code></td></tr><tr><td>Kega Fusion</td><td>Sauvegardes / sauvegardes d'état</td><td><code>saves\sega32x</code> / <code>saves\sega32x\kega-fusion\sstates</code></td></tr><tr><td>BizHawk</td><td>Sauvegardes</td><td><code>saves\sega32x\bizhawk</code></td></tr><tr><td>Captures d'écran</td><td></td><td><code>screenshots</code> (un sous-dossier par émulateur)</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="292.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Écran noir avec BlastEm</td><td>Copiez les trois BIOS 32X dans le dossier bios, ou utilisez lr-picodrive.</td></tr><tr><td>Le jeu est lent ou saccade</td><td>L'émulation du 32X est exigeante avec BlastEm, Jgenesis et Ares : utilisez lr-picodrive.</td></tr><tr><td>Un jeu Mega-CD 32X ne démarre pas</td><td>Placez-le dans le système Mega-CD et utilisez libretro: picodrive ou ares: MegaCD32X.</td></tr><tr><td>Les boutons ne sont pas où je les attends</td><td>Changez la DISPOSITION DES BOUTONS. Voir la page Megadrive - Genesis.</td></tr></tbody></table>
