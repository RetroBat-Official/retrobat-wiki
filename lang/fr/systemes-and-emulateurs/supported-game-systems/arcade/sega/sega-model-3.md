---
description: Sega
---

# Sega Model 3

<div align="left"><figure><img src="../../../../.gitbook/assets/image (4).png" alt="" width="482"><figcaption></figcaption></figure></div>

## Présentation

Le **Sega Model 3** est la troisième carte d'arcade 3D de Sega, sortie en 1996. Construite avec Lockheed Martin autour d'un processeur PowerPC et du processeur graphique Real3D Pro-1000, elle affiche des graphismes très en avance sur les consoles de l'époque : la Dreamcast n'arrivera qu'en 1998. Plusieurs révisions se succèdent (Step 1.0, 1.5, 2.0 et 2.1), de plus en plus puissantes.

La ludothèque compte une vingtaine de jeux, dont **Virtua Fighter 3**, **Scud Race**, **Daytona USA 2**, **Sega Rally 2**, **The Lost World: Jurassic Park**, **Star Wars Trilogy Arcade**, **Fighting Vipers 2**, **Spikeout**, **Virtua Striker 2**, **Virtual On 2: Oratorio Tangram** ou **Sega Bass Fishing**.

RetroBat propose quatre émulateurs : **Supermodel** (l'émulateur de référence du Model 3), **Keisho** (anciennement sm2-emu, un émulateur dédié aux Model 1, 2 et 3), le core libretro **supermodel**, et **Model3-Vulkan** (une version de Supermodel en Vulkan).

{% embed url="https://fr.wikipedia.org/wiki/Model_3" %}

## En bref

<table><thead><tr><th width="277.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\model3</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>supermodel</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core libretro, Keisho, Model3-Vulkan ; Supermodel par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>supermodel, Keisho, core libretro, Model3-Vulkan</td></tr><tr><td><strong>Volants</strong></td><td>supermodel, Keisho, Model3-Vulkan</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="202">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>supermodel</strong> (défaut)</td><td>La référence : tous les jeux, pistolets, volants et retour de force, écran large.</td><td>Sauvegardes instantanées non gérées par RetroBat. À deux joueurs, les deux manettes doivent utiliser le même pilote.</td></tr><tr><td><strong>keisho</strong></td><td>Émulateur moderne : Vulkan / OpenGL, résolution augmentée, filtre CRT, sauvegardes instantanées, retour arrière ; aucun réglage à faire dans le menu de test des bornes.</td><td>Model 3 tout récent (63 romsets) ; les prototypes de Sega Rally 2 ne démarrent pas.</td></tr><tr><td><strong>libretro: supermodel</strong></td><td>Fonctions de RetroArch (shaders, sauvegardes instantanées).</td><td>Version bêta.</td></tr><tr><td><strong>model3-vulkan</strong></td><td>Version Vulkan de Supermodel : résolution interne, textures HD, filtre CRT, sauvegardes instantanées.</td><td>Carte graphique compatible Vulkan 1.3 obligatoire.</td></tr></tbody></table>

## BIOS

Le Model 3 n'a pas de BIOS : rien à installer.

## Quel format de jeu ?

Les jeux sont des archives `.zip` au format MAME, à garder sans les décompresser et sans les renommer.

* Les clones (`scudplus`, `vf3tb`, `dayto2pe`…) ont besoin de leur jeu parent (`scud`, `vf3`, `daytona2`) dans le même dossier, sauf avec un romset non-merged. Keisho cherche le parent à côté de l'archive.
* Keisho reconnaît les jeux par leur contenu : une archive merged qui contient plusieurs versions lance celle qui porte le nom de l'archive.

L'extension `.decomp` correspond aux portages PC, voir la page [**Recompilations**](../../autres/recomp.md).

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour tous les émulateurs. L'option **AUTOCONFIGURER LES MANETTES** permet de garder sa propre configuration.

Pour tous les jeux : **START** = Start, **SELECT** = pièce. Au clavier : 1 / 2 = Start des joueurs 1 / 2, 5 / 6 = pièce, 9 = Service, 0 = Test.

**DISPOSITION DES BOUTONS** adapte les boutons aux sticks arcade (modern8, 8alternative, 6alternative). Pour plus de détails sur les dispositions arcade, voir la page [**Le Guide Arcade**](../../../arcade-guide.md).

### Supermodel et Model3-Vulkan

Les deux émulateurs ont la même disposition, réglée par jeu dans `supermodel.yml` (`system\resources\inputmapping`, copie modifiable dans `user\inputmapping`). Model3-Vulkan lit d'abord un fichier `model3vulkan.yml` s'il existe.

<table><thead><tr><th width="349">Jeu</th><th>Commandes</th></tr></thead><tbody><tr><td>Virtua Fighter 3 (<code>vf3</code>, <code>vf3tb</code>), Fighting Vipers 2 (<code>fvipers2</code>)</td><td>Croix ou stick gauche : déplacements ; OUEST : poing ; SUD : pied ; EST : garde ; NORD : esquive</td></tr><tr><td>Spikeout (<code>spikeout</code>, <code>spikeofe</code>)</td><td>Croix ou stick gauche : déplacements ; SUD : frappe ; OUEST : charge ; EST ou R1 : shift ; NORD : saut</td></tr><tr><td>Virtua Striker 2 (<code>vs2</code>, <code>vs298</code>, <code>vs2v991</code>…)</td><td>Croix ou stick gauche : déplacements ; SUD : passe longue ; EST : tir ; OUEST : passe courte</td></tr><tr><td>Daytona USA 2 (<code>daytona2</code>), Scud Race (<code>scud</code>, <code>scudplus</code>…)</td><td>Stick gauche : direction ; R2 / L2 : accélérer / freiner ; R1 / L1 : rapport supérieur / inférieur ; NORD, SUD, OUEST, EST : rapports 1, 2, 3, 4 ; croix haut, bas, gauche, droite : VR1 à VR4</td></tr><tr><td>Sega Rally 2, Le Mans 24, Dirt Devils, Emergency Call Ambulance</td><td>Stick gauche : direction ; R2 / L2 : accélérer / freiner ; R1 / L1 : rapport supérieur / inférieur ; stick droit : rapports (haut 1, bas 2, gauche 3, droite 4) ; NORD : vue ; SUD : frein à main</td></tr><tr><td>Harley-Davidson &#x26; L.A. Riders (<code>harley</code>)</td><td>Comme les autres jeux de course ; SUD : frein arrière ; EST : choix de la musique ; NORD : vue</td></tr><tr><td>The Lost World (<code>lostwsga</code>), The Ocean Hunter (<code>oceanhun</code>), L.A. Machineguns (<code>lamachin</code>)</td><td>Pistolet ou souris : viser ; clic gauche : tir ; clic droit : recharger (The Lost World) ou 2e gâchette ; viser hors de l'écran recharge aussi</td></tr><tr><td>Star Wars Trilogy Arcade (<code>swtrilgy</code>)</td><td>Stick gauche ou souris : manche ; R2, OUEST ou clic gauche : tir ; SUD ou clic droit : bouton d'événement</td></tr><tr><td>Virtual On 2 (<code>von2</code>)</td><td>Stick gauche : avancer, reculer, pas de côté ; stick droit : tourner ; L2 / R2 : tirs gauche / droit ; OUEST ou L1 / EST ou R1 : turbo gauche / droit ; NORD : saut ; SUD : s'accroupir</td></tr><tr><td>Ski Champ (<code>skichamp</code>)</td><td>Stick gauche : tourner ; stick droit : tourner plus fort ; L2 / R2 : bâtons gauche / droit ; OUEST, SUD, EST : Select 1, 2, 3</td></tr><tr><td>Sega Bass Fishing / Get Bass (<code>bassdx</code>)</td><td>Stick gauche : canne ; stick droit : manette de la borne ; R2 : moulinet ; SUD : lancer ; EST : Select</td></tr><tr><td>Magical Truck Adventure (<code>magtruck</code>)</td><td>Stick gauche : levier ; SUD : pédale</td></tr></tbody></table>

L'option **CONTRÔLES > UTILISER R1/L1 POUR LES JEUX DE COURSE** met l'accélérateur et le frein sur R1 / L1, et les rapports sur la croix directionnelle (sauf Daytona USA 2 et Scud Race, dont la disposition est fixée par `supermodel.yml`).

### Keisho

Keisho suit la même logique, avec ses propres boutons réglés dans `keisho.yml`. Pour plus de détails, voir la page [**Configuration des touches Keisho**](../../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-keisho.md).

<table><thead><tr><th width="280.25">Jeu</th><th>Commandes</th></tr></thead><tbody><tr><td>Virtua Fighter 3, Fighting Vipers 2</td><td>Comme Supermodel : OUEST : poing ; SUD : pied ; EST : garde ; NORD : esquive</td></tr><tr><td>Spikeout</td><td>Comme Supermodel : SUD : frappe ; OUEST : charge ; EST : shift ; NORD : saut</td></tr><tr><td>Virtua Striker 2</td><td>Comme Supermodel : SUD : passe longue ; EST : tir ; OUEST : passe courte</td></tr><tr><td>Jeux de course</td><td>Stick gauche : direction ; R2 / L2 : accélérer / freiner ; R1 / L1 : rapport supérieur / inférieur ; SUD, EST, OUEST, NORD : boutons VR1 à VR4 ou vue (Harley-Davidson : SUD = choix de la musique, EST = vue)</td></tr><tr><td>Jeux au pistolet</td><td>Pistolet, souris ou stick : viser ; SUD ou R2 : tir ; EST ou L2 : recharger</td></tr><tr><td>Star Wars Trilogy Arcade</td><td>Stick gauche : manche ; R2 / L2 : gâchettes du manche ; SUD / EST : événements 1 / 2</td></tr><tr><td>Sega Bass Fishing</td><td>Stick gauche : canne ; stick droit : manette de la borne ; gâchettes : moulinet et tension du fil ; SUD : lancer ; EST : Select</td></tr><tr><td>Magical Truck Adventure</td><td>Stick gauche : levier ; SUD : pédale</td></tr><tr><td>Virtual On 2 (disposition fixe)</td><td>Stick gauche ou croix : manche gauche ; stick droit ou boutons de face : manche droit ; L1 / R1 : turbo ; L2 / R2 : tirs</td></tr><tr><td>Ski Champ (disposition fixe)</td><td>Stick gauche : tourner ; L1 / R1 : bâtons ; OUEST, NORD, EST : Select 1, 2, 3</td></tr></tbody></table>

Les dispositions de Virtual On 2 et de Ski Champ sont propres à Keisho et ne se modifient pas.

### Core libretro supermodel

Le core utilise la disposition de RetroArch, ajustée par RetroBat pour Daytona USA 2, Scud Race, Fighting Vipers 2, Spikeout et Virtua Fighter 3 (fichier `libretro_supermodel.yml`). L'option **CONTRÔLES > BOUTONS SERVICE** place Service / Test sur L3 / R3 (défaut) ou sur les gâchettes.

### Pistolets

Jeux au pistolet : The Lost World, The Ocean Hunter, L.A. Machineguns.

Activez **PISTOLETS > ACTIVER LES PISTOLETS**.

* **Supermodel** : **MULTI-PISTOLETS (RAW INPUT)** pour deux pistolets, **INDEX DU 1ER PISTOLET** / **2E PISTOLET** si les pistolets ne sont pas reconnus dans le bon ordre, **AFFICHER CIBLE**, **UTILISER MAMEHOOKER** et **SORTIR DES DONNÉES DE JEU** pour les retours (recul, lampes).
* **Model3-Vulkan** : **AFFICHER CIBLE**, **STYLE DE CIBLE**, **TAILLE DE LA BORDURE SINDEN**, **UN SEUL PISTOLET**, et les mêmes options MameHooker.
* **Keisho** : sans l'option, Keisho est en mode automatique : il affiche le viseur dans les jeux au pistolet, et l'on vise à la souris ou au stick de la manette. Avec l'option, il utilise les pistolets branchés. Options **AFFICHER CIBLE**, **MASQUER LE FLASH DES TIRS**, **TAILLE DE LA BORDURE SINDEN**, **ACTIVER LE RECUL DU PISTOLET**.
* **Core libretro** : **AFFICHER CIBLE**, **UN SEUL PISTOLET**.

Avec Supermodel, Model3-Vulkan et le core libretro, les jeux au pistolet doivent être calibrés dans leur menu de test (voir [**Calibrer les pistolets**](sega-model-3.md#calibrer-les-pistolets) plus bas). Pour plus de détails sur les pistolets, voir la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/).

### Volants

Supermodel, Keisho et Model3-Vulkan gèrent les volants, avec l'option **VOLANTS DE COURSE > ACTIVER LES VOLANTS**.

* Supermodel et Model3-Vulkan : **ACTIVER LE RETOUR DE FORCE**, levier de vitesses séparé ; boutons réglés par type de volant dans `model3_wheels.yml` (Model3-Vulkan lit d'abord `model3vulkan_wheels.yml` s'il existe). **FORCER L'INDEX DU VOLANT** choisit le volant s'il n'est pas reconnu.
* Keisho : **ACTIVER LE RETOUR DE FORCE** et **FORCE DU RETOUR DE FORCE** ; boutons réglés par type de volant dans `keisho_wheels.yml`, direction et pédales détectées par Keisho.
* Core libretro : **ACTIVER LE RETOUR DE FORCE**.

Pour plus de détails sur les volants, voir la page [**Volants**](../../../../controleurs/supported-controllers/volants.md).

### Raccourcis

**Supermodel**

<table><thead><tr><th width="195.75">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>ÉCHAP</td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée</td><td>F5</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement de la sauvegarde instantanée</td><td>F7</td></tr><tr><td><strong>HOTKEY + HAUT</strong></td><td>Changer d'emplacement de sauvegarde</td><td>F6</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test (option <strong>ÉMULATION > ACTIVER LE MENU SERVICE</strong>)</td><td>9 / 0</td></tr><tr><td>—</td><td>Pause</td><td>ALT + P</td></tr><tr><td>—</td><td>Réinitialiser</td><td>ALT + R</td></tr><tr><td>—</td><td>Capture d'écran</td><td>ALT + S</td></tr><tr><td>—</td><td>Plein écran</td><td>ALT + ENTRÉE</td></tr><tr><td>—</td><td>Effacer la NVRAM</td><td>ALT + N</td></tr></tbody></table>

**Model3-Vulkan**

<table><thead><tr><th width="193.25">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>ÉCHAP</td></tr><tr><td><strong>HOTKEY + SUD</strong></td><td>Menu de Model3-Vulkan</td><td>F1</td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement de la sauvegarde instantanée</td><td>F4</td></tr><tr><td><strong>HOTKEY + HAUT</strong></td><td>Changer d'emplacement de sauvegarde</td><td>F7</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test (option <strong>ÉMULATION > ACTIVER LE MENU SERVICE</strong>)</td><td>9 / 0</td></tr><tr><td>—</td><td>Capture d'écran</td><td>F8</td></tr><tr><td>—</td><td>Pause</td><td>P</td></tr><tr><td>—</td><td>Plein écran</td><td>ALT + ENTRÉE</td></tr><tr><td>—</td><td>Activer / désactiver les textures HD</td><td>ALT + H</td></tr><tr><td>—</td><td>Recharger les textures HD</td><td>F3</td></tr></tbody></table>

**Keisho** : mêmes raccourcis que pour le Model 1 (voir la page **Sega Model 1**). Dans les jeux de course, F1 à F5 servent aux rapports au clavier : le menu passe sur F10, la sauvegarde sur F6 et le chargement sur F7, et les raccourcis de la manette suivent automatiquement.

**Core libretro** : raccourcis RetroArch habituels (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

Les touches du clavier de Keisho et de Model3-Vulkan sont personnalisables, voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="350.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Supermodel : configuration</td><td><code>emulators\supermodel\Config\Supermodel.ini</code></td></tr><tr><td>Supermodel : NVRAM (réglages et records des bornes)</td><td><code>emulators\supermodel\NVRAM</code></td></tr><tr><td>Supermodel : sauvegardes instantanées</td><td><code>emulators\supermodel\Saves</code></td></tr><tr><td>Keisho : NVRAM</td><td><code>saves\model3\keisho</code></td></tr><tr><td>Keisho : sauvegardes instantanées (gérées par RetroBat)</td><td><code>saves\model3\keisho\sstates</code></td></tr><tr><td>Keisho : sauvegardes instantanées (dossier de l'émulateur)</td><td><code>saves\model3\keisho\states</code></td></tr><tr><td>Keisho : captures d'écran</td><td><code>screenshots\keisho</code></td></tr><tr><td>Keisho : configuration</td><td><code>emulators\keisho\keisho.ini</code></td></tr><tr><td>Model3-Vulkan : configuration</td><td><code>emulators\model3-vulkan\Data\Config\Model3-Vulkan.ini</code></td></tr><tr><td>Model3-Vulkan : sauvegardes instantanées (gérées par RetroBat)</td><td><code>saves\model3\model3-vulkan</code></td></tr><tr><td>Model3-Vulkan : sauvegardes instantanées (dossier de l'émulateur)</td><td><code>emulators\model3-vulkan\Data\Saves</code></td></tr><tr><td>Model3-Vulkan : NVRAM</td><td><code>emulators\model3-vulkan\Data\NVRAM</code></td></tr><tr><td>Model3-Vulkan : captures d'écran</td><td><code>emulators\model3-vulkan\Data\Screenshots</code></td></tr><tr><td>Model3-Vulkan : textures HD</td><td><code>emulators\model3-vulkan\Data\Assets\HDTextures\&#x3C;jeu></code></td></tr><tr><td>Correspondance des boutons par jeu</td><td><code>system\resources\inputmapping\supermodel.yml</code>, <code>keisho.yml</code>, <code>libretro_supermodel.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr><tr><td>Boutons des volants</td><td><code>system\resources\inputmapping\wheels\model3_wheels.yml</code> (Supermodel, Model3-Vulkan), <code>keisho_wheels.yml</code> (Keisho)</td></tr></tbody></table>

## Guides

### Menu Service

Le menu de test de chaque borne donne accès aux réglages du jeu (difficulté, calibration des pistolets, réseau…).

* Au clavier : **9** (Service) et **0** (Test), avec tous les émulateurs autonomes.
* À la manette : **L3** (Service) et **R3** (Test). Avec Supermodel et Model3-Vulkan, activez d'abord **ÉMULATION > ACTIVER LE MENU SERVICE** ; avec le core libretro, c'est le réglage par défaut de **CONTRÔLES > BOUTONS SERVICE**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure></div>

### Calibrer les pistolets

Avec Supermodel, Model3-Vulkan et le core libretro, ouvrez le menu de test, puis **GUN SETTINGS**, et suivez les indications à l'écran. Keisho n'en a pas besoin.

### Textures HD (Model3-Vulkan)

Model3-Vulkan peut remplacer les textures d'origine par des packs de textures HD. Placez le pack dans `emulators\model3-vulkan\Data\Assets\HDTextures\<jeu>` (`<jeu>` = nom du romset, par exemple `scud`) et activez **RENDU VISUEL > PACKS DE TEXTURES HD**.

### Autres options utiles

**Supermodel**

| Option                                          | Effet                                                                                                            |
| ----------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **VIDÉO > HACK ÉCRAN LARGE**                    | Affiche les jeux en 16/9 (ou étirés).                                                                            |
| **RENDU VISUEL > SURÉCHANTILLONNAGE**           | Lisse l'image, au prix des performances.                                                                         |
| **VIDÉO > NOUVEAU MOTEUR 3D**                   | Activé par défaut ; à désactiver seulement si le jeu affiche une erreur OpenGL sur une ancienne carte graphique. |
| **ÉMULATION > FRÉQUENCE DU PROCESSEUR POWERPC** | Automatique par défaut ; à augmenter si un jeu ralentit.                                                         |

**Model3-Vulkan**

<table><thead><tr><th width="352.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu.</td></tr><tr><td><strong>HACK ÉCRAN LARGE</strong></td><td>Affiche les jeux en 16/9 (ou étirés).</td></tr><tr><td><strong>RENDU VISUEL > FILTRE CRT</strong> / <strong>COULEURS CRT</strong></td><td>Aspect et couleurs d'un écran cathodique.</td></tr><tr><td><strong>RENDU VISUEL > DÉSACTIVER LE FLASH BLANC</strong></td><td>Retire le flash blanc des tirs.</td></tr><tr><td><strong>CONTRÔLES > LISSAGE DE LA DIRECTION</strong> / <strong>SENSIBILITÉ DE LA DIRECTION</strong></td><td>Réglage de la direction à la manette dans les jeux de course.</td></tr><tr><td><strong>VIDÉO > FAIBLE LATENCE</strong></td><td>Réduit le délai d'affichage.</td></tr></tbody></table>

**Keisho** : **RÉSOLUTION INTERNE**, **RAPPORT D'ASPECT**, **RENDU VISUEL > FILTRE CRT**, **AJUSTER LA LUMINOSITÉ** (aussi en Model 3), **ÉMULATION > REMBOBINAGE**. **TRANSPARENCE** et **PROFONDEUR DE VISION** ne s'appliquent qu'aux Model 1 et Model 2. Voir aussi la page [**Sega Model 1**](sega-model-1.md).

**Core libretro** : **RÉSOLUTION INTERNE**, **VIDÉO > HACK ÉCRAN LARGE**, **ÉMULATION > FRÉQUENCE DU PROCESSEUR POWERPC**.

## Problèmes connus

<table><thead><tr><th width="365.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Message « Network Board Not Present »</td><td>Ouvrez le menu de test, puis <strong>Game Assignments > Link ID</strong>, et choisissez <strong>Single</strong>. Keisho n'a pas ce problème.</td></tr><tr><td>Avec Supermodel, la manette du joueur 2 ne répond pas</td><td>Les deux manettes doivent utiliser le même pilote que celle du joueur 1 (deux manettes XInput, ou deux manettes non XInput). Changez le pilote dans <strong>PILOTES > MANETTES</strong>, ou essayez Model3-Vulkan ou Keisho.</td></tr><tr><td>Les manettes des joueurs 1 et 2 sont inversées (Supermodel)</td><td>Activez <strong>CONTRÔLES > INVERSER LES INDEX MANETTES</strong>, ou forcez l'index de chaque manette.</td></tr><tr><td>Un clone ne démarre pas</td><td>Placez le jeu parent dans <code>roms\model3</code>, ou utilisez un <a href="../../../arcade-guide.md#types-de-romsets">romset non-merged</a>.</td></tr><tr><td>Le viseur des jeux au pistolet ne suit pas le pistolet</td><td>Calibrez le pistolet dans le menu de test (<strong>GUN SETTINGS</strong>).</td></tr><tr><td>Model3-Vulkan ne démarre pas</td><td>Vérifiez que la carte graphique et son pilote gèrent Vulkan 1.3, sinon utilisez Supermodel ou Keisho.</td></tr><tr><td>Prototypes de Sega Rally 2 (<code>srally2p</code>, <code>srally2pa</code>) : écran noir avec Keisho</td><td>Ces romsets ne fonctionnent pas encore avec Keisho : utilisez Supermodel.</td></tr></tbody></table>
