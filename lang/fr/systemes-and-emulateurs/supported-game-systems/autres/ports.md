# Ports

<div align="left"><figure><img src="../../../.gitbook/assets/image (796).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

Certains cores libretro ne sont pas des émulateurs mais des **jeux complets**, qui tournent dans RetroArch. Le système **Ports** les regroupe. RetroBat fournit six de ces jeux, prêts à jouer :

<table><thead><tr><th width="114.5">Jeu</th><th width="181">Fichier</th><th>Genre</th></tr></thead><tbody><tr><td><strong>2048</strong></td><td><code>2048.libretro</code></td><td>Réflexion : faire glisser les tuiles pour atteindre 2048.</td></tr><tr><td><strong>Anarch</strong></td><td><code>anarch.libretro</code></td><td>Jeu de tir à la première personne, dans le style des années 90.</td></tr><tr><td><strong>Craft</strong></td><td><code>craft.libretro</code></td><td>Construction de blocs, inspiré de Minecraft.</td></tr><tr><td><strong>Gong</strong></td><td><code>gong.libretro</code></td><td>Pong, contre l'ordinateur ou à deux.</td></tr><tr><td><strong>Mr. Boom</strong></td><td><code>mrboom.libretro</code></td><td>Bomberman, jusqu'à 8 joueurs.</td></tr><tr><td><strong>XRick</strong></td><td><code>xrick.libretro</code></td><td>Version libre de Rick Dangerous.</td></tr></tbody></table>

Les autres portages de jeux de RetroBat (Doom, Quake, Cave Story, Sonic…) ont leur propre système et leur propre page.

## En bref

<table><thead><tr><th width="297.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\ports</code></td></tr><tr><td><strong>Extensions</strong></td><td>.libretro</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro (le core porte le nom du fichier)</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>2048, Gong, Mr. Boom</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

Il n'y a rien à choisir : chaque fichier `<core>.libretro` lance le core libretro du même nom. `mrboom.libretro` lance le core mrboom, `craft.libretro` le core craft…

## BIOS

Aucun BIOS n'est nécessaire.

XRick a besoin de ses données, `data.zip`, que RetroBat installe dans `roms\ports\xrick`.

## Quel format de jeu ?

Les fichiers `.libretro` sont des fichiers vides : seul leur nom compte. Ils sont fournis par RetroBat, avec leurs images et leurs descriptions.

Si vous supprimez un de ces jeux par erreur, recréez simplement un fichier vide portant le nom du core, par exemple `gong.libretro`, dans `roms\ports`.

## Contrôles

RetroBat configure automatiquement les manettes.

**2048**

<table><thead><tr><th width="222.75">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Faire glisser les tuiles</td></tr><tr><td>START</td><td>Démarrer</td></tr><tr><td>SELECT</td><td>Pause</td></tr></tbody></table>

**Anarch**

<table><thead><tr><th width="255.25">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Se déplacer</td></tr><tr><td>SUD</td><td>Bouton B du jeu</td></tr><tr><td>EST</td><td>Bouton A du jeu</td></tr><tr><td>OUEST</td><td>Sauter</td></tr><tr><td>NORD</td><td>Bouton C du jeu</td></tr><tr><td>L1 / R1</td><td>Arme précédente / suivante</td></tr><tr><td>START</td><td>Carte</td></tr><tr><td>SELECT</td><td>Menu</td></tr></tbody></table>

**Craft**

<table><thead><tr><th width="235.25">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Se déplacer</td></tr><tr><td>Stick droit</td><td>Viser</td></tr><tr><td>Croix directionnelle</td><td>Avancer, reculer, viser à gauche ou à droite</td></tr><tr><td>L1 / R1</td><td>Aller à gauche / à droite</td></tr><tr><td>L2 / R2</td><td>Viser vers le haut / le bas</td></tr><tr><td>SUD</td><td>Sauter</td></tr><tr><td>OUEST</td><td>Détruire le bloc</td></tr><tr><td>NORD</td><td>Poser le bloc</td></tr><tr><td>EST</td><td>Bloc suivant</td></tr><tr><td>SELECT</td><td>Vue plus large</td></tr></tbody></table>

**Gong**

| Manette RetroBat                 | Action                |
| -------------------------------- | --------------------- |
| Croix directionnelle (haut, bas) | Déplacer la raquette  |
| SUD, EST, OUEST, NORD            | Accélérer la raquette |

Le joueur 2 est joué par l'ordinateur par défaut. Pour jouer à deux, ouvrez le menu de RetroArch (**HOTKEY + SUD**), puis **Options du cœur > Player 2** et choisissez un joueur humain.

**Mr. Boom**

<table><thead><tr><th width="241.5">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Se déplacer, pousser une bombe</td></tr><tr><td>SUD</td><td>Poser une bombe, rejoindre la partie</td></tr><tr><td>EST</td><td>Faire exploser la bombe (avec la télécommande), rejoindre la partie</td></tr><tr><td>NORD</td><td>Sauter (sur un kangourou), rejoindre la partie</td></tr><tr><td>SELECT</td><td>Ajouter un joueur ordinateur (écran de choix des joueurs)</td></tr><tr><td>START</td><td>Démarrer la partie</td></tr></tbody></table>

Chaque manette branchée peut rejoindre la partie, jusqu'à 8 joueurs.

**XRick**

<table><thead><tr><th width="234">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Se déplacer, sauter (haut), se baisser (bas)</td></tr><tr><td>EST</td><td>Attaquer</td></tr><tr><td>EST + gauche / droite</td><td>Coup de baïonnette</td></tr><tr><td>EST + haut</td><td>Tirer</td></tr><tr><td>EST + bas</td><td>Poser une bombe</td></tr></tbody></table>

### Raccourcis

Les jeux utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../navigation/hotkeys.md)).

## Dossiers

<table><thead><tr><th width="337.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux (fichiers <code>.libretro</code>)</td><td><code>roms\ports</code></td></tr><tr><td>Images de la liste des jeux</td><td><code>roms\ports\images</code></td></tr><tr><td>Données de XRick</td><td><code>roms\ports\xrick\data.zip</code></td></tr><tr><td>Sauvegardes (2048 : parties et records ; Anarch)</td><td><code>saves\ports</code></td></tr><tr><td>Monde de Craft (<code>craft.db</code>)</td><td><code>bios</code></td></tr><tr><td>Sauvegardes instantanées</td><td><code>saves\ports\libretro.&#x3C;core></code></td></tr></tbody></table>

## Guides

### Options des jeux

Chaque jeu a ses propres options dans le menu de RetroArch (**HOTKEY + SUD**, puis **Options du cœur**) :

* **Mr. Boom** : équipes (par couleur, par sexe…), monstres, tir automatique des bombes ;
* **Craft** : résolution, champ de vision, distance d'affichage, inversion de la visée ;
* **Gong** : joueur 2 humain ou ordinateur.

## Problèmes connus

<table><thead><tr><th width="342.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>XRick ne démarre pas</td><td>Le fichier <code>roms\ports\xrick\data.zip</code> manque.</td></tr><tr><td>Un jeu a disparu de la liste</td><td>Recréez le fichier vide <code>&#x3C;core>.libretro</code> dans <code>roms\ports</code>.</td></tr><tr><td>Craft ne garde pas la partie en sauvegarde instantanée</td><td>Craft ne gère pas les sauvegardes instantanées : le monde est enregistré automatiquement dans <code>bios\craft.db</code>.</td></tr></tbody></table>

