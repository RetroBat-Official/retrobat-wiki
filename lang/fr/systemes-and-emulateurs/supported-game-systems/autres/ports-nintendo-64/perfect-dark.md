# Perfect Dark

<div align="left"><figure><img src="https://github.com/fabricecaruso/es-theme-carbon/blob/master/art/logos/pdark.png?raw=true" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

**Perfect Dark** est un jeu de tir à la première personne de Rare, sorti en 2000 sur Nintendo 64. Successeur spirituel de GoldenEye 007, il suit l'agente Joanna Dark dans une campagne d'espionnage et de science-fiction. Il propose aussi un mode multijoueur à quatre en écran partagé, le **Combat Simulator**, avec des adversaires contrôlés par l'ordinateur (les « simulants »).

Le port PC **perfect\_dark**, réalisé par fgsfds à partir de la décompilation du jeu, ajoute :

* la visée à la souris et les manettes à deux sticks ;
* l'écran large et le réglage du champ de vision ;
* le jeu à 60 images par seconde, et plus à titre expérimental ;
* la correction de quelques bugs d'origine.

Le jeu n'est pas fourni : le port lit les données de votre propre ROM du jeu.

{% embed url="https://github.com/fgsfdsfgs/perfect_dark" %}

## En bref

<table><thead><tr><th width="260.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\pdark</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64 .n64 .v64</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>pdark</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (ROM du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (4 joueurs)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Placez la ROM Nintendo 64 du jeu dans `roms\pdark`, décompressée (pas de `.zip` ni de `.7z`). La ROM doit faire 32 Mo.

Les formats `.z64`, `.n64` et `.v64` sont acceptés. Une ROM `.n64` ou `.v64` est convertie automatiquement en `.z64` au premier lancement, dans `emulators\pdark\data`.

Versions compatibles :

<table><thead><tr><th width="100.25">Version</th><th width="141.5">Écran de démarrage</th><th width="301.75">MD5 (.z64)</th><th>Remarque</th></tr></thead><tbody><tr><td>USA 1.1</td><td>NTSC version 8.7 final</td><td><code>e03b088b6ac9e0080440efed07c1e40f</code></td><td>Version conseillée</td></tr><tr><td>USA 1.0</td><td>NTSC version 8.7 final</td><td><code>7f4171b0c8d17815be37913f535e4e93</code></td><td>Fonctionne, mais déconseillée</td></tr><tr><td>Europe</td><td>PAL 8.7 final</td><td><code>d9b5cd305d228424891ce38e71bc9213</code></td><td></td></tr><tr><td>Japon</td><td>JPN version 8.9 final</td><td><code>538d2b75945eae069b29c46193e74790</code></td><td></td></tr></tbody></table>

RetroBat reconnaît la version d'après la ROM et lance l'exécutable qui lui correspond (américain, européen ou japonais) : il n'y a rien à régler. Les versions bêta et les ROM modifiées ne sont pas prises en charge.

## Contrôles

### Configuration de la manette

RetroBat configure automatiquement jusqu'à 4 manettes, une par joueur. La disposition suit celle d'une manette Xbox, avec un stick pour se déplacer et l'autre pour viser.

<table><thead><tr><th width="192">Manette RetroBat</th><th>Action</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Se déplacer</td><td>Boutons C (en analogique)</td></tr><tr><td>Stick droit</td><td>Regarder / viser</td><td>Stick</td></tr><tr><td>Croix</td><td>Avancer, reculer, se décaler</td><td>Boutons C</td></tr><tr><td>R2</td><td>Tirer / valider</td><td>Z</td></tr><tr><td>L2</td><td>Mode visée</td><td>R</td></tr><tr><td>SUD</td><td>Utiliser / valider</td><td>A</td></tr><tr><td>EST</td><td>Arme précédente / retour dans les menus</td><td>Croix gauche</td></tr><tr><td>OUEST</td><td>Recharger</td><td></td></tr><tr><td>NORD</td><td>Arme suivante</td><td></td></tr><tr><td>L1</td><td>Menu des armes (menu radial)</td><td>Croix bas</td></tr><tr><td>R1</td><td>Mode de tir secondaire</td><td>L</td></tr><tr><td>L3</td><td>S'accroupir (appuis successifs)</td><td></td></tr><tr><td>START</td><td>Pause</td><td>START</td></tr></tbody></table>

Combinaisons :

<table><thead><tr><th width="289">Combinaison</th><th>Action</th></tr></thead><tbody><tr><td><strong>SUD + R2</strong> ou <strong>R1 + R2</strong></td><td>Tir secondaire, une seule fois</td></tr><tr><td><strong>SUD + EST</strong> ou <strong>SUD + OUEST</strong></td><td>Faire exploser les explosifs posés</td></tr></tbody></table>

**CONTRÔLES > PUISSANCE DES VIBRATIONS** règle la force des vibrations (50 % par défaut).

### Clavier et souris

Le joueur 1 peut aussi jouer au clavier et à la souris, en même temps que sa manette. La souris ne commande que le joueur 1.

<table><thead><tr><th width="286.5">Touche</th><th>Action</th></tr></thead><tbody><tr><td><strong>Z Q S D</strong></td><td>Se déplacer (W A S D sur un clavier QWERTY)</td></tr><tr><td><strong>Souris</strong></td><td>Regarder / viser</td></tr><tr><td><strong>Clic gauche</strong> ou <strong>Espace</strong></td><td>Tirer</td></tr><tr><td><strong>Clic droit</strong> ou <strong>W</strong></td><td>Mode visée (Z sur un clavier QWERTY) ; retour dans les menus</td></tr><tr><td><strong>E</strong></td><td>Utiliser</td></tr><tr><td><strong>R</strong></td><td>Recharger</td></tr><tr><td><strong>Molette</strong></td><td>Arme précédente / suivante</td></tr><tr><td><strong>A</strong> ou <strong>clic molette</strong></td><td>Menu des armes (Q sur un clavier QWERTY)</td></tr><tr><td><strong>F</strong> ou <strong>X</strong></td><td>Mode de tir secondaire</td></tr><tr><td><strong>Maj gauche</strong></td><td>S'accroupir à moitié</td></tr><tr><td><strong>Ctrl gauche</strong></td><td>S'accroupir complètement</td></tr><tr><td><strong>Tab</strong></td><td>Pause</td></tr><tr><td><strong>Entrée</strong></td><td>Valider dans les menus</td></tr><tr><td><strong>Flèches</strong></td><td>Stick de la Nintendo 64</td></tr></tbody></table>

### Raccourcis

<table><thead><tr><th width="234">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td><strong>Alt + Entrée</strong></td><td>Plein écran / fenêtre</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="325.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegarde</td><td><code>saves\pdark\eeprom.bin</code></td></tr><tr><td>Réglages multijoueur enregistrés</td><td><code>emulators\pdark\mpsetups.bin</code></td></tr><tr><td>Configuration</td><td><code>emulators\pdark\pd.ini</code></td></tr><tr><td>ROM convertie (ROM <code>.n64</code> / <code>.v64</code>)</td><td><code>emulators\pdark\data</code></td></tr><tr><td>ROM Game Boy Color (facultative)</td><td><code>emulators\pdark\data\pd.gbc</code></td></tr></tbody></table>

Une sauvegarde d'une ancienne version de RetroBat (`emulators\pdark\eeprom.bin`) est copiée automatiquement dans `saves\pdark` au premier lancement.

## Guides

### Jouer à plusieurs

Le **Combat Simulator** (multijoueur et simulants) se joue jusqu'à 4 en écran partagé. Les missions peuvent aussi se jouer à 2 : en **coopération**, ou en **contre-opération**, où le second joueur incarne les ennemis. Branchez une manette par joueur avant de lancer le jeu : RetroBat attribue la manette du joueur 1 au joueur 1, et ainsi de suite.

### Options étendues du jeu

Le port ajoute un menu **Extended Options** dans les options du jeu (pages **Video**, **Audio**, **Mouse**, **Controller**, **Game**, **Key Bindings**). On y trouve notamment :

* **Vert FOV** : le champ de vision ;
* **HUD Centering** : garde l'affichage tête haute dans une zone 4:3 au centre de l'écran ;
* **Crouch Mode** : le mode d'accroupissement ;
* la couleur et la taille du réticule ;
* **Uncap Tickrate** : fréquence d'images au-delà de 60 images par seconde (expérimental, voir [**Problèmes connus**](perfect-dark.md#problemes-connus)).

Ces réglages sont conservés d'une partie à l'autre, sauf ceux gérés par RetroBat (plein écran, résolution, synchronisation verticale, filtrage, anticrénelage, touches et vibrations).

### Débloquer des cheats avec la version Game Boy Color

Sur Nintendo 64, le Transfer Pak débloquait quelques cheats grâce à la cartouche Game Boy Color de Perfect Dark. Le port reproduit cette fonction : placez la ROM Game Boy Color (version USA / Europe) dans `emulators\pdark\data`, sous le nom `pd.gbc`.

### Autres options utiles

| Option                                   | Effet                                                                                                                     |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **SYNCHRONISATION VERTICALE**            | Activée par défaut.                                                                                                       |
| **PASSER L'INTRO**                       | Démarre directement sur le menu du jeu.                                                                                   |
| **VIDÉO > RÉSOLUTION DE L'ÉCRAN**        | Par défaut, le jeu utilise la résolution du bureau.                                                                       |
| **VIDÉO > INDEX DE L'ÉCRAN**             | Écran sur lequel le jeu s'affiche.                                                                                        |
| **RENDU VISUEL > FILTRAGE DES TEXTURES** | **BILINÉAIRE** (par défaut), **PLUS PROCHE** (pixels nets) ou **TROIS POINTS** (comme la Nintendo 64).                    |
| **RENDU VISUEL > TEXTURES DÉTAILLÉES**   | Activées par défaut.                                                                                                      |
| **RENDU VISUEL > ANTICRÉNELAGE (MSAA)**  | Lisse les contours des polygones : **NON** (par défaut), **2X**, **4X**, **8X** ou **16X**.                               |
| **AUTOCONFIGURER LES MANETTES**          | Désactivé, RetroBat ne touche plus aux touches : celles réglées dans **Extended Options > Key Bindings** sont conservées. |

L'image remplit toujours l'écran (écran large) : les décorations ne sont pas disponibles pour ce jeu.

## Problèmes connus

| Problème                                                                 | Solution                                                                                                                                                                                                                     |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Message « Unsupported rom » au lancement                                 | La ROM n'est pas une version compatible, est compressée, ou ne fait pas 32 Mo (voir [**Quel format de jeu ?**](perfect-dark.md#quel-format-de-jeu)).                                                                         |
| « ROM header does not match » ou « Data segment is not 1173-compressed » | ROM modifiée, bêta ou mauvais dump : utilisez une ROM dont le MD5 est dans la liste des versions compatibles.                                                                                                                |
| Écran noir ou plantage au lancement                                      | Le port demande une carte graphique compatible OpenGL 3.0 ; mettez à jour le pilote graphique.                                                                                                                               |
| Les touches changées dans le jeu reviennent à chaque lancement           | Désactivez **AUTOCONFIGURER LES MANETTES** pour ce jeu.                                                                                                                                                                      |
| Ralentissements ou bugs au-delà de 60 images par seconde                 | **Uncap Tickrate** est expérimental : le jeu se comporte mal au-delà d'environ 165 images par seconde. Gardez la synchronisation verticale, ou limitez la fréquence avec **Framerate Limit** (**Extended Options > Video**). |
| La souris ne commande pas les autres joueurs                             | Normal : le clavier et la souris ne servent qu'au joueur 1.                                                                                                                                                                  |
