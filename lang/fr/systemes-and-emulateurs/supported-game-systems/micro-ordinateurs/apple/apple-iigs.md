---
description: Apple
---

# Apple IIGS

<div align="left"><figure><img src="../../../../.gitbook/assets/image (616).png" alt="" width="540"><figcaption></figcaption></figure></div>

### Présentation

L'**Apple IIGS** est le dernier modèle de la gamme Apple II. Sorti en 1986, il repose sur un processeur 16 bits 65C816, une palette de 4 096 couleurs et la puce sonore Ensoniq à 32 voix, la même que dans les synthétiseurs de la marque. Il reste compatible avec les programmes de l'Apple II et lit des disquettes 3,5 pouces de 800 Ko. Sa production s'arrête en 1992.

Parmi ses jeux : **Dungeon Master**, **Silpheed**, **Zany Golf**, **The Immortal**, **Rastan**, **Arkanoid II**, **Out of This World**, **Wolfenstein 3D**, **Xenocide**, **Dragon Wars**.

RetroBat propose trois émulateurs : **GSplus** (par défaut), le core libretro **mame** et **MAME**.

{% embed url="https://fr.wikipedia.org/wiki/Apple_IIGS" %}

### En bref

<table><thead><tr><th width="261.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\apple2gs</code></td></tr><tr><td><strong>Extensions</strong></td><td>.2mg .woz .m3u .hdv .zip</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>gsplus</td></tr><tr><td><strong>BIOS</strong></td><td>ROM de l'Apple IIGS dans <code>bios</code> : <code>APPLE2GS.ROM</code> (ou <code>ROM</code>, <code>ROM.01</code>, <code>ROM.03</code>) pour GSplus, <code>apple2gs.zip</code> pour MAME</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>GSplus : la première manette sert de joystick ; MAME : PadToKey</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core libretro mame</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core libretro mame</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>votrsc01a.zip</code> et listes logicielles MAME</td></tr></tbody></table>

### Quel émulateur choisir ?

<table><thead><tr><th width="162">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>gsplus</strong> (défaut)</td><td>Léger et rapide, monte tous les disques d'un <code>.m3u</code> en même temps, disques durs, scanlines.</td><td>Ne lit pas les <code>.woz</code>. Pas de sauvegardes instantanées gérées par RetroBat.</td></tr><tr><td><strong>libretro: mame</strong></td><td>Lit les <code>.woz</code>, sauvegardes instantanées, shaders et raccourcis de RetroArch, listes logicielles MAME.</td><td>Demande <code>apple2gs.zip</code>. Pas de configuration automatique de la manette.</td></tr><tr><td><strong>mame</strong></td><td>Même émulation que le core mame, en émulateur autonome.</td><td>Demande <code>apple2gs.zip</code>. Pas de configuration automatique de la manette.</td></tr></tbody></table>

### BIOS

<table><thead><tr><th width="177">Émulateur</th><th>Fichiers</th><th>Dossier</th></tr></thead><tbody><tr><td>GSplus</td><td>ROM de l'Apple IIGS (ROM 01 ou ROM 03) sous l'un de ces noms : <code>ROM</code>, <code>ROM.01</code>, <code>ROM.03</code> ou <code>APPLE2GS.ROM</code></td><td><code>bios</code></td></tr><tr><td>MAME, core mame</td><td><code>apple2gs.zip</code> ; <code>votrsc01a.zip</code> en option</td><td><code>bios</code></td></tr></tbody></table>

Si plusieurs ROM sont présentes, GSplus prend la première trouvée dans l'ordre `ROM`, `ROM.01`, `ROM.03`, `APPLE2GS.ROM`. Le fichier `APPLE2GS.ROM` contrôlé par RetroBat a pour md5 `20a0334c447cb069a040ae5be1d938df`.

Les listes logicielles MAME (`apple2gs_flop_clcracked.xml`, `apple2gs_flop_misc.xml`, `apple2gs_flop_orig.xml`) vont dans `bios\mame\hash`.

<details>

<summary>Contenu de apple2gs.zip</summary>

```
"apple2gs.zip"
- "341-0728" size="131072" crc="8d410067" sha1="c0f4704233ead14cb8e1e8a68fbd7063c56afd27"
- "341-0748" size="131072" crc="18190283" sha1="c70576869deec92ca82c78438b1d5c686eac7480"
- "341s0632-2.bin" size="4096" crc="e1c11fb0" sha1="141d18c36a617ab9dce668445440d34354be0672"
- "344s0047.bin" size="16384" crc="2d541944" sha1="5a5a77c8ec45632aea1a57cd9c9257f7f6e44668"
```

</details>

### Quel format de jeu ?

<table><thead><tr><th width="119">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.2mg</strong></td><td>Image de disquette 3,5 pouces (800 Ko) ou de disque dur. Le format le plus courant.</td></tr><tr><td><strong>.woz</strong></td><td>Copie fidèle de la disquette, protections comprises. Lu uniquement par MAME et le core mame.</td></tr><tr><td><strong>.hdv</strong></td><td>Image de disque dur ProDOS.</td></tr><tr><td><strong>.m3u</strong></td><td>Liste des disques d'un jeu sur plusieurs disquettes.</td></tr><tr><td><strong>.zip</strong></td><td>Archive contenant l'image du jeu.</td></tr></tbody></table>

### Contrôles

#### Configuration par émulateur

L'Apple IIGS se joue au clavier, à la souris et au joystick analogique à deux boutons. Pour les touches du clavier, créez un profil **PadToKey** (voir la page [**PadToKey**](../../../../controleurs/pad2key.md)).

* **GSplus** : la première manette branchée sert de joystick (stick analogique et deux boutons). La souris de l'Apple IIGS suit la souris du PC. **CONTRÔLES > INTERVERTIR LES PADDLES** et **INVERSER LES PADDLES** pour les quelques jeux qui attendent les axes dans l'autre sens.
* **MAME, core mame** : **CONTRÔLES > TYPE DE JOYSTICK** (Apple ou Gizmo).

#### Raccourcis

**Core mame, MAME** : raccourcis par défaut de RetroBat (sauvegarde, chargement, capture…). Pour plus de détails, voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

**GSplus**

| Raccourci          | Action  |
| ------------------ | ------- |
| **HOTKEY + START** | Quitter |

Au clavier, `F4` ouvre le menu de configuration de GSplus.

### Écriture sur les disquettes

Avec GSplus, l'option **ÉMULATION > AUTORISER LES JEUX À ÉCRIRE SUR LES IMAGES DISQUE** décide si un jeu peut enregistrer sur sa disquette :

<table><thead><tr><th width="332.75">Choix</th><th>Effet</th></tr></thead><tbody><tr><td><strong>NON (LECTURE SEULE)</strong> (défaut)</td><td>La disquette est protégée en écriture : le jeu ne peut pas enregistrer.</td></tr><tr><td><strong>OUI (COPIE DE TRAVAIL DANS SAVES)</strong></td><td>Le jeu tourne sur une copie de la disquette, créée au premier lancement dans <code>saves\apple2gs\gsplus</code> puis réutilisée : la progression est gardée d'une partie à l'autre.</td></tr><tr><td><strong>OUI ET RÉINITIALISER LE DISQUE</strong></td><td>Repart de la disquette d'origine (l'ancienne copie est gardée en <code>.bak</code>).</td></tr></tbody></table>

Les fichiers de `roms\apple2gs` ne sont jamais modifiés.

### Dossiers

| Contenu                                   | Dossier                        |
| ----------------------------------------- | ------------------------------ |
| ROM                                       | `bios`                         |
| Listes logicielles MAME                   | `bios\mame\hash`               |
| GSplus : copies de travail des disquettes | `saves\apple2gs\gsplus`        |
| GSplus : configuration                    | `emulators\gsplus\config.txt`  |
| GSplus : captures d'écran                 | `screenshots`                  |
| Core mame : sauvegardes instantanées      | `saves\apple2gs\libretro.mame` |

### Guides

#### Jeux sur plusieurs disquettes

Créez un fichier `.m3u` dans `roms\apple2gs`, avec une ligne par disquette, dans l'ordre. Les images doivent être dans le même dossier que le `.m3u`. Exemple pour Silpheed :

* **GSplus** monte toutes les disquettes en même temps : le jeu trouve lui-même le disque suivant, sans manipulation.
* **MAME** et le **core mame** chargent les deux premières disquettes dans les deux lecteurs 3,5 pouces.

#### Le jeu ne démarre pas avec GSplus

GSplus choisit le lecteur d'après la taille de l'image : les disquettes 5,25 pouces vont dans le slot 6, les disquettes 3,5 pouces et les disques durs dans le slot 7. Si un jeu refuse de démarrer, essayez un autre choix dans **ÉMULATION > SLOT DU DISQUE**.

#### Autres options utiles

| Option                                                | Effet                                                     |
| ----------------------------------------------------- | --------------------------------------------------------- |
| **RENDU VISUEL > SCANLINES** (GSplus)                 | Aspect d'un écran cathodique, de léger à fort.            |
| **RENDU VISUEL > IGNORER LE FORMAT D'IMAGE** (GSplus) | Image étirée sur tout l'écran.                            |
| **RENDU VISUEL > NOIR ET BLANC** (GSplus)             | Affichage d'un moniteur monochrome.                       |
| **ÉMULATION > TAILLE DE LA MÉMOIRE RAM** (MAME)       | De 1 à 8 Mo.                                              |
| **SLOTS D'EXTENSION** (MAME)                          | Carte son Mockingboard, carte joystick 4play, carte MIDI. |

### Problèmes connus

<table><thead><tr><th width="345.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Un <code>.woz</code> ne démarre pas avec GSplus</td><td>GSplus ne lit pas ce format : choisissez le core mame ou MAME pour ce jeu.</td></tr><tr><td>GSplus démarre sur un écran vide ou sans système</td><td>Vérifiez la ROM de l'Apple IIGS dans <code>bios</code> (voir <a href="apple-iigs.md#bios"><strong>BIOS</strong></a>).</td></tr><tr><td>Un jeu refuse de démarrer avec GSplus</td><td>Changez <strong>ÉMULATION > SLOT DU DISQUE</strong>.</td></tr><tr><td>Le jeu ne garde pas la partie</td><td>Activez <strong>ÉMULATION > AUTORISER LES JEUX À ÉCRIRE SUR LES IMAGES DISQUE</strong> (GSplus).</td></tr></tbody></table>
