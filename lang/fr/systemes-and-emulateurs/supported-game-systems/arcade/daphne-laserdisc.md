# LaserDisc

<div align="left"><figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure></div>

## Présentation

Au début des années 1980, certaines bornes d'arcade n'affichent pas des graphismes calculés par la machine : elles lisent un film enregistré sur un **LaserDisc**. Le joueur doit réagir au bon moment, et la borne saute à la séquence suivante ou à la scène de défaite.

Le genre est lancé en 1983 par **Dragon's Lair**, un dessin animé interactif réalisé par l'ancien animateur de Disney Don Bluth, dont la qualité d'image n'avait rien de comparable à l'époque. Suivent Space Ace, Cliff Hanger, Astron Belt, M.A.C.H. 3, Cobra Command, Thayer's Quest ou Super Don Quix-ote, puis Dragon's Lair II: Time Warp en 1991.

Le nom du système vient de **Daphne**, le premier émulateur de bornes LaserDisc, créé par Matt Ownby. RetroBat utilise par défaut **Hypseus Singe**, sa version moderne, qui lit aussi les jeux **Singe** (voir la page [**Singe**](../moteurs-de-jeu/singe.md)).

Un jeu LaserDisc est fait de deux parties : la ROM de la borne et les fichiers vidéo et audio tirés du disque.

{% embed url="https://fr.wikipedia.org/wiki/DAPHNE" %}

## En bref

<table><thead><tr><th width="264"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\daphne</code></td></tr><tr><td><strong>Extensions</strong></td><td>.daphne .hypseus .7z .rar .squashfs</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>hypseus</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, sauf daphne</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>Hypseus (jeux Singe)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="134">Émulateur</th><th width="174.25">Pour qui ?</th><th width="224">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>hypseus</strong> (défaut)</td><td>Tout le monde</td><td>Version moderne de Daphne, toujours mise à jour. Manette configurée automatiquement, décorations, jeux Daphne et jeux Singe, pistolets.</td><td>—</td></tr><tr><td><strong>daphne</strong></td><td>Cas particuliers</td><td>L'émulateur d'origine.</td><td>Plus mis à jour. RetroBat ne configure pas la manette : il se joue au clavier. Pas de jeux Singe.</td></tr><tr><td><strong>singe2</strong></td><td>Jeux au format Singe 2</td><td>Voir la page <a href="../moteurs-de-jeu/singe.md"><strong>Singe</strong></a>.</td><td>Ne lit pas les jeux Daphne.</td></tr></tbody></table>

**En cas de doute, gardez hypseus.**

## BIOS

Aucun BIOS n'est nécessaire. Chaque jeu a en revanche besoin de sa ROM, à placer dans `roms\daphne\roms` (voir ci-dessous).

## Quel format de jeu ?

Un jeu Daphne se compose de deux éléments, qui portent le **même nom** :

<table><thead><tr><th width="163.25">Élément</th><th width="260.75">Emplacement</th><th>Contenu</th></tr></thead><tbody><tr><td>Dossier du jeu</td><td><code>roms\daphne\&#x3C;nom>.daphne</code></td><td>Les vidéos (<code>.m2v</code>), le son (<code>.ogg</code>) et le fichier <code>&#x3C;nom>.txt</code>, qui donne l'ordre des vidéos</td></tr><tr><td>ROM de la borne</td><td><code>roms\daphne\roms\&#x3C;nom>.zip</code></td><td>Le programme du jeu</td></tr></tbody></table>

Exemple pour Dragon's Lair (`lair`) :

```
roms\daphne\
├─ roms\
│  └─ lair.zip
└─ lair.daphne\
   ├─ lair.txt
   ├─ lair.m2v
   └─ lair.ogg
```

Le nom est celui attendu par l'émulateur : `lair` pour Dragon's Lair, `ace` pour Space Ace, `cliff` pour Cliff Hanger… C'est le dossier `.daphne` qui apparaît dans la liste des jeux de RetroBat.

<table><thead><tr><th width="199.25">Format</th><th width="107.75">hypseus</th><th width="83.5">daphne</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>Dossier .daphne</strong></td><td>✔</td><td>✔</td><td>Le format normal.</td></tr><tr><td>Dossier .hypseus</td><td>✔</td><td>✔</td><td>Même contenu, autre nom d'extension.</td></tr><tr><td>.7z / .rar / .squashfs</td><td>✔</td><td>✔</td><td>Dossier du jeu compressé, extrait au lancement.</td></tr></tbody></table>

Les jeux Singe (American Laser Games, Time Gal…) fonctionnent aussi ici avec Hypseus, mais ils ont leur propre système : voir la page [**Singe**](../moteurs-de-jeu/singe.md).

## Contrôles

### Configuration automatique

Avec **Hypseus**, RetroBat configure automatiquement la manette du joueur 1. Le clavier reste toujours utilisable.

<table><thead><tr><th width="195.75">Action</th><th>Manette RetroBat</th><th>Clavier</th></tr></thead><tbody><tr><td>Directions</td><td>Croix directionnelle / stick gauche</td><td>Flèches</td></tr><tr><td>Bouton 1</td><td>SUD</td><td>CTRL gauche</td></tr><tr><td>Bouton 2</td><td>EST</td><td>ALT gauche</td></tr><tr><td>Bouton 3</td><td>R1</td><td>ESPACE</td></tr><tr><td>Skill 1</td><td>OUEST</td><td>MAJ gauche</td></tr><tr><td>Skill 2</td><td>NORD</td><td>Z</td></tr><tr><td>Skill 3</td><td>L1</td><td>X</td></tr><tr><td>Crédit joueur 1</td><td>SELECT</td><td>5</td></tr><tr><td>Start joueur 1</td><td>START</td><td>1</td></tr><tr><td>Crédit joueur 2</td><td>—</td><td>6</td></tr><tr><td>Start joueur 2</td><td>—</td><td>2</td></tr><tr><td>Service</td><td>L3</td><td>9</td></tr><tr><td>Test</td><td>R3</td><td>0</td></tr><tr><td>Pause</td><td>—</td><td>P</td></tr><tr><td>Reset</td><td>—</td><td>F3</td></tr><tr><td>Capture d'écran</td><td>—</td><td>F12</td></tr></tbody></table>

Dans la plupart des jeux, seuls les directions et le bouton 1 servent (l'épée dans Dragon's Lair, le tir dans Space Ace). Les boutons Skill choisissent le niveau de difficulté dans les jeux qui le proposent.

Pour les jeux de vol, l'option **CONTRÔLES > INVERSER AXE VERTICAL** inverse le haut et le bas.

Avec **daphne**, RetroBat ne configure pas la manette : le jeu se joue au clavier.

Pour configurer vous-même les touches de Hypseus, désactivez **AUTOCONFIGURER LES MANETTES**.

### Raccourcis

<table><thead><tr><th width="234">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td>ÉCHAP</td><td>Quitter (clavier)</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="312.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>ROM des jeux</td><td><code>roms\daphne\roms</code></td></tr><tr><td>Vidéos et son d'un jeu</td><td><code>roms\daphne\&#x3C;nom>.daphne</code></td></tr><tr><td>Paramètres d'un jeu</td><td><code>roms\daphne\&#x3C;nom>.commands</code></td></tr><tr><td>Touches de Hypseus</td><td><code>emulators\hypseus\hypinput.ini</code></td></tr><tr><td>Décorations de Hypseus</td><td><code>emulators\hypseus\bezels</code></td></tr><tr><td>Captures d'écran de Hypseus (F12)</td><td><code>emulators\hypseus\screenshots</code></td></tr></tbody></table>

## Guides

### Ajouter un jeu

1. Copiez la ROM du jeu, par exemple `lair.zip`, dans `roms\daphne\roms`.
2. Copiez le dossier contenant les vidéos dans `roms\daphne`.
3. Renommez ce dossier avec le nom de la ROM suivi de `.daphne` : `lair.daphne`.
4. Vérifiez que le dossier contient un fichier `.txt` du même nom : `lair.txt`.
5. Mettez à jour la liste des jeux dans RetroBat.

<div align="left"><figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure></div>

Au premier lancement, l'émulateur analyse les vidéos et crée des fichiers `.dat` dans le dossier du jeu : le démarrage est plus long cette fois-là.

### Régler un jeu avec un fichier .commands

Les bornes se réglaient avec des interrupteurs (nombre de vies, difficulté, crédits). Pour les modifier, ou pour passer d'autres paramètres à l'émulateur, créez un fichier texte portant le nom du jeu et l'extension `.commands`, **à côté** du dossier du jeu :

```
roms\daphne\lair.daphne\
roms\daphne\lair.commands
```

Écrivez les paramètres sur une seule ligne, séparés par des espaces. Par exemple, pour régler les deux séries d'interrupteurs :

```
-bank 0 xxxxxxxx -bank 1 xxxxxxxx
```

Chaque `x` vaut 0 ou 1 et correspond à un interrupteur. Leur signification dépend du jeu et de la version de sa ROM.

RetroBat ignore dans ce fichier les paramètres qu'il gère lui-même (plein écran, chemins, type de rendu…).

### Décorations avec Hypseus

Hypseus affiche une décoration autour de l'image. RetroBat la choisit dans cet ordre :

1. le fichier choisi avec l'option **FORCER LA DÉCORATION** ;
2. un fichier `<nom>.png` dans `emulators\hypseus\bezels` ;
3. un fichier `.png` dont le nom contient `bezel`, dans le dossier du jeu ;
4. la décoration RetroBat du jeu ou du système.

Les étapes 2 et 3 ne valent que si vous n'avez pas choisi de décoration particulière dans RetroBat. Si les décorations sont désactivées, seule l'option **FORCER LA DÉCORATION** s'applique.

## Problèmes connus

<table><thead><tr><th width="325.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu apparaît dans la liste mais ne se lance pas</td><td>Vérifiez les trois noms, qui doivent être identiques : <code>roms\daphne\roms\&#x3C;nom>.zip</code>, le dossier <code>&#x3C;nom>.daphne</code> et le fichier <code>&#x3C;nom>.txt</code> qu'il contient.</td></tr><tr><td>Le premier lancement est très long</td><td>C'est normal : l'émulateur analyse les vidéos une fois pour toutes.</td></tr><tr><td>La manette ne répond pas</td><td>Seul Hypseus est configuré par RetroBat, et pour le joueur 1. Avec daphne, utilisez le clavier ou passez sur Hypseus.</td></tr><tr><td>Le haut et le bas sont inversés dans un jeu de vol</td><td>Activez <strong>INVERSER AXE VERTICAL</strong>.</td></tr><tr><td>L'image ne remplit pas l'écran</td><td>Activez <strong>ÉTIRER POUR REMPLIR L'ÉCRAN</strong>.</td></tr><tr><td>Des scènes sont coupées trop tôt</td><td>Ajoutez <code>-latency</code> suivi d'un délai en millisecondes dans le fichier <code>.commands</code> du jeu.</td></tr><tr><td>F12 ne crée pas de capture d'écran avec Hypseus</td><td>Créez le dossier <code>emulators\hypseus\screenshots</code> s'il n'existe pas. Les captures ne fonctionnent que sur l'écran principal.</td></tr></tbody></table>

