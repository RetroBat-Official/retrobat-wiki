---
description: Fujitsu
---

# FM-7

<div align="left"><figure><img src="../../../../.gitbook/assets/image (746).png" alt="" width="300"><figcaption></figcaption></figure></div>

## Présentation

Le **FM-7** (Fujitsu Micro 7) est un ordinateur de Fujitsu sorti en 1982, au Japon. Il a deux processeurs Motorola 6809 : l'un fait tourner les programmes, l'autre gère l'affichage. Il est suivi du **FM-77AV** (1985), avec 4 096 couleurs et un son FM. Le FM Towns lui succède en 1989.

Sa ludothèque compte surtout des jeux sur cassette et disquette, souvent des jeux d'aventure et de rôle : Thexder, Xanadu, Hydlide, Ys…

{% embed url="https://fr.wikipedia.org/wiki/FM-7" %}

## En bref

<table><thead><tr><th width="254"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\fm7</code></td></tr><tr><td><strong>Extensions</strong></td><td>.wav .t77 .mfi .dfi .hfe .mfm .td0 .imd .d77 .d88 .1dd .cqm .cqi .dsk .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: mame</td></tr><tr><td><strong>BIOS</strong></td><td><code>fm7.zip</code> (<code>fm77av.zip</code> pour le FM-77AV)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Clavier ; Pad2Key pour la manette</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core libretro ; MAME par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core libretro mame</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                   | Pour qui ?           | Points forts                                                                                        | Limites                                  |
| --------------------------- | -------------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| **libretro: mame** (défaut) | Tout le monde        | MAME dans RetroArch : FM-7 et FM-77AV, cassettes lancées automatiquement, sauvegardes instantanées. | —                                        |
| **mame64** (MAME autonome)  | Utilisateurs de MAME | Même émulation, avec le menu de MAME.                                                               | Sauvegardes instantanées par raccourcis. |

**En cas de doute, gardez libretro: mame.**

## BIOS

MAME demande le jeu de ROM du modèle émulé, au format MAME, de la même version que l'émulateur MAME de RetroBat.

<table><thead><tr><th width="258.25">Fichier</th><th width="153.25">Dossier</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>fm7.zip</code></td><td><code>bios</code></td><td>FM-7 (modèle par défaut)</td></tr><tr><td><code>fm77av.zip</code></td><td><code>bios</code></td><td>FM-77AV (<strong>MODÈLE DE MACHINE ÉMULÉE = FM-77AV</strong>), facultatif</td></tr><tr><td><code>fm7_cass.xml</code>, <code>fm7_disk.xml</code>, <code>fm77av.xml</code></td><td><code>bios\mame\hash</code></td><td>Listes de logiciels MAME (fournies avec RetroBat), pour <strong>FORCER LA SOFTWARELIST</strong></td></tr></tbody></table>

La vérification des BIOS de RetroBat demande `fm7.zip` et liste les autres fichiers comme optionnels.

## Quel format de jeu ?

<table><thead><tr><th width="110.75">Type</th><th>Extensions</th><th>Remarques</th></tr></thead><tbody><tr><td>Cassette</td><td><code>.t77</code>, <code>.wav</code></td><td>RetroBat lance la cassette automatiquement (commande <code>LOADM"",,R</code> tapée après 5 secondes).</td></tr><tr><td>Disquette</td><td><code>.d77</code>, <code>.d88</code>, <code>.mfi</code>, <code>.dfi</code>, <code>.hfe</code>, <code>.mfm</code>, <code>.td0</code>, <code>.imd</code>, <code>.1dd</code>, <code>.cqm</code>, <code>.cqi</code>, <code>.dsk</code></td><td><code>.d77</code> est le plus courant. La machine démarre sur la disquette.</td></tr></tbody></table>

Les fichiers peuvent être compressés en `.zip` ou `.7z`. Les jeux écrits pour le FM-77AV ne marchent qu'en FM-77AV : voir [**Guides**](fm-7.md#fm-7-ou-fm-77av).

## Contrôles

Le FM-7 n'a pas de manette standard : la plupart des jeux se jouent au clavier, avec le pavé numérique pour les directions. Le clavier du PC sert de clavier FM-7.

* Pour jouer à la manette, mettez des touches du clavier sur la manette avec **Pad2Key** (voir la page [**Pad2Key**](../../../../controleurs/pad2key.md)).
* Avec le core libretro mame, appuyez sur `Arrêt défil` pour activer le **Game Focus** de RetroArch : toutes les touches vont au FM-7.
* Avec MAME autonome, `Arrêt défil` bascule entre le clavier émulé complet et les touches de MAME.

### Raccourcis

Le core libretro mame utilise les raccourcis standards de RetroArch. MAME autonome utilise les raccourcis communs de RetroBat. Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

| Contenu                                       | Dossier                                       |
| --------------------------------------------- | --------------------------------------------- |
| Jeux                                          | `roms\fm7`                                    |
| BIOS                                          | `bios` (`fm7.zip`, `fm77av.zip`)              |
| Listes de logiciels MAME                      | `bios\mame\hash`                              |
| Core libretro mame : sauvegardes instantanées | `saves\fm7\libretro.mame`                     |
| MAME autonome                                 | Voir la page [**MAME**](../../arcade/mame.md) |

## Guides

### FM-7 ou FM-77AV ?

Par défaut, RetroBat émule un FM-7. Les jeux écrits pour le FM-77AV (plus de couleurs, son FM) demandent **ÉMULATION > MODÈLE DE MACHINE ÉMULÉE = FM-77AV**, et le fichier `fm77av.zip` dans `bios`.

### Lancer une cassette ou une disquette

RetroBat choisit le média d'après l'extension : cassette pour `.t77` et `.wav`, disquette pour les autres. Si le jeu est mal reconnu (archive `.zip`, par exemple), **ÉMULATION > FORCER LE TYPE DE MÉDIA** choisit **Cassette**, **Disque (lecteur 1)** ou **Disque (lecteur 2)**.

### Listes de logiciels

**ÉMULATION > FORCER LA SOFTWARELIST** lance le jeu depuis une liste de logiciels MAME (**Images disque Fujitsu FM-7**, **Cassettes Fujitsu FM-7**, **Images disque Fujitsu FM-77AV**). Le fichier doit alors porter le nom court du jeu dans cette liste.

## Problèmes connus

<table><thead><tr><th width="371.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>MAME ne démarre pas ou demande des fichiers</td><td><code>fm7.zip</code> manque dans <code>bios</code>, ou il ne correspond pas à la version de MAME. Pour le FM-77AV, ajoutez <code>fm77av.zip</code>.</td></tr><tr><td>Une cassette ne se lance pas</td><td>Attendez quelques secondes que la commande soit tapée. Sinon, tapez <code>LOADM"",,R</code> puis Entrée.</td></tr><tr><td>Le jeu affiche des couleurs fausses ou plante</td><td>C'est un jeu FM-77AV : voir <a href="fm-7.md#fm-7-ou-fm-77av"><strong>FM-7 ou FM-77AV ?</strong></a>.</td></tr><tr><td>Les touches du clavier lancent des raccourcis de RetroArch</td><td>Appuyez sur <code>Arrêt défil</code> (Game Focus).</td></tr></tbody></table>
