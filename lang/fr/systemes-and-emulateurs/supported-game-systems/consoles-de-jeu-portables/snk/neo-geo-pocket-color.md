---
description: SNK
---

# Neo Geo Pocket Color

<div align="left"><figure><img src="../../../../.gitbook/assets/image (708).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **Neo Geo Pocket Color** est la version couleur de la console portable de SNK, sortie en mars 1999 au Japon, puis en Amérique du Nord et en Europe. Elle est arrêtée en 2000 hors du Japon et en 2001 au Japon, après le rachat de SNK.

Sa ludothèque compte environ 80 jeux, dont beaucoup de jeux de combat et d'adaptations de l'arcade : SNK vs. Capcom: The Match of the Millennium, The King of Fighters R-2, Metal Slug 1st et 2nd Mission, Sonic the Hedgehog Pocket Adventure… Elle se distingue par son petit stick à micro-interrupteurs, qui « clique » comme un stick d'arcade, et par ses deux boutons **A** et **B**.

Elle lit aussi tous les jeux de la Neo Geo Pocket, qui a son propre système dans RetroBat (voir la page [**Neo Geo Pocket**](neo-geo-pocket.md)).

{% embed url="https://fr.wikipedia.org/wiki/Neo-Geo_Pocket_Color" %}

## En bref

<table><thead><tr><th width="285.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\ngpc</code></td></tr><tr><td><strong>Extensions</strong></td><td>.ngp .ngc .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: mednafen_ngp</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (optionnel pour ares)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk ; Mednafen et ares par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non (console à un joueur, câble de liaison non émulé)</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                            | Pour qui ?               | Points forts                                                                                                         | Limites                                                                                                                             |
| ------------------------------------ | ------------------------ | -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **libretro: mednafen\_ngp** (défaut) | Tout le monde            | Beetle NeoPop, la version libretro de l'émulation Neo Geo Pocket de Mednafen : fiable, sans BIOS, RetroAchievements. | —                                                                                                                                   |
| **libretro: race**                   | Alternative              | RACE, autre émulateur très léger, sans BIOS. RetroAchievements.                                                      | —                                                                                                                                   |
| **mednafen** (autonome)              | Utilisateurs de Mednafen | Même émulation que le core mednafen\_ngp, avec des boutons de tir automatique.                                       | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.                                                                  |
| **ares**                             | Puristes                 | Émulation la plus précise, avec le vrai BIOS de la console.                                                          | Demande le BIOS (voir [**BIOS**](neo-geo-pocket-color.md#bios)). Pas de RetroAchievements. Sauvegardes instantanées par raccourcis. |
| **bizhawk: NeoPop**                  | Utilisateurs de BizHawk  | Émulation de Mednafen dans BizHawk, sauvegardes instantanées dans le menu de RetroBat.                               | —                                                                                                                                   |

**En cas de doute, gardez libretro: mednafen\_ngp.**

## BIOS

Aucun BIOS n'est nécessaire, sauf pour **ares**. Les autres émulateurs ont un BIOS de remplacement intégré.

<table><thead><tr><th width="190">Fichier</th><th width="86.5">Dossier</th><th width="320.5">MD5</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp</code></td><td><code>bios</code></td><td>d87d876c4391935c9d48ef352a3ff02d</td><td>ares, système Neo Geo Pocket</td></tr><tr><td><code>[BIOS] SNK Neo Geo Pocket Color (Japan, Europe) (En,Ja).ngp</code></td><td><code>bios</code></td><td>3655aacebb43a963607d4cf821fc1301</td><td>ares, système Neo Geo Pocket Color</td></tr></tbody></table>

ares prend le BIOS de la console de chaque système. S'il manque, il utilise l'autre : un seul des deux fichiers suffit pour jouer aux deux systèmes. Les fichiers doivent porter exactement ces noms.

> **Ancienne installation** : RetroBat utilisait avant un seul fichier, `[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp`, qui contenait en fait le **BIOS Color** (MD5 3655aacebb43a963607d4cf821fc1301). ares fonctionne toujours avec ce fichier. Pour que chaque système ait le bon BIOS, renommez-le en `[BIOS] SNK Neo Geo Pocket Color (Japan, Europe) (En,Ja).ngp`, puis ajoutez le BIOS monochrome sous l'autre nom.

La vérification des BIOS de RetroBat les liste comme optionnels.

Au premier lancement avec ares, le BIOS peut demander de régler la langue, la date et l'heure de la console, comme sur la vraie machine. **ÉMULATION > DÉMARRAGE RAPIDE** (ares) passe l'animation de démarrage du BIOS.

## Quel format de jeu ?

Les jeux sont des fichiers `.ngp` (jeux Neo Geo Pocket) ou `.ngc` (jeux Neo Geo Pocket Color), éventuellement compressés en `.zip` ou `.7z` (un jeu par archive). Tous les émulateurs lisent les deux formats.

### Neo Geo Pocket ou Neo Geo Pocket Color ?

RetroBat a deux systèmes, `ngp` et `ngpc`, avec les mêmes émulateurs. Rangez chaque jeu dans le système de sa console.

* Avec les cores libretro, Mednafen et BizHawk, l'émulateur choisit tout seul le mode d'après le jeu : un jeu couleur s'affiche en couleur, même dans le système `ngp`.
* Avec **ares**, le système choisit la console émulée : `ngp` émule la Neo Geo Pocket monochrome, `ngpc` la Neo Geo Pocket Color. Dans ce système, ares émule la console **couleur**.
* Sur la vraie Neo Geo Pocket monochrome, la plupart des jeux couleur fonctionnent en noir et blanc. Quelques-uns ne démarrent pas (Sonic the Hedgehog Pocket Adventure, SNK vs. Capcom: The Match of the Millennium…).

## Contrôles

RetroBat configure automatiquement les manettes. La console a un stick (sur la croix directionnelle de la manette), deux boutons **A** et **B**, un bouton **Option** (pause et menus des jeux) et un bouton **Power**.

| Manette RetroBat     | cores libretro | mednafen            | ares   | bizhawk |
| -------------------- | -------------- | ------------------- | ------ | ------- |
| Croix directionnelle | Stick          | Stick               | Stick  | Stick   |
| SUD                  | A              | A                   | A      | A       |
| EST                  | B              | B                   | B      | B       |
| OUEST                | —              | A (tir automatique) | —      | —       |
| NORD                 | —              | B (tir automatique) | —      | —       |
| START                | Option         | Option              | Option | Option  |
| L1                   | —              | —                   | Power  | —       |

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch. Mednafen, ares et BizHawk utilisent les raccourcis communs de RetroBat (sauvegarde et chargement instantanés, capture d'écran, avance rapide…). Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

| Contenu                                         | Dossier                                                                                                                  |
| ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Jeux                                            | `roms\ngpc`                                                                                                              |
| BIOS (ares)                                     | `bios`                                                                                                                   |
| Cores libretro, Mednafen : sauvegardes des jeux | `saves\ngpc`                                                                                                             |
| Cores libretro : sauvegardes instantanées       | `saves\ngpc\libretro.<core>`                                                                                             |
| Mednafen : sauvegardes instantanées             | `saves\ngpc\mednafen\sstates`                                                                                            |
| ares : sauvegardes des jeux et instantanées     | `saves\ngpc\ares`                                                                                                        |
| BizHawk : sauvegardes des jeux                  | `saves\ngpc\bizhawk`                                                                                                     |
| BizHawk : sauvegardes instantanées              | `saves\ngpc\bizhawk\sstates\NeoPop`                                                                                      |
| Captures d'écran (Mednafen, ares, BizHawk)      | <p><code>screenshots\mednafen</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\ngpc</code></p> |

## Guides

### Langue des jeux

Beaucoup de jeux sont bilingues anglais / japonais : la console choisit la langue. RetroBat règle l'**anglais** par défaut.

* Cores mednafen\_ngp et race, Mednafen, BizHawk : **ÉMULATION > LANGUE DE LA CONSOLE** (**ANGLAIS** ou **JAPONAIS**). Redémarrez le jeu après un changement.
* ares : la langue se règle dans le menu du BIOS de la console, comme sur la vraie machine.

### RetroAchievements

Les jeux Neo Geo Pocket et Neo Geo Pocket Color sont dans la même catégorie de RetroAchievements. Les cores mednafen\_ngp et race sont compatibles. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

<table><thead><tr><th width="105.75">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>ares</td><td><strong>RENDU VISUEL > MÉLANGE INTER-IMAGE</strong></td><td>Imite la rémanence de l'écran LCD : certains jeux s'en servent pour des effets de transparence.</td></tr><tr><td>ares</td><td><strong>RENDU VISUEL > ÉMULATION PRÉCISE DES COULEURS</strong></td><td>Couleurs proches de celles de l'écran d'origine.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="326.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>ares demande un firmware ou ne démarre pas</td><td>Aucun des deux BIOS n'est présent, ou ils n'ont pas exactement le bon nom dans <code>bios</code> (voir <a href="neo-geo-pocket-color.md#bios"><strong>BIOS</strong></a>). Ou utilisez un autre émulateur, qui n'a pas besoin de BIOS.</td></tr><tr><td>La vérification des BIOS signale un fichier différent (système Neo Geo Pocket)</td><td>Le fichier <code>[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp</code> est le BIOS Color d'une ancienne installation : renommez-le (voir <a href="neo-geo-pocket-color.md#bios"><strong>BIOS</strong></a>).</td></tr><tr><td>Un jeu s'affiche en noir et blanc</td><td>Avec ares, le jeu est rangé dans le système <code>ngp</code> : déplacez-le dans <code>roms\ngpc</code>.</td></tr><tr><td>Un jeu s'affiche en japonais</td><td>Réglez <strong>ÉMULATION > LANGUE DE LA CONSOLE</strong> sur <strong>ANGLAIS</strong>, puis redémarrez le jeu. Certains jeux n'existent qu'en japonais.</td></tr><tr><td>Un jeu propose un mode à deux joueurs par câble</td><td>Le câble de liaison entre deux consoles (et la connexion avec la Dreamcast) n'est émulé par aucun émulateur.</td></tr></tbody></table>
