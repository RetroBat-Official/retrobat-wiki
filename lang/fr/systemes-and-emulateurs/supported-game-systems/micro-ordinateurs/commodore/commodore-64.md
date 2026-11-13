---
description: Commodore
---

# Commodore 64

<div align="left"><figure><img src="../../../../.gitbook/assets/image (589).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

Le **Commodore 64** sort en 1982. Il dispose de 64 Ko de mémoire, d'une puce graphique (VIC-II) qui gère les sprites et le défilement, et surtout de la puce sonore **SID**, dont la musique a marqué toute une génération. Son prix baisse rapidement et il devient l'ordinateur le plus vendu de l'histoire, avec plusieurs millions d'exemplaires jusqu'à l'arrêt de sa production en 1994. Une version au boîtier redessiné, le C64C, sort en 1986.

Sa ludothèque compte des milliers de jeux, sur cassette, disquette et cartouche : Impossible Mission, The Last Ninja, Maniac Mansion, Boulder Dash, Turrican ou The Great Giana Sisters. La scène démo y est encore très active.

RetroBat émule le C64 avec **VICE**, l'émulateur de référence des ordinateurs Commodore, et avec **Frodo**, plus ancien.

{% embed url="https://fr.wikipedia.org/wiki/Commodore_64" %}

## En bref

<table><thead><tr><th width="271.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\c64</code></td></tr><tr><td><strong>Extensions</strong></td><td>.crt .d64 .d71 .d81 .g64 .nib .prg .t64 .tap .m3u .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: vice_x64</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro (sauf frodo)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>cores libretro (vice_x64, vice_x64sc)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="178.25">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: vice_x64</strong> (défaut)</td><td>Très compatible et rapide, tous les formats, clavier virtuel, sauvegardes instantanées, crayons optiques et pistolets.</td><td>—</td></tr><tr><td><strong>libretro: vice_x64sc</strong></td><td>Émulation exacte au cycle près : pour les démos et les rares jeux qui posent problème avec vice_x64.</td><td>Demande un peu plus de puissance.</td></tr><tr><td><strong>libretro: frodo</strong></td><td>Émulateur léger.</td><td>Lit seulement les disquettes <code>.d64</code> et les cassettes <code>.t64</code>. Pas de sauvegardes instantanées. Moins compatible.</td></tr></tbody></table>

Gardez **vice\_x64** sauf pour un jeu ou une démo qui ne fonctionne pas : essayez alors **vice\_x64sc**.

## BIOS

Aucun BIOS n'est nécessaire : les ROM du C64 et des lecteurs de disquette sont intégrées à VICE et à Frodo.

## Quel format de jeu ?

<table><thead><tr><th width="164">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.d64</strong></td><td>Image de disquette 1541. Le format le plus courant.</td></tr><tr><td><strong>.crt</strong></td><td>Cartouche. Démarre immédiatement.</td></tr><tr><td><strong>.prg</strong></td><td>Programme seul, chargé directement en mémoire. Le plus rapide à démarrer (VICE uniquement).</td></tr><tr><td><strong>.tap</strong></td><td>Image de cassette. Le chargement est long (voir <a href="commodore-64.md#jeux-sur-cassette">Guides</a>). VICE uniquement.</td></tr><tr><td>.t64</td><td>Archive de cassette, chargée directement.</td></tr><tr><td>.d71, .d81</td><td>Disquettes des lecteurs 1571 et 1581 (VICE uniquement).</td></tr><tr><td>.g64, .nib</td><td>Images exactes de disquettes protégées contre la copie (VICE uniquement).</td></tr><tr><td>.m3u</td><td>Liste des disquettes d'un même jeu (voir <a href="commodore-64.md#jeux-sur-plusieurs-disquettes">Guides</a>).</td></tr><tr><td>.zip, .7z</td><td>Archive contenant un des formats ci-dessus.</td></tr></tbody></table>

VICE démarre le jeu tout seul : pas besoin de taper `LOAD"*",8,1` puis `RUN`.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes. Le joystick est branché sur le **port 2**, utilisé par la plupart des jeux.

<table><thead><tr><th width="244">Manette RetroBat</th><th>Commodore 64 (VICE)</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Joystick</td></tr><tr><td>SUD</td><td>Tir</td></tr><tr><td>EST</td><td>Second tir (rarement utilisé)</td></tr><tr><td>NORD</td><td>Barre d'espace</td></tr><tr><td>L2</td><td>RUN/STOP (touche Échap)</td></tr><tr><td>R2</td><td>RETURN (Entrée)</td></tr><tr><td>SELECT</td><td>Clavier virtuel</td></tr></tbody></table>

Beaucoup de jeux demandent d'appuyer sur la barre d'espace, sur RETURN ou sur F1 pour commencer : utilisez NORD, R2 ou le clavier virtuel.

### Clavier virtuel (VICE)

**SELECT** affiche ou masque le clavier virtuel. Déplacez-vous avec la croix directionnelle et appuyez sur une touche avec **SUD**. Dans le clavier virtuel, **START** tape RETURN, **NORD** la barre d'espace, **OUEST** verrouille les majuscules (SHIFT LOCK) et **EST** rend le clavier transparent.

### Clavier

Un clavier branché sur le PC sert de clavier C64. Activez **CONTRÔLES > FOCUS CLAVIER** pour que les touches ne déclenchent pas les raccourcis de RetroArch. La touche **Arrêt défil** active ou désactive ce mode en jeu.

Avec VICE, la touche **CTRL droite** échange les ports joystick 1 et 2 en jeu.

### Options de contrôle (VICE)

| Option                                                     | Effet                                                                                 |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| **CONTRÔLES > PORT JOYSTICK**                              | Port 2 (par défaut) ou port 1, pour les jeux qui attendent le joystick sur le port 1. |
| **CONTRÔLES > TYPE DE PORT JOYSTICK**                      | Joystick (par défaut), paddles, souris, KoalaPad, crayon optique ou pistolet.         |
| **CONTRÔLES > OPTIONS DES BOUTONS DE FAÇADE RETROPAD**     | Change le bouton de tir, ou place « haut » (sauter) sur un bouton.                    |
| **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** / **JOUEUR 2** | RETROPAD (par défaut), JOYSTICK ou CLAVIER.                                           |

### Pistolets

Avec vice\_x64 et vice\_x64sc, l'option **PISTOLETS > ACTIVER LES PISTOLETS** branche un crayon optique ou un pistolet sur le port 1, le seul port du C64 qui les accepte. Par défaut, c'est un crayon optique (gâchette haut). L'option **TYPE DE PORT JOYSTICK** permet de choisir un autre modèle, par exemple le **Magnum Light Phaser** ou le **Stack Light Rifle**.

Pour plus de détails, voir la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/).

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

<table><thead><tr><th width="361.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes instantanées</td><td><code>saves\c64\libretro.vice_x64</code>, <code>saves\c64\libretro.vice_x64sc</code></td></tr><tr><td>Disquettes de sauvegarde créées par VICE</td><td><code>saves\c64</code></td></tr><tr><td>Fichiers facultatifs de VICE (JiffyDOS, configuration <code>vicerc</code>)</td><td><code>bios\vice</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### Jeux sur plusieurs disquettes

Créez un fichier `.m3u` qui liste les disquettes dans l'ordre, une par ligne :

```
Mon jeu (Disk 1).d64
Mon jeu (Disk 2).d64
```

Placez le `.m3u` et les disquettes dans `roms\c64`. Changez de disquette en jeu avec les [raccourcis de RetroArch](../../../../navigation/hotkeys.md) prévus pour les jeux sur plusieurs disques.

### Jeux sur cassette

Un jeu sur cassette (`.tap`) met plusieurs minutes à se charger, comme sur la vraie machine. L'option **ÉMULATION > CHARGEMENT RAPIDE** fait tourner l'émulation à vitesse maximale pendant le chargement, tant qu'aucun son n'est joué. Elle marche aussi avec les disquettes, si **ÉMULATION FIDÈLE DU LECTEUR** est activée. L'option **ÉMULATION > WARP BOOST** rend ce mode encore plus rapide.

Quand c'est possible, préférez la version `.d64`, `.t64` ou `.crt` du jeu.

### Choisir le modèle et la région

L'option **ÉMULATION > MODÈLE DE MACHINE ÉMULÉE** choisit la machine émulée : C64 ou C64C, PAL ou NTSC, SX-64, C64 Games System…

* Les modèles **auto** choisissent la région d'après le nom du fichier : `NTSC`, `(USA)` ou `(Japan)` lancent le jeu en NTSC, `PAL` ou `(Europe)` en PAL. Sans indication, c'est la région du modèle choisi. Le réglage par défaut est **C64 PAL auto**, adapté à la grande majorité des jeux, qui sont européens.
* Un jeu européen lancé en NTSC tourne trop vite et sa musique est faussée.

### Extension mémoire

L'option **ÉMULATION > EXTENSION MÉMOIRE** ajoute une extension mémoire (REU) de 128 Ko à 16 Mo. Seuls quelques programmes et démos récents en ont besoin.

### Autres options utiles

<table><thead><tr><th width="325.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RENDU VISUEL > PALETTE DE COULEURS</strong></td><td>Colodore (par défaut), Pepto, palette interne de VICE…</td></tr><tr><td><strong>RENDU VISUEL > RECADRER (CROP)</strong></td><td>Masque la bordure autour de l'image.</td></tr><tr><td><strong>RENDU VISUEL > RATIO D'ASPECT DES PIXELS</strong></td><td>Forme des pixels : automatique, PAL, NTSC ou carrés.</td></tr><tr><td><strong>ÉMULATION > ÉMULATION FIDÈLE DU LECTEUR</strong></td><td>Émule exactement le lecteur de disquette (activé par défaut). Nécessaire pour beaucoup de jeux protégés.</td></tr><tr><td><strong>RÉSOLUTION DE SORTIE</strong> (frodo)</td><td>Résolution de l'image produite par Frodo.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="326.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le joystick ne répond pas</td><td>Le jeu attend le joystick sur l'autre port : changez <strong>PORT JOYSTICK</strong>, ou appuyez sur <strong>CTRL droite</strong> au clavier.</td></tr><tr><td>Le jeu tourne trop vite ou la musique est fausse</td><td>C'est un jeu européen lancé en NTSC : choisissez un modèle <strong>PAL</strong>.</td></tr><tr><td>Une disquette protégée ne démarre pas</td><td>Vérifiez que <strong>ÉMULATION FIDÈLE DU LECTEUR</strong> est activée, ou utilisez une image <code>.g64</code> / <code>.nib</code>.</td></tr><tr><td>Le jeu reste bloqué sur un écran de chargement</td><td>C'est normal avec une cassette : le chargement dure plusieurs minutes. Activez <strong>CHARGEMENT RAPIDE</strong> ou utilisez une version <code>.d64</code> / <code>.t64</code>.</td></tr><tr><td>Un fichier <code>.prg</code> ou <code>.tap</code> ne se lance pas avec frodo</td><td>Frodo ne lit que <code>.d64</code> et <code>.t64</code> : utilisez vice_x64.</td></tr><tr><td>Le jeu demande d'appuyer sur une touche</td><td>Utilisez NORD (barre d'espace), R2 (RETURN) ou le clavier virtuel (SELECT).</td></tr></tbody></table>
