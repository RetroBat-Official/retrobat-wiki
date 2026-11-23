---
description: SNK
---

# Neo Geo Pocket

<div align="left"><figure><img src="../../../../.gitbook/assets/image (707).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **Neo Geo Pocket** est la première console portable de SNK, sortie au Japon en octobre 1998. Son écran est **monochrome**, en niveaux de gris. Faute de succès face au Game Boy, elle est remplacée dès mars 1999 par la Neo Geo Pocket Color, et ne compte qu'une dizaine de jeux (Samurai Shodown!, King of Fighters R-1, Neo Geo Cup '98…).

Comme sa remplaçante, elle se distingue par son petit stick à micro-interrupteurs, qui « clique » comme un stick d'arcade, et par ses deux boutons **A** et **B**.

La plupart des jeux de la Neo Geo Pocket Color fonctionnent aussi sur la Neo Geo Pocket, en noir et blanc (voir [**Neo Geo Pocket ou Neo Geo Pocket Color ?**](neo-geo-pocket.md#neo-geo-pocket-ou-neo-geo-pocket-color)). Ils ont leur propre système dans RetroBat (voir la page [**Neo Geo Pocket Color**](neo-geo-pocket-color.md)).

{% embed url="https://fr.wikipedia.org/wiki/Neo-Geo_Pocket" %}

## En bref

<table><thead><tr><th width="274"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\ngp</code></td></tr><tr><td><strong>Extensions</strong></td><td>.ngp .ngc .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: mednafen_ngp</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (optionnel pour ares)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk ; Mednafen et ares par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non (console à un joueur, câble de liaison non émulé)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="157.75">Émulateur</th><th>Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: mednafen_ngp</strong> (défaut)</td><td>Tout le monde</td><td>Beetle NeoPop, la version libretro de l'émulation Neo Geo Pocket de Mednafen : fiable, sans BIOS, RetroAchievements.</td><td>—</td></tr><tr><td><strong>libretro: race</strong></td><td>Alternative</td><td>RACE, autre émulateur très léger, sans BIOS. RetroAchievements.</td><td>—</td></tr><tr><td><strong>mednafen</strong> (autonome)</td><td>Utilisateurs de Mednafen</td><td>Même émulation que le core mednafen_ngp, avec des boutons de tir automatique.</td><td>Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr><tr><td><strong>ares</strong></td><td>Puristes</td><td>Émulation la plus précise, avec le vrai BIOS de la console.</td><td>Demande le BIOS (voir <a href="neo-geo-pocket.md#bios"><strong>BIOS</strong></a>). Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr><tr><td><strong>bizhawk: NeoPop</strong></td><td>Utilisateurs de BizHawk</td><td>Émulation de Mednafen dans BizHawk, sauvegardes instantanées dans le menu de RetroBat.</td><td>—</td></tr></tbody></table>

**En cas de doute, gardez libretro: mednafen\_ngp.**

## BIOS

Aucun BIOS n'est nécessaire, sauf pour **ares**. Les autres émulateurs ont un BIOS de remplacement intégré.

<table><thead><tr><th width="202.5">Fichier</th><th width="80.25">Dossier</th><th width="318.75">MD5</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp</code></td><td><code>bios</code></td><td>d87d876c4391935c9d48ef352a3ff02d</td><td>ares, système Neo Geo Pocket</td></tr><tr><td><code>[BIOS] SNK Neo Geo Pocket Color (Japan, Europe) (En,Ja).ngp</code></td><td><code>bios</code></td><td>3655aacebb43a963607d4cf821fc1301</td><td>ares, système Neo Geo Pocket Color</td></tr></tbody></table>

ares prend le BIOS de la console de chaque système. S'il manque, il utilise l'autre : un seul des deux fichiers suffit pour jouer aux deux systèmes. Les fichiers doivent porter exactement ces noms.

> **Ancienne installation** : RetroBat utilisait avant un seul fichier, `[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp`, qui contenait en fait le **BIOS Color** (MD5 3655aacebb43a963607d4cf821fc1301). ares fonctionne toujours avec ce fichier. Pour que chaque système ait le bon BIOS, renommez-le en `[BIOS] SNK Neo Geo Pocket Color (Japan, Europe) (En,Ja).ngp`, puis ajoutez le BIOS monochrome sous l'autre nom.

La vérification des BIOS de RetroBat les liste comme optionnels.

Au premier lancement avec ares, le BIOS peut demander de régler la langue, la date et l'heure de la console, comme sur la vraie machine. **ÉMULATION > DÉMARRAGE RAPIDE** (ares) passe l'animation de démarrage du BIOS.

## Quel format de jeu ?

Les jeux sont des fichiers `.ngp` (jeux Neo Geo Pocket) ou `.ngc` (jeux Neo Geo Pocket Color), éventuellement compressés en `.zip` ou `.7z` (un jeu par archive). Tous les émulateurs lisent les deux formats.

### Neo Geo Pocket ou Neo Geo Pocket Color ?

RetroBat a deux systèmes, `ngp` et `ngpc`, avec les mêmes émulateurs. Rangez chaque jeu dans le système de sa console.

* Avec les cores libretro, Mednafen et BizHawk, l'émulateur choisit tout seul le mode d'après le jeu : un jeu couleur s'affiche en couleur, même dans le système `ngp`.
* Avec **ares**, le système choisit la console émulée : `ngp` émule la Neo Geo Pocket monochrome, `ngpc` la Neo Geo Pocket Color. Dans ce système, ares émule la console **monochrome**.
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

| Contenu                                         | Dossier                                                                                                                 |
| ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Jeux                                            | `roms\ngp`                                                                                                              |
| BIOS (ares)                                     | `bios`                                                                                                                  |
| Cores libretro, Mednafen : sauvegardes des jeux | `saves\ngp`                                                                                                             |
| Cores libretro : sauvegardes instantanées       | `saves\ngp\libretro.<core>`                                                                                             |
| Mednafen : sauvegardes instantanées             | `saves\ngp\mednafen\sstates`                                                                                            |
| ares : sauvegardes des jeux et instantanées     | `saves\ngp\ares`                                                                                                        |
| BizHawk : sauvegardes des jeux                  | `saves\ngp\bizhawk`                                                                                                     |
| BizHawk : sauvegardes instantanées              | `saves\ngp\bizhawk\sstates\NeoPop`                                                                                      |
| Captures d'écran (Mednafen, ares, BizHawk)      | <p><code>screenshots\mednafen</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\ngp</code></p> |

## Guides

### Langue des jeux

Beaucoup de jeux sont bilingues anglais / japonais : la console choisit la langue. RetroBat règle l'**anglais** par défaut.

* Cores mednafen\_ngp et race, Mednafen, BizHawk : **ÉMULATION > LANGUE DE LA CONSOLE** (**ANGLAIS** ou **JAPONAIS**). Redémarrez le jeu après un changement.
* ares : la langue se règle dans le menu du BIOS de la console, comme sur la vraie machine.

### RetroAchievements

Les jeux Neo Geo Pocket et Neo Geo Pocket Color sont dans la même catégorie de RetroAchievements. Les cores mednafen\_ngp et race sont compatibles. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

<table><thead><tr><th width="112">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>ares</td><td><strong>RENDU VISUEL > MÉLANGE INTER-IMAGE</strong></td><td>Imite la rémanence de l'écran LCD : certains jeux s'en servent pour des effets de transparence.</td></tr><tr><td>ares</td><td><strong>RENDU VISUEL > ÉMULATION PRÉCISE DES COULEURS</strong></td><td>Couleurs proches de celles de l'écran d'origine.</td></tr></tbody></table>

## Problèmes connus

| Problème                                                                       | Solution                                                                                                                                                                                     |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ares demande un firmware ou ne démarre pas                                     | Aucun des deux BIOS n'est présent, ou ils n'ont pas exactement le bon nom dans `bios` (voir [**BIOS**](neo-geo-pocket.md#bios)). Ou utilisez un autre émulateur, qui n'a pas besoin de BIOS. |
| La vérification des BIOS signale un fichier différent (système Neo Geo Pocket) | Le fichier `[BIOS] SNK Neo Geo Pocket (Japan, Europe) (En,Ja).ngp` est le BIOS Color d'une ancienne installation : renommez-le (voir [**BIOS**](neo-geo-pocket.md#bios)).                    |
| Un jeu s'affiche en noir et blanc                                              | Avec ares, le jeu est rangé dans le système `ngp` : déplacez-le dans `roms\ngpc`.                                                                                                            |
| Un jeu s'affiche en japonais                                                   | Réglez **ÉMULATION > LANGUE DE LA CONSOLE** sur **ANGLAIS**, puis redémarrez le jeu. Certains jeux n'existent qu'en japonais.                                                                |
| Un jeu propose un mode à deux joueurs par câble                                | Le câble de liaison entre deux consoles (et la connexion avec la Dreamcast) n'est émulé par aucun émulateur.                                                                                 |
