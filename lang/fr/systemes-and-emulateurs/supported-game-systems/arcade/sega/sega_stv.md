---
description: Sega
---

# Sega Titan-Video

<div align="left"><figure><img src="../../../../.gitbook/assets/image (639).png" alt="" width="376"><figcaption></figcaption></figure></div>

## Présentation

Le **ST-V** (Sega Titan Video) est une carte d'arcade de Sega, sortie en 1994. Elle reprend presque à l'identique le matériel de la Saturn (deux processeurs SH-2, puces graphiques VDP1 et VDP2), ce qui permet d'adapter rapidement ses jeux sur la console. Les jeux sont sur cartouches. Bon marché, la carte est utilisée par Sega et de nombreux éditeurs jusqu'au début des années 2000.

Parmi ses jeux : **Radiant Silvergun**, **Die Hard Arcade**, **Virtua Fighter Remix**, **Shienryu**, **Cotton 2**, **Final Fight Revenge**, **Astra Superstars**, **Decathlete**, **Golden Axe: The Duel**, **Puyo Puyo Sun**, **Columns '97**, **Baku Baku Animal**, **Groove on Fight**, **Funky Head Boxers**.

RetroBat propose plusieurs émulateurs : les cores libretro **kronos** (par défaut) et **mednafen\_saturn**, les cores libretro **mame** (et ses anciennes versions), **Mednafen** et **MAME**.

{% embed url="https://fr.wikipedia.org/wiki/ST-V" %}

## En bref

<table><thead><tr><th width="280.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\segastv</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: kronos</td></tr><tr><td><strong>BIOS</strong></td><td><code>stvbios.zip</code> dans <code>bios</code> ; <code>epr-20091.ic8</code>, <code>epr-17952a.ic8</code>, <code>epr-17954a.ic8</code> dans <code>bios</code> (Mednafen)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs (mappage par jeu pour les cores mednafen_saturn, mame et mame2003_plus)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Cores libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Cores libretro</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="202">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: kronos</strong> (défaut)</td><td>Émulateur Saturn et ST-V rapide, résolution augmentée (jusqu'à 8x), choix de la région du BIOS.</td><td>Demande une carte graphique compatible OpenGL 4.3. Pas de placement des boutons jeu par jeu.</td></tr><tr><td><strong>libretro: mednafen_saturn</strong></td><td>Émulation très précise, boutons placés comme sur la borne pour chaque jeu, dispositions arcade.</td><td>Plus gourmand.</td></tr><tr><td><strong>libretro: mame</strong></td><td>Grande compatibilité, choix de la version du BIOS, mappage par jeu, dispositions arcade.</td><td>Romset du MAME actuel.</td></tr><tr><td><strong>libretro: mame2016</strong>, <strong>mame2014</strong>, <strong>mame2010</strong>, <strong>mame2003_plus</strong>, <strong>mame2003</strong></td><td>Anciennes versions de MAME, plus légères (mappage par jeu avec mame2003_plus).</td><td>Chaque core demande le romset de sa version de MAME, moins de jeux fonctionnels.</td></tr><tr><td><strong>mednafen</strong></td><td>Même émulation que le core mednafen_saturn, en émulateur autonome.</td><td>Une quarantaine de jeux pris en charge. Demande les fichiers du BIOS hors archive. Pas de placement des boutons jeu par jeu.</td></tr><tr><td><strong>mame</strong></td><td>MAME autonome.</td><td>Romset du MAME actuel. Pas de placement des boutons jeu par jeu pour le ST-V.</td></tr></tbody></table>

## BIOS

<table><thead><tr><th>Fichier</th><th width="165.75">Dossier</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>stvbios.zip</code></td><td><code>bios</code></td><td>tous les émulateurs sauf Mednafen (le core kronos accepte aussi <code>bios\kronos</code>)</td></tr><tr><td><code>stvbios.zip</code> de la version du core</td><td><code>roms\segastv</code></td><td>anciens cores mame (mame2016, mame2014, mame2010, mame2003_plus, mame2003)</td></tr><tr><td><code>epr-20091.ic8</code> (Japon)</td><td><code>bios</code></td><td>Mednafen</td></tr><tr><td><code>epr-17952a.ic8</code> (États-Unis)</td><td><code>bios</code></td><td>Mednafen</td></tr><tr><td><code>epr-17954a.ic8</code> (Europe)</td><td><code>bios</code></td><td>Mednafen</td></tr></tbody></table>

`stvbios.zip` est le BIOS du ST-V au format MAME. Placé dans `bios`, il sert au core kronos, au core mednafen\_saturn (qui y lit directement le fichier de la région du jeu), au core mame et à MAME. Son contenu dépend de la version de MAME : les anciens cores mame ont besoin du `stvbios.zip` de leur romset, à côté des jeux. Mednafen (émulateur autonome) ne lit pas l'archive : copiez dans `bios` les fichiers `epr-20091.ic8`, `epr-17952a.ic8` et `epr-17954a.ic8`, que vous trouverez dans `stvbios.zip`. Le jeu utilise celui de sa région.

<details>

<summary>Contenu de stvbios.zip</summary>

```
epr-17740.ic8
epr-17740a.ic8
epr-17741a.ic8
epr-17742a.ic8
epr-17951a.ic8
epr-17952a.ic8
epr-17953a.ic8
epr-17954a.ic8
epr-19730.ic8
epr-19854.ic8
epr-20091.ic8
epr-23603.ic8
stv110.bin
stv1061.bin
stvbios.nv
```

</details>

## Quel format de jeu ?

Les jeux sont des archives `.zip` au format MAME, à garder telles quelles, sans les décompresser ni les renommer (`rsgun.zip`, `diehard.zip`, `shienryu.zip`…). Les clones ont besoin du jeu parent dans le même dossier.

Le core kronos, le core mednafen\_saturn, Mednafen, le core mame et MAME utilisent le romset du MAME actuel. Les anciens cores mame (mame2016, mame2014, mame2010, mame2003\_plus, mame2003) ont besoin du romset de leur version.

## Contrôles

### Configuration automatique

<table><thead><tr><th width="242.75">Borne</th><th>Manette</th></tr></thead><tbody><tr><td>Joystick</td><td>Croix directionnelle, stick gauche</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Crédit</td><td>SELECT</td></tr><tr><td>Test / Service</td><td>R3 / L3 (cores mame : clavier, voir plus bas)</td></tr></tbody></table>

* **Cores mednafen\_saturn**, **mame** et **mame2003\_plus** : la position des boutons est définie jeu par jeu, pour retrouver la disposition de la borne (par défaut : boutons 1 à 4 sur OUEST, SUD, EST, NORD, boutons 5 et 6 sur L1 et R1). **CONTRÔLES > DISPOSITION DES BOUTONS** choisit la disposition pour un stick arcade (6 ou 8 boutons). Fichiers utilisés : `libretro_mednafen_saturn_segastv.yml` (core mednafen\_saturn), `libretro_mame.yml` (cores mame et mame2003\_plus), voir la page [**Configuration des touches MAME**](../../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-mame64.md).
* **Core kronos** : boutons 1 à 4 sur SUD, EST, OUEST, NORD ; jeux à 6 boutons : OUEST, NORD, L1, SUD, EST, R1. Test et Service sont actifs par défaut ; **ÉMULATION > ACTIVER LE MENU SERVICE** les désactive.
* **Mednafen** : boutons de la borne sur ceux de la manette Saturn, réglables avec **CONTRÔLES > DISPOSITION DES BOUTONS** et **CONTRÔLES > INVERSER GÂCHETTES ET ÉPAULES**. Test et Service aussi sur `0` et `9` au clavier.
* **MAME** : boutons de la borne dans l'ordre de la manette. Test et Service aussi sur `0` et `9` au clavier ; **CONTRÔLES > TEST/SERVICE SUR L3/R3** les retire de la manette.
* **Cores mame2016**, **mame2014**, **mame2010**, **mame2003** : configuration par défaut du core, sans placement jeu par jeu.
* **Cores mame** (toutes versions) : Test et Service ne sont pas sur la manette ; avec le core mame, utilisez `0` (Test) et `9` (Service) au clavier.

### Raccourcis

Tous les émulateurs utilisent les raccourcis par défaut de RetroBat (sauvegarde, chargement, capture…). Pour plus de détails, voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="259">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS</td><td><code>bios</code> (core kronos : aussi <code>bios\kronos</code> ; anciens cores mame : <code>roms\segastv</code>)</td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><code>saves\segastv\libretro.&#x3C;core></code></td></tr><tr><td>Mappage par jeu (core mednafen_saturn)</td><td><code>system\resources\inputmapping\libretro_mednafen_saturn_segastv.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr></tbody></table>

## Guides

### Menu de test

Le menu de test de la borne permet de régler les crédits, la difficulté ou de vérifier les commandes. En jeu, appuyez sur **R3** (Test) ; **L3** (Service) ajoute un crédit de service. Avec les cores mame, utilisez le clavier (voir [**Contrôles**](sega_stv.md#controles)).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (640).png" alt=""><figcaption></figcaption></figure></div>

### Région du BIOS

La région change la langue et parfois le contenu des jeux (textes, censure).

* **Core kronos** : **ÉMULATION > RÉGION ST-V** (Europe par défaut, USA, Japon, Taïwan). La région est ignorée si le jeu ne la prend pas en charge.
* **Core mame** : **ÉMULATION > BIOS ST-V** choisit la version exacte du BIOS (Japon, Europe, USA, Taïwan, développement).
* **Mednafen**, **core mednafen\_saturn**, **anciens cores mame** : la région suit le jeu.

### Autres options utiles

| Option                                                              | Effet                                                          |
| ------------------------------------------------------------------- | -------------------------------------------------------------- |
| **RÉSOLUTION INTERNE** (core kronos)                                | Rendu en 2x, 4x ou 8x.                                         |
| **RENDU VISUEL > MESH AMÉLIORÉ** (cores kronos et mednafen\_saturn) | Remplace la transparence en damier par une vraie transparence. |
| **RENDU VISUEL > BANDING AMÉLIORÉ** (core kronos)                   | Ombrage de Gouraud au lieu d'un ombrage plat.                  |
| **VIDÉO > MÉTHODE DE DÉSENTRELACEMENT** (core mednafen\_saturn)     | Pour les jeux en haute résolution entrelacée.                  |

## Problèmes connus

<table><thead><tr><th width="362.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le core kronos ne démarre pas le jeu</td><td>Vérifiez <code>stvbios.zip</code> dans <code>bios</code> (ou <code>bios\kronos</code>), et la compatibilité OpenGL 4.3 de la carte graphique.</td></tr><tr><td>Mednafen ne démarre pas le jeu</td><td>Copiez <code>epr-20091.ic8</code>, <code>epr-17952a.ic8</code> et <code>epr-17954a.ic8</code> (dans <code>stvbios.zip</code>) à la racine de <code>bios</code>.</td></tr><tr><td>Le core mednafen_saturn, le core mame ou MAME ne démarre pas le jeu</td><td>Placez <code>stvbios.zip</code> dans <code>bios</code> : <code>bios\kronos</code> ne sert qu'au core kronos.</td></tr><tr><td>Astra Superstars, Decathlete, Final Fight Revenge, Steep Slope Sliders, Tecmo World Cup '98 ou Touryuu Densetsu Elan Doree ne fonctionnent pas avec Mednafen</td><td>Ces jeux ne sont pas pris en charge par Mednafen : utilisez le core kronos ou le core mame.</td></tr><tr><td>Un jeu ne démarre pas avec un ancien core mame</td><td>Utilisez le romset de la version de MAME du core, ou le core mame.</td></tr><tr><td>Test et Service ne répondent pas avec le core kronos</td><td>Vérifiez que <strong>ÉMULATION > ACTIVER LE MENU SERVICE</strong> n'est pas désactivé.</td></tr></tbody></table>
