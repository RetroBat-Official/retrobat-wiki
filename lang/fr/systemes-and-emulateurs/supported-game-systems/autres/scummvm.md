---
description: ScummVM Team
---

# ScummVM

<div align="left"><figure><img src="../../../.gitbook/assets/image (529).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

**ScummVM** n'est pas un émulateur : c'est un programme qui remplace l'exécutable d'origine de centaines de jeux d'aventure et de rôle, pour les faire tourner sur les machines actuelles. Il faut donc posséder les fichiers de données des jeux.

Le projet naît en 2001 pour relancer les jeux LucasArts écrits avec le moteur SCUMM, créé en 1987 pour Maniac Mansion : Monkey Island, Day of the Tentacle, Sam & Max, Full Throttle… D'où son nom. Il s'est ouvert depuis à beaucoup d'autres moteurs : Sierra (King's Quest, Space Quest), Revolution (Les Chevaliers de Baphomet, Beneath a Steel Sky), Westwood (Kyrandia), Cyan (Myst, Riven)… Depuis sa fusion avec ResidualVM en 2020, il lance aussi des jeux en 3D comme Grim Fandango.

Quelques jeux sont offerts par leurs éditeurs et se téléchargent sur le site de ScummVM, par exemple Beneath a Steel Sky, Flight of the Amazon Queen ou Lure of the Temptress.

{% embed url="https://fr.wikipedia.org/wiki/ScummVM" %}

## En bref

<table><thead><tr><th width="276.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\scummvm</code></td></tr><tr><td><strong>Extensions</strong></td><td>.scummvm .7z .zip .rar .squashfs</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: scummvm</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun obligatoire</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (scummvm : gérée par ScummVM)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>MT32_CONTROL.ROM</code> et <code>MT32_PCM.ROM</code> dans <code>bios\scummvm\extra</code> (musique Roland MT-32)</td></tr></tbody></table>

## Quel émulateur choisir ?

Les deux émulateurs utilisent la même version de ScummVM et partagent leurs sauvegardes.

<table><thead><tr><th width="184.5">Émulateur</th><th width="314.75">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: scummvm</strong> (défaut)</td><td>ScummVM dans RetroArch : manettes configurées par RetroBat, shaders, décorations, raccourcis habituels, réglage du curseur à la manette.</td><td>Le fichier <code>.scummvm</code> doit contenir l'identifiant du jeu.</td></tr><tr><td><strong>scummvm</strong></td><td>Reconnaît le jeu tout seul si le fichier <code>.scummvm</code> est vide. Plus d'options d'affichage : filtres de mise à l'échelle, rendu EGA / CGA / Amiga…, rotation de l'écran.</td><td>Les manettes ne sont pas configurées par RetroBat. Un seul raccourci à la manette : quitter.</td></tr></tbody></table>

## BIOS

ScummVM n'a besoin d'aucun BIOS. Deux fichiers optionnels permettent d'entendre la musique des jeux prévus pour le synthétiseur **Roland MT-32** :

<table><thead><tr><th width="170.75">Fichier</th><th width="315.5">MD5</th><th>Emplacement</th></tr></thead><tbody><tr><td><code>MT32_CONTROL.ROM</code></td><td><code>5626206284b22c2734f3e9efefcd2675</code></td><td><code>bios\scummvm\extra</code></td></tr><tr><td><code>MT32_PCM.ROM</code></td><td><code>89e42e386e82e0cacb4a2704a03706ca</code></td><td><code>bios\scummvm\extra</code></td></tr></tbody></table>

Ils sont utilisés quand l'option **AUDIO > MODE SON** est réglée sur **MT-32 émulé**.

Les fichiers de données de ScummVM (dossier `bios\scummvm\extra`), ses thèmes (`bios\scummvm\theme`) et le soundfont `Roland_SC-55.sf2` sont fournis avec RetroBat.

## Quel format de jeu ?

Un jeu ScummVM est un **dossier** qui contient les fichiers du jeu d'origine. RetroBat le lance grâce à un petit fichier texte `.scummvm` placé dans ce dossier.

<table><thead><tr><th width="289">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>Dossier du jeu + fichier <code>.scummvm</code></strong></td><td>Le format conseillé : <code>roms\scummvm\Full Throttle\Full Throttle.scummvm</code>. Le fichier contient l'identifiant du jeu sur sa première ligne (voir Guides).</td></tr><tr><td>.7z, .zip, .rar, .squashfs</td><td>Le dossier du jeu compressé, avec son fichier <code>.scummvm</code> à la racine de l'archive. RetroBat monte ou extrait l'archive au lancement.</td></tr></tbody></table>

Le nom du fichier `.scummvm` est celui que RetroBat affiche dans la liste des jeux.

Avec l'émulateur **scummvm**, le fichier `.scummvm` peut rester vide (ou être absent d'une archive) : ScummVM reconnaît alors le jeu présent dans le dossier.

## Contrôles

### Configuration automatique

Les jeux ScummVM se jouent à la souris et au clavier. La souris fonctionne avec les deux émulateurs, et la manette déplace le curseur.

**libretro: scummvm** : RetroBat configure les manettes. Le core utilise ces boutons par défaut :

<table><thead><tr><th width="314">Manette</th><th>Action</th></tr></thead><tbody><tr><td>Croix directionnelle, stick gauche</td><td>Déplacer le curseur</td></tr><tr><td>L1</td><td>Clic gauche</td></tr><tr><td>R1</td><td>Clic droit</td></tr><tr><td>R2 (maintenu)</td><td>Curseur lent, pour plus de précision</td></tr><tr><td>SUD</td><td>ENTRÉE</td></tr><tr><td>EST</td><td>ESPACE (pause)</td></tr><tr><td>NORD</td><td>F5 (menu du jeu)</td></tr><tr><td>OUEST</td><td>ÉCHAP (passer une scène)</td></tr><tr><td>Stick droit</td><td>Flèches du clavier</td></tr><tr><td>START</td><td>Menu de ScummVM</td></tr><tr><td>SELECT</td><td>Clavier virtuel</td></tr></tbody></table>

Ces boutons se changent dans les options du core de RetroArch (catégorie RetroPad). Options utiles, dans **CONTRÔLES** :

<table><thead><tr><th width="331.5">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>PÉRIPHÉRIQUE DE POINTAGE</strong></td><td>Ce qui déplace le curseur : manette et souris (par défaut), manette uniquement, ou manette et pointeur (écran tactile).</td></tr><tr><td><strong>VITESSE DU CURSEUR À LA MANETTE</strong></td><td>1.0 par défaut, prévu pour les jeux en 320x200. Montez à 2.0 pour les jeux en 640x480.</td></tr><tr><td><strong>ZONE MORTE ANALOGIQUE</strong></td><td>À augmenter si le curseur bouge tout seul.</td></tr><tr><td><strong>FOCUS CLAVIER</strong></td><td>Réserve tout le clavier au jeu et désactive les raccourcis clavier de RetroArch.</td></tr></tbody></table>

**scummvm** : RetroBat ne configure pas les manettes, ScummVM les reconnaît lui-même. Boutons par défaut :

<table><thead><tr><th width="272.75">Manette</th><th>Action</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Déplacer le curseur</td></tr><tr><td>R1 (maintenu)</td><td>Curseur lent</td></tr><tr><td>SUD</td><td>Clic gauche</td></tr><tr><td>EST</td><td>Clic droit</td></tr><tr><td>NORD</td><td>Passer une scène (ÉCHAP)</td></tr><tr><td>OUEST</td><td>Passer une ligne de dialogue</td></tr><tr><td>L1</td><td>Menu du jeu (F5)</td></tr><tr><td>Croix directionnelle</td><td>Directions</td></tr><tr><td>START</td><td>Menu de ScummVM</td></tr><tr><td>SELECT</td><td>Clavier virtuel</td></tr></tbody></table>

Certains moteurs de jeu définissent leurs propres boutons. Tout se règle dans ScummVM : **Options Globales > Config. Touches**.

Pour associer d'autres touches du clavier à la manette, créez un profil depuis les options du jeu dans RetroBat : **CRÉER UN PROFIL PADTOKEY** (les deux émulateurs). Pour plus de détails, voir la page [**Pad2Key**](../../../controleurs/pad2key.md).

### Raccourcis

| Action                                          | libretro: scummvm | scummvm        | Clavier (scummvm) |
| ----------------------------------------------- | ----------------- | -------------- | ----------------- |
| **Quitter**                                     | HOTKEY + START    | HOTKEY + START | CTRL + Q          |
| Menu de ScummVM (sauvegarder, charger, options) | START             | START          | CTRL + F5         |
| Clavier virtuel                                 | SELECT            | SELECT         | CTRL + F7         |
| Menu de RetroArch                               | HOTKEY + SUD      | —              | —                 |
| Capture d'écran                                 | HOTKEY + R3       | —              | ALT + S           |
| Avance rapide                                   | HOTKEY + DROITE   | —              | —                 |
| Plein écran                                     | —                 | —              | ALT + ENTRÉE      |
| Couper le son                                   | —                 | —              | CTRL + U          |

Le core libretro ne gère ni les sauvegardes instantanées ni le retour en arrière : ces raccourcis sont sans effet.

## Dossiers

| Contenu                                          | Dossier                         |
| ------------------------------------------------ | ------------------------------- |
| Jeux                                             | `roms\scummvm`                  |
| Sauvegardes (communes aux deux émulateurs)       | `saves\scummvm`                 |
| Fichiers de données, soundfonts, ROM MT-32       | `bios\scummvm\extra`            |
| Thèmes de ScummVM                                | `bios\scummvm\theme`            |
| Configuration et jeux ajoutés, libretro: scummvm | `bios\scummvm.ini`              |
| Configuration et jeux ajoutés, scummvm           | `emulators\scummvm\scummvm.ini` |
| Journal de l'émulateur scummvm                   | `emulators\scummvm\scummvm.log` |
| Captures d'écran                                 | `screenshots`                   |

## Guides

### Ajouter un jeu

1. Copiez le dossier du jeu dans `roms\scummvm`, par exemple `roms\scummvm\Full Throttle`.
2. Dans ce dossier, créez un fichier texte au nom du jeu : `Full Throttle.txt`.
3. Écrivez l'identifiant du jeu sur la première ligne, par exemple :

```
scumm:ft
```

4. Remplacez l'extension `.txt` par `.scummvm` : `Full Throttle.scummvm`.
5. Mettez à jour la liste des jeux de RetroBat.

L'identifiant se trouve dans la liste de compatibilité du site de ScummVM ([scummvm.org/compatibility](https://www.scummvm.org/compatibility/)), sous la forme `moteur:jeu`. Quelques exemples :

<table><thead><tr><th width="271.5">Jeu</th><th>Identifiant</th></tr></thead><tbody><tr><td>The Secret of Monkey Island</td><td><code>scumm:monkey</code></td></tr><tr><td>Day of the Tentacle</td><td><code>scumm:tentacle</code></td></tr><tr><td>Sam &#x26; Max Hit the Road</td><td><code>scumm:samnmax</code></td></tr><tr><td>Beneath a Steel Sky</td><td><code>sky:sky</code></td></tr><tr><td>Les Chevaliers de Baphomet</td><td><code>sword1:sword1</code></td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (531).png" alt=""><figcaption></figcaption></figure></div>

### Choisir une version ou régler un jeu dans ScummVM

Quand un dossier contient plusieurs versions d'un jeu (disquette et CD, plusieurs langues), ou pour garder des réglages propres à un jeu, ajoutez le jeu dans ScummVM :

1. Dans le système **RetroBat**, lancez **ScummVM** ou **ScummVM Libretro**, selon l'émulateur utilisé.

<div align="left"><figure><img src="../../../.gitbook/assets/image (532).png" alt=""><figcaption></figcaption></figure></div>

2. Cliquez sur **Ajouter**, choisissez le dossier du jeu puis la version voulue.

<div align="left"><figure><img src="../../../.gitbook/assets/image (533).png" alt=""><figcaption></figcaption></figure></div>

3. Dans les options du jeu, relevez ou modifiez le champ **ID**, par exemple `ft-cd-fr`, et réglez le jeu (langue, sous-titres…).

<div align="left"><figure><img src="../../../.gitbook/assets/image (534).png" alt=""><figcaption></figcaption></figure></div>

4. Dans le dossier du jeu, créez un fichier `.scummvm` qui contient exactement cet ID.

<div align="left"><figure><img src="../../../.gitbook/assets/image (535).png" alt=""><figcaption></figcaption></figure></div>

Chaque émulateur garde sa propre liste de jeux : un jeu ajouté dans ScummVM n'est pas connu de ScummVM Libretro, et inversement.

### Jeu compressé

Compressez le **contenu** du dossier du jeu, fichier `.scummvm` compris, pour que ce fichier soit à la racine de l'archive. Placez l'archive dans `roms\scummvm`.

### Musique : MT-32, AdLib ou General MIDI

Par défaut, ScummVM choisit lui-même le rendu sonore de chaque jeu. L'option **AUDIO > MODE SON** permet de l'imposer :

<table><thead><tr><th width="160.25">Choix</th><th>Rendu</th></tr></thead><tbody><tr><td><strong>FluidSynth</strong></td><td>General MIDI, joué avec le soundfont choisi dans <strong>SOUNDFONT MIDI</strong>.</td></tr><tr><td><strong>MT-32 émulé</strong></td><td>Roland MT-32, la meilleure musique de beaucoup de jeux de 1988 à 1992. Demande les deux fichiers ROM (voir BIOS).</td></tr><tr><td><strong>AdLib</strong></td><td>La carte son la plus courante de l'époque, avec trois émulations au choix.</td></tr></tbody></table>

Le soundfont **Roland SC-55** est fourni. Pour utiliser **Roland SC-88**, placez un fichier `Roland_SC-88.sf2` dans `bios\scummvm\extra`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (536).png" alt=""><figcaption></figcaption></figure></div>

### Sauvegarder

Il n'y a pas de sauvegardes instantanées : utilisez les sauvegardes du jeu. Appuyez sur **START** pour ouvrir le menu de ScummVM, puis **Sauvegarder** ou **Charger**. Les sauvegardes sont lues par les deux émulateurs.

## Problèmes connus

| Problème                                                               | Solution                                                                                                                                   |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Message « Game not found » ou retour à la liste des jeux               | Vérifiez l'identifiant écrit dans le fichier `.scummvm`, et que ce fichier est bien dans le dossier du jeu, avec tous les fichiers du jeu. |
| Le jeu se lance avec scummvm mais pas avec libretro: scummvm           | Le fichier `.scummvm` est vide ou absent de l'archive : écrivez l'identifiant du jeu sur sa première ligne.                                |
| Un ID créé dans ScummVM n'est pas reconnu                              | Il a été créé dans l'autre émulateur : ajoutez le jeu dans les deux, ou utilisez l'identifiant `moteur:jeu`.                               |
| Message indiquant que le jeu n'est pas complètement supporté (scummvm) | Activez **ÉMULATION > AUTORISER LES JEUX NON SUPPORTÉS**.                                                                                  |
| Le curseur est trop lent à la manette                                  | libretro: scummvm : augmentez **VITESSE DU CURSEUR À LA MANETTE**.                                                                         |
| Pas de musique MT-32                                                   | Ajoutez `MT32_CONTROL.ROM` et `MT32_PCM.ROM` dans `bios\scummvm\extra`, puis choisissez **MT-32 émulé** dans **MODE SON**.                 |
| Le choix **Roland SC-88** ne change rien                               | Le fichier `Roland_SC-88.sf2` n'est pas fourni : ajoutez-le dans `bios\scummvm\extra`.                                                     |
| Voix sans sous-titres, ou l'inverse                                    | Réglez **PAROLES ET SOUS-TITRES** (libretro: scummvm) ou **TEXTES ET VOIX** (scummvm).                                                     |
