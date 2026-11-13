---
description: Commodore
---

# Commodore 16

<div align="left"><figure><img src="../../../../.gitbook/assets/c16.png" alt=""><figcaption></figcaption></figure></div>

## Présentation

Le **Commodore 16** sort en 1984. Commodore le conçoit comme un ordinateur familial bon marché, pour remplacer le VIC-20. Il dispose de 16 Ko de mémoire, du BASIC 3.5 (plus complet que celui du Commodore 64) et d'une puce graphique et sonore nouvelle, le **TED**, qui affiche 121 couleurs.

Il n'est pas compatible avec le Commodore 64, ce qui freine son succès aux États-Unis. En Europe, il se vend mieux grâce à son prix : au Royaume-Uni, en Allemagne ou en Hongrie, il accueille beaucoup de jeux à petit prix vendus sur cassette. La même famille compte le **C116**, à clavier en caoutchouc, et le **Plus/4**, avec 64 Ko et des logiciels intégrés. Les jeux C16 fonctionnent sur Plus/4.

RetroBat émule le C16 avec **VICE**, l'émulateur de référence des ordinateurs Commodore.

{% embed url="https://fr.wikipedia.org/wiki/Commodore_16" %}

## En bref

<table><thead><tr><th width="286.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\c16</code></td></tr><tr><td><strong>Extensions</strong></td><td>.d64 .prg .tap .t64 .crt .bin .m3u .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: vice_xplus4</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

Le C16 n'a qu'un émulateur dans RetroBat.

| Émulateur                           | Points forts                                                                                                                                            | Limites                                                                                |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **libretro: vice\_xplus4** (défaut) | Émulation très fidèle de la famille C16 / C116 / Plus/4, lecteur de disquette et lecteur de cassette émulés, clavier virtuel, sauvegardes instantanées. | Les jeux sur cassette se chargent lentement, comme sur la vraie machine (voir Guides). |

Le même core sert au système Commodore Plus/4 (dossier `roms\cplus4`). Pour le C16, RetroBat règle automatiquement le modèle sur C16.

## BIOS

Aucun BIOS n'est nécessaire : les ROM du C16 sont intégrées à VICE.

## Quel format de jeu ?

<table><thead><tr><th width="161.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.d64</strong></td><td>Image de disquette (lecteurs 1541 / 1551). Le format le plus pratique.</td></tr><tr><td><strong>.prg</strong></td><td>Programme seul, chargé directement en mémoire. Le plus rapide à démarrer.</td></tr><tr><td><strong>.tap</strong></td><td>Image de cassette. Le chargement est long (voir <a href="commodore-16.md#accelerer-le-chargement-des-cassettes">Guides</a>).</td></tr><tr><td>.t64</td><td>Archive de cassette, rare sur C16.</td></tr><tr><td>.crt, .bin</td><td>Cartouche.</td></tr><tr><td>.m3u</td><td>Liste des disquettes ou cassettes d'un même jeu (voir <a href="commodore-16.md#jeux-sur-plusieurs-disquettes-ou-cassettes">Guides</a>).</td></tr><tr><td>.zip, .7z</td><td>Archive contenant un des formats ci-dessus.</td></tr></tbody></table>

VICE démarre le jeu tout seul : pas besoin de taper la commande de chargement.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes. Le joystick est branché sur le **port 2**, utilisé par la plupart des jeux.

<table><thead><tr><th width="255.25">Manette RetroBat</th><th>Commodore 16</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Joystick</td></tr><tr><td>SUD</td><td>Tir</td></tr><tr><td>EST</td><td>Second tir (rarement utilisé)</td></tr><tr><td>NORD</td><td>Barre d'espace</td></tr><tr><td>L2</td><td>ÉCHAP</td></tr><tr><td>R2</td><td>RETURN (Entrée)</td></tr><tr><td>SELECT</td><td>Clavier virtuel</td></tr></tbody></table>

Beaucoup de jeux demandent d'appuyer sur la barre d'espace ou sur RETURN pour commencer : utilisez NORD ou R2.

### Clavier virtuel

**SELECT** affiche ou masque le clavier virtuel. Déplacez-vous avec la croix directionnelle et appuyez sur une touche avec **SUD**. Dans le clavier virtuel, **START** tape RETURN, **NORD** la barre d'espace, **OUEST** verrouille les majuscules (SHIFT LOCK) et **EST** rend le clavier transparent.

### Clavier

Un clavier branché sur le PC sert de clavier C16. Activez **CONTRÔLES > FOCUS CLAVIER** pour que les touches ne déclenchent pas les raccourcis de RetroArch. La touche **Arrêt défil** active ou désactive ce mode en jeu.

La touche **CTRL droite** échange les ports joystick 1 et 2 en jeu.

### Options de contrôle

| Option                                                     | Effet                                                                                          |
| ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| **CONTRÔLES > PORT JOYSTICK**                              | Port 2 (par défaut) ou port 1, pour les quelques jeux qui attendent le joystick sur le port 1. |
| **CONTRÔLES > OPTIONS DES BOUTONS DE FAÇADE RETROPAD**     | Change le bouton de tir, ou place « haut » (sauter) sur un bouton.                             |
| **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** / **JOUEUR 2** | RETROPAD (par défaut), JOYSTICK ou CLAVIER.                                                    |

### Raccourcis

vice\_xplus4 utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

| Contenu                                  | Dossier                          |
| ---------------------------------------- | -------------------------------- |
| Sauvegardes instantanées                 | `saves\c16\libretro.vice_xplus4` |
| Disquettes de sauvegarde créées par VICE | `saves\c16`                      |
| Captures d'écran                         | `screenshots`                    |

## Guides

### Accélérer le chargement des cassettes

Un jeu sur cassette met plusieurs minutes à se charger, comme sur la vraie machine. L'option **ÉMULATION > CHARGEMENT RAPIDE** fait tourner l'émulation à vitesse maximale pendant le chargement, tant qu'aucun son n'est joué. Elle marche aussi avec les disquettes, si **ÉMULATION > ÉMULATION FIDÈLE DU LECTEUR** est activée.

Quand c'est possible, préférez la version `.prg` ou `.d64` d'un jeu : elle se lance beaucoup plus vite.

### Jeux sur plusieurs disquettes ou cassettes

Créez un fichier `.m3u` qui liste les fichiers dans l'ordre, un par ligne :

```
Mon jeu (Disk 1).d64
Mon jeu (Disk 2).d64
```

Placez le `.m3u` et les fichiers dans `roms\c16`. Changez de disquette en jeu avec les raccourcis de RetroArch prévus pour les jeux sur plusieurs disques.

### Choisir le modèle

L'option **ÉMULATION > MODÈLE DE MACHINE ÉMULÉE** choisit la machine émulée : C16 PAL (par défaut pour ce système), C16 NTSC, Plus/4 PAL ou NTSC, V364 et C232.

* Gardez une version **PAL** pour les jeux européens, qui sont la grande majorité. En NTSC, ils tournent trop vite ou affichent mal l'image.
* Un jeu qui demande plus de 16 Ko de mémoire ne démarre pas sur un C16 : choisissez **PLUS4 PAL**, ou placez le jeu dans le système Commodore Plus/4.

### Autres options utiles

<table><thead><tr><th width="361.5">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RENDU VISUEL > PALETTE DE COULEURS</strong></td><td>Colodore (par défaut), palette interne de VICE ou palettes Yape.</td></tr><tr><td><strong>RENDU VISUEL > RECADRER (CROP)</strong></td><td>Masque la bordure autour de l'image.</td></tr><tr><td><strong>RENDU VISUEL > RATIO D'ASPECT DES PIXELS</strong></td><td>Forme des pixels : automatique, PAL, NTSC ou carrés.</td></tr></tbody></table>

## Problèmes connus

| Problème                                               | Solution                                                                                                                                      |
| ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Le jeu reste bloqué sur un écran de chargement         | C'est normal avec une cassette : le chargement dure plusieurs minutes. Activez **CHARGEMENT RAPIDE** ou utilisez une version `.prg` / `.d64`. |
| Le joystick ne répond pas                              | Le jeu attend le joystick sur l'autre port : changez **PORT JOYSTICK**.                                                                       |
| Le jeu tourne trop vite ou l'image saute               | C'est un jeu européen lancé en NTSC : choisissez un modèle **PAL**.                                                                           |
| Le jeu ne démarre pas ou affiche une erreur de mémoire | Il est fait pour le Plus/4 : choisissez le modèle **PLUS4 PAL**.                                                                              |
| Le jeu demande d'appuyer sur une touche                | Utilisez NORD (barre d'espace), R2 (RETURN) ou le clavier virtuel (SELECT).                                                                   |
