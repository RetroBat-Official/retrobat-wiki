---
description: Commodore
---

# Commodore 128

<div align="left"><figure><img src="../../../../.gitbook/assets/image (588).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

Le **Commodore 128** sort en 1985. Il succède au Commodore 64 et reste compatible avec lui. Il réunit en fait trois ordinateurs : un mode **C128** avec 128 Ko de mémoire et le BASIC 7.0, un mode **C64** qui fait tourner presque toute la ludothèque du Commodore 64, et un mode **CP/M** grâce à un second processeur, le Z80. Il peut afficher 40 colonnes sur une télévision ou 80 colonnes sur un moniteur.

La plupart des joueurs l'utilisaient en mode C64 : peu de jeux ont été écrits pour le mode C128. Le C128D, avec un lecteur de disquette intégré, sort en 1986.

RetroBat émule le C128 avec **VICE**, l'émulateur de référence des ordinateurs Commodore.

{% embed url="https://fr.wikipedia.org/wiki/Commodore_128" %}

## En bref

<table><thead><tr><th width="257.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\c128</code></td></tr><tr><td><strong>Extensions</strong></td><td>.d64 .d71 .d81 .g64 .prg .t64 .tap .crt .m3u .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: vice_x128</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>cores libretro (vice_x128)</td></tr></tbody></table>

## Quel émulateur choisir ?

Le C128 n'a qu'un émulateur dans RetroBat.

<table><thead><tr><th width="172">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: vice_x128</strong> (défaut)</td><td>Émule les modes C128 et C64, l'affichage 40 et 80 colonnes, les lecteurs 1571 et 1581, le clavier virtuel et les sauvegardes instantanées.</td><td>Pour les jeux Commodore 64, le système Commodore 64 est plus simple à utiliser.</td></tr></tbody></table>

Les jeux Commodore 64 se placent de préférence dans le système **Commodore 64** (voir la page **Commodore 64**). Le système C128 sert aux programmes écrits pour le C128.

## BIOS

Aucun BIOS n'est nécessaire : les ROM du C128 et des lecteurs de disquette sont intégrées à VICE.

## Quel format de jeu ?

<table><thead><tr><th width="161.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.d64</strong></td><td>Image de disquette 1541.</td></tr><tr><td><strong>.d71</strong></td><td>Image de disquette double face du lecteur 1571, le lecteur du C128.</td></tr><tr><td>.d81</td><td>Image de disquette 3,5 pouces du lecteur 1581.</td></tr><tr><td>.g64</td><td>Image exacte d'une disquette protégée contre la copie.</td></tr><tr><td><strong>.prg</strong></td><td>Programme seul, chargé directement en mémoire.</td></tr><tr><td>.t64, .tap</td><td>Cassette. Le chargement d'une <code>.tap</code> est long (voir <a href="commodore-128.md#accelerer-le-chargement">Guides</a>).</td></tr><tr><td>.crt</td><td>Cartouche.</td></tr><tr><td>.m3u</td><td>Liste des disquettes d'un même jeu (voir <a href="commodore-128.md#jeux-sur-plusieurs-disquettes">Guides</a>).</td></tr><tr><td>.zip, .7z</td><td>Archive contenant un des formats ci-dessus.</td></tr></tbody></table>

VICE démarre le programme tout seul : pas besoin de taper la commande de chargement.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes. Le joystick est branché sur le **port 2**, utilisé par la plupart des jeux.

<table><thead><tr><th width="204">Manette RetroBat</th><th>Commodore 128</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Joystick</td></tr><tr><td>SUD</td><td>Tir</td></tr><tr><td>EST</td><td>Second tir (rarement utilisé)</td></tr><tr><td>NORD</td><td>Barre d'espace</td></tr><tr><td>L2</td><td>RUN/STOP (touche Échap)</td></tr><tr><td>R2</td><td>RETURN (Entrée)</td></tr><tr><td>SELECT</td><td>Clavier virtuel</td></tr></tbody></table>

### Clavier virtuel

**SELECT** affiche ou masque le clavier virtuel. Déplacez-vous avec la croix directionnelle et appuyez sur une touche avec **SUD**. Dans le clavier virtuel, **START** tape RETURN, **NORD** la barre d'espace, **OUEST** verrouille les majuscules (SHIFT LOCK) et **EST** rend le clavier transparent.

### Clavier

Un clavier branché sur le PC sert de clavier C128. Activez **CONTRÔLES > FOCUS CLAVIER** pour que les touches ne déclenchent pas les raccourcis de RetroArch. La touche **Arrêt défil** active ou désactive ce mode en jeu.

La touche **CTRL droite** échange les ports joystick 1 et 2 en jeu. La touche **F7** bascule l'affichage entre 40 et 80 colonnes.

### Options de contrôle

| Option                                                     | Effet                                                                                 |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| **CONTRÔLES > PORT JOYSTICK**                              | Port 2 (par défaut) ou port 1, pour les jeux qui attendent le joystick sur le port 1. |
| **CONTRÔLES > TYPE DE PORT JOYSTICK**                      | Joystick (par défaut), paddles, souris, KoalaPad, crayon optique ou pistolet.         |
| **CONTRÔLES > OPTIONS DES BOUTONS DE FAÇADE RETROPAD**     | Change le bouton de tir, ou place « haut » (sauter) sur un bouton.                    |
| **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** / **JOUEUR 2** | RETROPAD (par défaut), JOYSTICK ou CLAVIER.                                           |

### Pistolets

L'option **PISTOLETS > ACTIVER LES PISTOLETS** branche un crayon optique sur le port 1, le seul port du C128 qui les accepte. L'option **TYPE DE PORT JOYSTICK** permet de choisir un autre modèle de crayon optique ou de pistolet.

Pour plus de détails, voir la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/).

### Raccourcis

vice\_x128 utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

<table><thead><tr><th width="355.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes instantanées</td><td><code>saves\c128\libretro.vice_x128</code></td></tr><tr><td>Disquettes de sauvegarde créées par VICE</td><td><code>saves\c128</code></td></tr><tr><td>Fichiers facultatifs de VICE (JiffyDOS, configuration <code>vicerc</code>)</td><td><code>bios\vice</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### Mode C64 et affichage 80 colonnes

* L'option **ÉMULATION > MODE C64** démarre la machine directement en mode Commodore 64, pour un jeu C64 placé dans ce système.
* L'option **ÉMULATION > SORTIE VIDÉO** choisit l'affichage au démarrage : 40 colonnes (VIC-II, par défaut) ou 80 colonnes (VDC). Certains programmes C128 et le mode CP/M utilisent l'affichage 80 colonnes. En jeu, **F7** bascule de l'un à l'autre.

### Jeux sur plusieurs disquettes

Créez un fichier `.m3u` qui liste les disquettes dans l'ordre, une par ligne :

```
Mon jeu (Disk 1).d71
Mon jeu (Disk 2).d71
```

Placez le `.m3u` et les disquettes dans `roms\c128`. Changez de disquette en jeu avec les [raccourcis de RetroArch](../../../../navigation/hotkeys.md) prévus pour les jeux sur plusieurs disques.

### Accélérer le chargement

L'option **ÉMULATION > CHARGEMENT RAPIDE** fait tourner l'émulation à vitesse maximale pendant le chargement d'une disquette ou d'une cassette, tant qu'aucun son n'est joué. **ÉMULATION FIDÈLE DU LECTEUR** doit être activée pour les disquettes. L'option **ÉMULATION > WARP BOOST** rend ce mode encore plus rapide.

### Choisir le modèle et la région

L'option **ÉMULATION > MODÈLE DE MACHINE ÉMULÉE** choisit la machine émulée : C128, C128D ou C128DCR, PAL ou NTSC.

Les modèles **Auto** choisissent la région d'après le nom du fichier : `NTSC`, `(USA)` ou `(Japan)` lancent le jeu en NTSC, `PAL` ou `(Europe)` en PAL. Sans indication, c'est la région du modèle choisi. Le réglage par défaut est **C128 PAL Auto**.

### Autres options utiles

<table><thead><tr><th width="332.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>ÉMULATION > EXTENSION MÉMOIRE</strong></td><td>Ajoute une extension mémoire (REU) de 128 Ko à 16 Mo.</td></tr><tr><td><strong>RENDU VISUEL > PALETTE DE COULEURS</strong></td><td>Colodore (par défaut), Pepto, palette interne de VICE…</td></tr><tr><td><strong>RENDU VISUEL > RECADRER (CROP)</strong></td><td>Masque la bordure autour de l'image.</td></tr><tr><td><strong>RENDU VISUEL > RATIO D'ASPECT DES PIXELS</strong></td><td>Forme des pixels : automatique, PAL, NTSC ou carrés.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="340.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Un jeu Commodore 64 ne démarre pas</td><td>Placez-le dans le système Commodore 64, ou activez <strong>MODE C64</strong>.</td></tr><tr><td>L'écran reste vide ou affiche seulement un curseur</td><td>Le programme utilise l'affichage 80 colonnes : appuyez sur <strong>F7</strong> ou réglez <strong>SORTIE VIDÉO</strong> sur 80 colonnes.</td></tr><tr><td>Le joystick ne répond pas</td><td>Le jeu attend le joystick sur l'autre port : changez <strong>PORT JOYSTICK</strong>, ou appuyez sur <strong>CTRL droite</strong> au clavier.</td></tr><tr><td>Le jeu tourne trop vite ou la musique est fausse</td><td>C'est un jeu européen lancé en NTSC : choisissez un modèle <strong>PAL</strong>.</td></tr></tbody></table>
