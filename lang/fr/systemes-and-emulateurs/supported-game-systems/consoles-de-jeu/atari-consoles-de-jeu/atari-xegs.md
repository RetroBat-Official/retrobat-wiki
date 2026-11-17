---
description: Atari
---

# Atari XEGS

<div align="left"><figure><img src="../../../../.gitbook/assets/image (641).png" alt="" width="469"><figcaption></figcaption></figure></div>

## Présentation

L'**Atari XE Game System** (XEGS) sort en 1987. C'est un Atari 65XE en forme de console : il lit les cartouches et les disquettes des ordinateurs Atari 8 bits, avec un clavier détachable et un pistolet optique, le XG-1. Le jeu Missile Command est intégré à la console : il démarre quand aucune cartouche n'est insérée et que le clavier est débranché.

Atari ressort pour l'occasion des jeux de ses ordinateurs en cartouche, souvent avec un nouvel emballage : Ballblazer, Rescue on Fractalus!, Lode Runner, One-on-One Basketball, Archon, Flight Simulator II, Bug Hunt (au pistolet)… La console est arrêtée en 1992.

Les jeux des ordinateurs Atari 8 bits ont leur propre système (voir la page [**Atari 800**](../../micro-ordinateurs/atari-micro-ordinateurs/atari-800.md)).

{% embed url="https://fr.wikipedia.org/wiki/Atari_XE_Video_Game_System" %}

## En bref

<table><thead><tr><th width="255.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\xegs</code></td></tr><tr><td><strong>Extensions</strong></td><td>.atr .dsk .xfd .bin .rom .car .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: atari800</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (MAME : <code>xegs.zip</code>)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; MAME par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core libretro mame</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="152.75">Émulateur</th><th width="153.5">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: atari800</strong> (défaut)</td><td>Tout le monde</td><td>Atari800 7.0 en mode XEGS, système intégré (AltirraOS), clavier XEGS branché ou débranché, sauvegardes instantanées.</td><td>—</td></tr><tr><td><strong>altirra</strong></td><td>Puristes</td><td>Altirra, l'émulateur le plus précis des Atari 8 bits, avec le profil XEGS et le choix exact du type de cartouche.</td><td>Un seul bouton de tir à la manette. Pas de sauvegardes instantanées ni de raccourcis RetroBat (seul HOTKEY + START, pour quitter).</td></tr><tr><td><strong>libretro: mame</strong></td><td>Utilisateurs de MAME</td><td>Émulation XEGS de MAME, jeu en réseau.</td><td>Demande <code>xegs.zip</code>. Cartouches de la liste de logiciels MAME uniquement (voir <a href="atari-xegs.md#quel-format-de-jeu"><strong>Quel format de jeu ?</strong></a>).</td></tr><tr><td><strong>mame64</strong> (MAME autonome)</td><td>Utilisateurs de MAME</td><td>Même émulation que le core libretro mame.</td><td>Mêmes limites.</td></tr></tbody></table>

**En cas de doute, gardez libretro: atari800.**

## BIOS

Aucun BIOS n'est nécessaire avec le core atari800 et Altirra : ils ont un système libre intégré. MAME demande le BIOS de la console.

<table><thead><tr><th width="140.25">Fichier</th><th width="148.75">Dossier</th><th>MD5</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>ATARIXL.ROM</code></td><td><code>bios</code></td><td>06daac977823773a3eea3422fd26a703</td><td>core atari800 (OS des XL/XE), facultatif</td></tr><tr><td><code>BB01R4_OS.ROM</code></td><td><code>bios</code></td><td>b7a2a04677d34f069eeb643d5238bf86</td><td>core atari800 (OS de l'XEGS), facultatif</td></tr><tr><td><code>XEGAME.ROM</code></td><td><code>bios</code></td><td>d7eb37aec6960cba36bc500e0e5d00bc</td><td>core atari800 (Missile Command intégré), facultatif</td></tr><tr><td><code>xegs.zip</code></td><td><code>bios</code></td><td>—</td><td>MAME (core libretro mame et mame64)</td></tr><tr><td><code>xegs.xml</code></td><td><code>bios\mame\hash</code></td><td>—</td><td>MAME : liste des logiciels (fournie avec RetroBat)</td></tr></tbody></table>

La vérification des BIOS de RetroBat les liste tous comme optionnels, car l'émulateur par défaut n'en a pas besoin. `xegs.zip` vient du set de BIOS de MAME de la même version que l'émulateur MAME de RetroBat.

## Quel format de jeu ?

<table><thead><tr><th width="118.25">Type</th><th width="167.75">Extensions</th><th>Remarques</th></tr></thead><tbody><tr><td>Cartouche</td><td><code>.car</code>, <code>.rom</code>, <code>.bin</code></td><td><code>.car</code> contient le type de la cartouche. Avec <code>.rom</code> et <code>.bin</code>, l'émulateur le déduit de la taille du fichier.</td></tr><tr><td>Disquette</td><td><code>.atr</code>, <code>.xfd</code>, <code>.dsk</code></td><td>Le XEGS lit les disquettes avec le lecteur des ordinateurs Atari.</td></tr></tbody></table>

Les fichiers peuvent être compressés en `.zip` ou `.7z` (un jeu par archive).

**Avec MAME**, RetroBat lance les cartouches par la liste de logiciels `xegs` : le fichier doit porter le nom court du jeu dans cette liste (le nom du jeu dans le set de logiciels MAME `xegs`). Une cartouche renommée, ou absente de la liste, ne démarre pas. **ÉMULATION > FORCER LA SOFTWARELIST** et **ÉMULATION > FORCER LE TYPE DE MÉDIA** permettent de forcer la liste ou le type de média.

## Contrôles

RetroBat configure automatiquement les manettes. La manette du XEGS est le joystick Atari à un bouton. Les touches **Start**, **Select** et **Option** de la console sont sur la manette.

| Manette RetroBat     | libretro: atari800              | altirra                                        |
| -------------------- | ------------------------------- | ---------------------------------------------- |
| Croix directionnelle | Joystick                        | Joystick                                       |
| Stick gauche         | —                               | Joystick (option **UTILISER LE STICK GAUCHE**) |
| SUD                  | Tir                             | Tir                                            |
| EST                  | Tir 2 (manettes à deux boutons) | —                                              |
| OUEST                | Espace                          | —                                              |
| NORD                 | Return                          | —                                              |
| START                | Start                           | Start                                          |
| SELECT               | Select                          | Select                                         |
| L1                   | Option                          | —                                              |
| L2                   | Esc                             | —                                              |
| R2                   | Help                            | —                                              |
| L3                   | Clavier virtuel                 | —                                              |

Avec MAME, les contrôles suivent la disposition de MAME dans RetroBat : voir la page [**MAME**](../../arcade/mame.md).

Le pistolet XG-1 (Bug Hunt, Crossbow…) n'est configuré par RetroBat avec aucun émulateur.

**CONTRÔLES > BRANCHER LE CLAVIER XEGS** (core atari800, activé par défaut) : clavier branché ou débranché. Clavier débranché, la console démarre comme sans clavier : quelques jeux changent de comportement.

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch. MAME autonome utilise les raccourcis communs de RetroBat. Avec Altirra, seul HOTKEY + START (quitter) est configuré par RetroBat. Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="401.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\xegs</code></td></tr><tr><td>BIOS</td><td><code>bios</code> (<code>xegs.zip</code> pour MAME)</td></tr><tr><td>Liste des logiciels MAME</td><td><code>bios\mame\hash\xegs.xml</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><code>saves\xegs\libretro.&#x3C;core></code></td></tr><tr><td>Core atari800 : fichier de configuration du moteur</td><td><code>emulators\retroarch\.atari800.cfg</code></td></tr><tr><td>MAME autonome</td><td>Voir la page <a href="../../arcade/mame.md"><strong>MAME</strong></a></td></tr><tr><td>Altirra : configuration</td><td><code>emulators\altirra\Altirra.ini</code></td></tr></tbody></table>

## Guides

### Type de cartouche (Altirra)

Avec une cartouche `.rom` ou `.bin`, Altirra choisit le type d'après la taille du fichier (8K, 16K, XEGS 32K à 1M). Si le jeu ne démarre pas, choisissez le type dans **ÉMULATION > CHOIX DE LA CARTOUCHE**. Les cartouches `.car` n'en ont pas besoin.

### Autres options utiles

<table><thead><tr><th width="140.75">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>core atari800</td><td><strong>VIDÉO > FORMAT VIDÉO ÉMULÉ</strong></td><td><strong>NTSC</strong> (défaut) ou <strong>PAL</strong>.</td></tr><tr><td>core atari800</td><td><strong>RENDU VISUEL > PALETTE</strong></td><td>Palettes de couleurs toutes faites.</td></tr><tr><td>core atari800</td><td><strong>CONTRÔLES > HACKS DES MANETTES</strong></td><td><strong>DOUBLE STICK</strong>, <strong>INVERSER LES PORTS</strong>, <strong>JOY 2B+</strong> (voir la page <strong>Atari 800</strong>).</td></tr><tr><td>altirra</td><td><strong>VIDÉO > STANDARD VIDÉO</strong></td><td>NTSC (défaut), PAL, SECAM…</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="342.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>MAME ne démarre pas ou demande des fichiers</td><td><code>xegs.zip</code> manque dans <code>bios</code>, ou le nom de la cartouche n'est pas celui de la liste de logiciels <code>xegs</code>. Utilisez le core atari800 ou Altirra.</td></tr><tr><td>Une cartouche <code>.rom</code> ou <code>.bin</code> ne démarre pas</td><td>Utilisez la version <code>.car</code>, ou choisissez le type dans <strong>CHOIX DE LA CARTOUCHE</strong> (Altirra).</td></tr><tr><td>Un jeu au pistolet ne répond pas</td><td>Le pistolet XG-1 n'est pas configuré par RetroBat.</td></tr></tbody></table>
