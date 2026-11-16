---
description: Apple
---

# Apple II

<div align="left"><figure><img src="../../../../.gitbook/assets/image (615).png" alt="" width="424"><figcaption></figcaption></figure></div>

## Présentation

L'**Apple II** est l'un des premiers micro-ordinateurs personnels vendus en grand nombre. Conçu par Steve Wozniak, il sort en 1977, suivi de l'Apple II Plus (1979), de l'Apple //e (1983, puis sa version « Enhanced » en 1985) et des portables //c et //c Plus. Sa production s'arrête en 1993. Ses programmes tiennent sur des disquettes 5,25 pouces, lues par le lecteur Disk II.

Sa ludothèque est immense : **Lode Runner**, **Karateka**, **Prince of Persia**, **Ultima**, **Wizardry**, **Choplifter**, **The Oregon Trail**, **Castle Wolfenstein**, **Conan**, ainsi que de nombreuses démos européennes récentes.

RetroBat propose sept émulateurs : **AppleWin** (par défaut), **POM2**, **Mednafen**, **BizHawk**, les cores libretro **applewin** et **mame**, et **MAME**.

{% embed url="https://fr.wikipedia.org/wiki/Apple_II" %}

## En bref

<table><thead><tr><th width="266.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\apple2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nib .do .po .dsk .woz .m3u .hdv .zip</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>applewin</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun pour AppleWin et le core applewin</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique : Mednafen, core applewin ; AppleWin utilise la manette Windows ; POM2, BizHawk, MAME : PadToKey</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk (gérées par RetroBat)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core libretro mame</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>ROM POM2 dans <code>bios\pom2</code>, ROM Mednafen et BizHawk, archives MAME dans <code>bios</code></td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="212">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>applewin</strong> (défaut)</td><td>La référence sous Windows : très compatible, ROM intégrées, nombreux types d'écran.</td><td>Ne lit pas les <code>.zip</code>. Sauvegardes instantanées non gérées par RetroBat. Réglages enregistrés dans le registre Windows.</td></tr><tr><td><strong>pom2</strong></td><td>Émulateur récent : //e, //c, //c Plus et modèles PAL (50 Hz) pour les démos européennes, filtres CRT, turbo disque, souris en paddles.</td><td>Demande les ROM dans <code>bios\pom2</code>. Un seul disque monté à la fois, pas de sauvegardes instantanées.</td></tr><tr><td><strong>mednafen</strong></td><td>Apple II, II+ et //e, manette configurée automatiquement.</td><td>Demande ses ROM dans <code>bios</code>. Ne lit pas les <code>.zip</code>.</td></tr><tr><td><strong>bizhawk</strong></td><td>Sauvegardes instantanées gérées par RetroBat, RetroAchievements.</td><td>Demande <code>AppleIIe.rom</code> et <code>AppleIIe_DiskII.rom</code>. Clavier seulement. Ne lit pas les <code>.zip</code>.</td></tr><tr><td><strong>libretro: applewin</strong></td><td>AppleWin dans RetroArch : sauvegardes instantanées, shaders, changement de disque, cartes d'extension.</td><td>—</td></tr><tr><td><strong>libretro: mame</strong>, <strong>mame</strong></td><td>Listes logicielles MAME, nombreuses cartes d'extension.</td><td>Demandent les archives MAME. Pas de configuration automatique de la manette.</td></tr></tbody></table>

## BIOS

**AppleWin** et le **core applewin** ont leurs ROM intégrées : rien à installer. Les autres émulateurs ont besoin de leurs propres fichiers, tous dans `bios` :

<table><thead><tr><th width="183.25">Émulateur</th><th>Fichiers</th><th>Dossier</th></tr></thead><tbody><tr><td>POM2</td><td>ROM de la machine choisie et de son générateur de caractères, plus <code>disk2.rom</code> et <code>diskii_p6.rom</code> (voir ci-dessous)</td><td><code>bios\pom2</code></td></tr><tr><td>Mednafen</td><td><code>apple2-asoft-auto.rom</code>, <code>apple2-int-auto.rom</code>, <code>disk2-13boot.rom</code>, <code>disk2-13seq.rom</code>, <code>disk2-16boot.rom</code>, <code>disk2-16seq.rom</code></td><td><code>bios</code></td></tr><tr><td>BizHawk</td><td><code>AppleIIe.rom</code>, <code>AppleIIe_DiskII.rom</code></td><td><code>bios</code></td></tr><tr><td>MAME, core mame</td><td><code>apple2ee.zip</code> et <code>apple2e.zip</code> (Apple //e Enhanced, modèle par défaut), <code>apple2.zip</code>, <code>apple2p.zip</code>, <code>a2diskiing.zip</code>, <code>d2fdc.zip</code>, <code>votrsc01a.zip</code> ; <code>a2cffa2.zip</code> pour les disques durs <code>.hdv</code></td><td><code>bios</code></td></tr></tbody></table>

Les listes logicielles MAME (`apple2_cass.xml`, `apple2_flop_clcracked.xml`, `apple2_flop_misc.xml`, `apple2_flop_orig.xml`) vont dans `bios\mame\hash`.

**ROM POM2** (noms de POM2) :

<table><thead><tr><th width="198.25">Machine</th><th>ROM système</th><th>ROM de caractères</th></tr></thead><tbody><tr><td>Apple //e Enhanced (défaut)</td><td><code>apple2e.rom</code></td><td><code>apple2e_char.rom</code></td></tr><tr><td>Apple ][</td><td><code>apple2o.rom</code> ou <code>apple2.rom</code></td><td><code>apple2_char.rom</code></td></tr><tr><td>Apple ][+</td><td><code>apple2p.rom</code> ou <code>apple2.rom</code></td><td><code>apple2_char.rom</code></td></tr><tr><td>Apple //e Unenhanced</td><td><code>apple2e_unenh.rom</code> ou <code>342-0135-b.64.rom</code></td><td><code>apple2e_char_2k.rom</code> ou <code>342-0133-a.chr.rom</code></td></tr><tr><td>Apple //c</td><td><code>apple2c-32Kv0.rom</code>, <code>apple2c-16K.rom</code> ou <code>3420033a.256</code></td><td><code>apple2e_char.rom</code></td></tr><tr><td>Apple //c Plus</td><td><code>apple2cp.rom</code> ou <code>apple2c-plus.rom</code></td><td><code>apple2e_char.rom</code></td></tr></tbody></table>

Toutes les machines ont aussi besoin de `diskii_p6.rom`, et toutes sauf les //c de `disk2.rom`. RetroBat copie les ROM de `bios\pom2` dans le dossier de POM2 et affiche le nom du fichier manquant si une ROM n'est pas trouvée.

## Quel format de jeu ?

<table><thead><tr><th width="202.75">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.woz</strong></td><td>Copie fidèle de la disquette, protections comprises. Le format le plus sûr pour les jeux protégés.</td></tr><tr><td><strong>.dsk</strong>, <strong>.do</strong>, <strong>.po</strong></td><td>Images de disquettes 5,25 pouces (ordre DOS 3.3 ou ProDOS).</td></tr><tr><td><strong>.nib</strong></td><td>Image « nibble » de disquette 5,25 pouces.</td></tr><tr><td><strong>.hdv</strong></td><td>Image de disque dur ProDOS.</td></tr><tr><td><strong>.m3u</strong></td><td>Liste des disques d'un jeu sur plusieurs disquettes.</td></tr><tr><td><strong>.zip</strong></td><td>Seuls POM2 et MAME lisent les archives.</td></tr></tbody></table>

## Contrôles

### Configuration par émulateur

L'Apple II se pilote surtout au clavier. Pour jouer à la manette, créez un profil **PadToKey** (voir la page [**PadToKey**](../../../../controleurs/pad2key.md)). Le port jeu de l'Apple II reçoit un joystick analogique à deux boutons, ou deux paddles.

* **AppleWin** : la première manette Windows sert de joystick (sinon les flèches du clavier). **CONTRÔLES > TYPE DE JOYSTICK JOUEUR 1** / **JOUEUR 2** : joystick, clavier (flèches ou pavé numérique) ou souris.
* **Core applewin** : **CONTRÔLES > PÉRIPHÉRIQUE JOUEUR 1** : manette avec la croix (par défaut), manette avec le stick analogique (mouvement progressif, pour les paddles), ou souris comme paddles. **TYPE DE CLAVIER** : ASCII (par défaut) ou clavier d'origine de la machine. **FOCUS CLAVIER** donne tout le clavier au jeu (Arrêt défil pour basculer).
* **Mednafen** : manette configurée automatiquement, SUD / EST = boutons 1 / 2, L1 = choix de la résistance des paddles. **CONTRÔLES > TYPE DE CONTRÔLEUR** : joystick (stick analogique), manette (croix) ou joystick Atari.
* **POM2** : **CONTRÔLES > MANETTE DU PORT JEU** choisit la manette (automatique par défaut). **LA SOURIS PILOTE LES PADDLES** pour Arkanoid, Breakout et les jeux à paddles, **COURSE DU PADDLE SOURIS**, **ZONE MORTE DU STICK**.
* **BizHawk** : clavier de l'Apple //e uniquement.
* **MAME, core mame** : **CONTRÔLES > TYPE DE JOYSTICK** (Apple, Sirius / Atari pour l'Apple II Plus, Gizmo).

### Raccourcis

#### **Cores libretro, Mednafen, BizHawk, MAME**

Raccourcis par défaut de RetroBat (sauvegarde, chargement, capture…). Pour plus de détails, voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

#### **AppleWin, POM2**

| Raccourci          | Action  |
| ------------------ | ------- |
| **HOTKEY + START** | Quitter |

AppleWin garde ses propres touches au clavier : `F11` / `F12` sauvegardent et chargent un instantané (non géré par RetroBat).

## Écriture sur les disquettes

Beaucoup de jeux Apple II enregistrent la partie directement sur leur disquette. RetroBat ne modifie jamais les fichiers de `roms\apple2`. L'option **ÉMULATION > AUTORISER LES JEUX À ÉCRIRE SUR LES IMAGES DISQUE** (AppleWin, core applewin, POM2, Mednafen, BizHawk) décide de ce qui se passe :

| Choix                                 | Effet                                                                                                                                                                       |
| ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **NON (LECTURE SEULE)** (défaut)      | La disquette est protégée en écriture : le jeu ne peut pas enregistrer.                                                                                                     |
| **OUI (COPIE DE TRAVAIL DANS SAVES)** | Le jeu tourne sur une copie de la disquette, créée au premier lancement dans `saves\apple2\<émulateur>` puis réutilisée : la progression est gardée d'une partie à l'autre. |
| **OUI ET RÉINITIALISER LE DISQUE**    | Repart de la disquette d'origine (l'ancienne copie est gardée en `.bak`).                                                                                                   |

Mednafen et BizHawk gardent les modifications dans leurs propres fichiers au lieu d'une copie de la disquette : la réinitialisation les met de côté de la même façon.

## Dossiers

<table><thead><tr><th width="357.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>ROM (POM2)</td><td><code>bios\pom2</code></td></tr><tr><td>ROM (Mednafen, BizHawk, MAME)</td><td><code>bios</code></td></tr><tr><td>AppleWin : copies de travail des disquettes</td><td><code>saves\apple2\applewin</code></td></tr><tr><td>AppleWin : configuration</td><td>Registre Windows (<code>HKEY_CURRENT_USER\SOFTWARE\AppleWin</code>)</td></tr><tr><td>Core applewin : copies de travail des disquettes</td><td><code>saves\apple2</code></td></tr><tr><td>Core applewin : sauvegardes instantanées</td><td><code>saves\apple2\libretro.applewin</code></td></tr><tr><td>POM2 : copies de travail des disquettes</td><td><code>saves\apple2\pom2</code></td></tr><tr><td>POM2 : configuration</td><td><code>emulators\pom2\POM2\state.cfg</code></td></tr><tr><td>Mednafen : modifications des disquettes</td><td><code>saves\apple2</code> (<code>&#x3C;jeu>.&#x3C;n>.afd.gz</code>, <code>&#x3C;jeu>.0.ahd.gz</code>)</td></tr><tr><td>BizHawk : modifications des disquettes</td><td><code>saves\apple2\bizhawk</code> (<code>&#x3C;jeu>.SaveRAM</code>)</td></tr><tr><td>BizHawk : sauvegardes instantanées</td><td><code>saves\apple2\bizhawk\sstates\AppleII</code></td></tr><tr><td>Listes logicielles MAME</td><td><code>bios\mame\hash</code></td></tr></tbody></table>

## Guides

### Jeux sur plusieurs disquettes

Créez un fichier `.m3u` dans `roms\apple2`, avec une ligne par disquette, dans l'ordre :

```
Ultima IV (Disk 1).woz
Ultima IV (Disk 2).woz
```

* **AppleWin** et **MAME** chargent les deux premières disquettes dans les lecteurs 1 et 2.
* **Core applewin** : changement de disque avec les raccourcis RetroArch ; **ÉMULATION > UTILISER LES DEUX LECTEURS DE DISQUETTES** charge les deux premières dans les lecteurs 1 et 2, **DISQUE DE DÉMARRAGE M3U** repart du dernier disque utilisé.
* **POM2** monte un seul disque : **ÉMULATION > NUMÉRO DE DISQUE (M3U)** choisit celui du démarrage, les autres se changent depuis le menu du jeu.

### Démos européennes (50 Hz)

Certaines démos et quelques programmes européens ont été écrits pour un Apple //e PAL. Choisissez un modèle PAL dans POM2 (**ÉMULATION > MACHINE ÉMULÉE**), ou **ÉMULATION > FRÉQUENCE DE RAFRAÎCHISSEMENT VIDÉO** sur 50 Hz avec le core applewin.

### Disques durs (.hdv)

AppleWin et le core applewin lisent les `.hdv` grâce au contrôleur de disque dur du slot 7 (activé par défaut). Avec MAME et le core mame, ajoutez `a2cffa2.zip` dans `bios` et choisissez **ÉMULATION > FORCER LE TYPE DE MÉDIA > Image de disque dur** : RetroBat installe alors la carte CFFA 2.0 dans le slot 7.

### Autres options utiles

| Option                                                                         | Effet                                                                                                        |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| **ÉMULATION > MACHINE ÉMULÉE**                                                 | Modèle d'Apple II (AppleWin, core applewin, POM2).                                                           |
| **RENDU VISUEL > TYPE D'ÉCRAN**                                                | Couleur RGB, composite (couleurs baveuses d'époque), télévision ou moniteur monochrome vert / ambre / blanc. |
| **RENDU VISUEL > SCANLINES** (core applewin), **EFFETS CRT** (POM2)            | Aspect d'un écran cathodique.                                                                                |
| **SLOTS D'EXTENSION > SLOT 4** (core applewin), **CARTE SON DU SLOT 4** (POM2) | Carte son Mockingboard (par défaut), Phasor, carte souris…                                                   |
| **ÉMULATION > TURBO DISQUE** (POM2)                                            | Chargements beaucoup plus rapides.                                                                           |
| **ÉMULATION > ROM DE CARACTÈRES** (POM2)                                       | Jeu de caractères français, britannique, allemand…                                                           |

## Problèmes connus

| Problème                                                       | Solution                                                                           |
| -------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Le jeu affiche une erreur d'écriture ou ne garde pas la partie | Activez **ÉMULATION > AUTORISER LES JEUX À ÉCRIRE SUR LES IMAGES DISQUE**.         |
| Un `.zip` ne se lance pas avec AppleWin, Mednafen ou BizHawk   | Ces émulateurs ne lisent pas les archives : décompressez le jeu, ou utilisez POM2. |
| POM2 indique « Missing POM2 ROM »                              | Ajoutez la ROM indiquée dans `bios\pom2`.                                          |
| Un jeu protégé ne démarre pas                                  | Utilisez la version `.woz` du jeu.                                                 |
| Le jeu ne réagit pas à la manette                              | Créez un profil PadToKey, ou vérifiez le type de joystick de l'émulateur.          |
