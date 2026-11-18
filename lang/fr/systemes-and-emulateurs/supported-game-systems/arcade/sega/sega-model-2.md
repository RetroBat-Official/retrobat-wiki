---
description: Sega
---

# Sega Model 2

<div align="left"><figure><img src="../../../../.gitbook/assets/image (1) (1).png" alt="" width="259"><figcaption></figcaption></figure></div>

## Présentation

Le **Sega Model 2** est la deuxième carte d'arcade 3D de Sega, sortie en 1994. Elle succède au Model 1 et ajoute le placage de textures, le filtrage et l'anticrénelage, ce qui donne aux jeux un rendu très en avance sur les consoles de l'époque. Plusieurs révisions se sont succédé (Model 2, 2A-CRX, 2B-CRX, 2C-CRX).

La ludothèque compte une quarantaine de jeux, dont de nombreux classiques de l'arcade : **Daytona USA**, **Virtua Fighter 2**, **Virtua Cop** 1 et 2, **Sega Rally Championship**, **The House of the Dead**, **Dead or Alive**, **Fighting Vipers**, **Virtual On** ou **Sega Touring Car Championship**.

RetroBat propose six émulateurs : **m2emulator** (l'émulateur historique d'ElSemi, en version multi-cœur ou simple cœur), **Keisho** (anciennement sm2-emu, un émulateur dédié aux Model 1, 2 et 3), le core libretro **sm2** (issu de sm2-emu), **Supermodel**, et **MAME** en version autonome ou en core libretro.

{% embed url="https://fr.wikipedia.org/wiki/Model_2" %}

## En bref

<table><thead><tr><th width="284"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\model2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>m2emulator (multicpu)</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (le core libretro sm2 utilise <code>bios\sm2-emu\games.xml</code>, voir BIOS)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, Keisho ; Supermodel et MAME par raccourcis ; pas avec m2emulator</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core libretro mame</td></tr><tr><td><strong>Pistolets</strong></td><td>m2emulator, Keisho, core libretro sm2, MAME</td></tr><tr><td><strong>Volants</strong></td><td>m2emulator, Keisho, Supermodel</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="145.75">Émulateur</th><th width="333.5">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>m2emulator</strong> (défaut)</td><td>La référence : tous les jeux, contrôles réglés jeu par jeu, pistolets (avec DemulShooter), volants et retour de force.</td><td>Ancien (Direct3D 9). Pas de sauvegardes instantanées.</td></tr><tr><td><strong>Keisho</strong> / <strong>libretro: sm2</strong></td><td>Émulateurs modernes : les quatre cartes Model 2 (original, 2A, 2B, 2C), résolution augmentée, Vulkan / OpenGL, filtre CRT, sauvegardes instantanées, retour arrière.</td><td>Développement récent.</td></tr><tr><td><strong>supermodel</strong></td><td>Gère aussi le Model 2 (environ 90 romsets), mode écran large.</td><td>Support du Model 2 récent. Sauvegardes instantanées au clavier uniquement.</td></tr><tr><td><strong>libretro: mame</strong> / <strong>mame64</strong></td><td>Seul émulateur avec le jeu en réseau (core libretro).</td><td>Plus lent, compatibilité variable selon les jeux.</td></tr></tbody></table>

**m2emulator** existe en deux versions : **multicpu** (défaut) répartit l'émulation sur plusieurs cœurs du processeur ; **singlecpu** est à essayer si un jeu se comporte mal.

## BIOS

Le Model 2 n'a pas de BIOS.

Le **core libretro sm2** a besoin de sa base de jeux `bios\sm2-emu\games.xml`, installée avec le core. Elle doit correspondre à la version du core : en cas de problème, mettez le core à jour plutôt que de remplacer ce fichier à la main. RetroBat le contrôle comme BIOS optionnel.

## Quel format de jeu ?

Les jeux sont des archives `.zip` au format MAME, à garder sans les décompresser et sans les renommer.

* Les clones (`daytonas`, `vf2b`, `srallycb`…) ont besoin de leur jeu parent (`daytona`, `vf2`, `srallyc`) dans le même dossier, sauf avec un romset non-merged.
* m2emulator ne lit que les archives `.zip`.

L'extension `.decomp` correspond aux portages PC, voir la page [**Recompilations**](../../autres/recomp.md).

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour tous les émulateurs. Avec m2emulator, la configuration est écrite jeu par jeu, pour les jeux listés ci-dessous ; les autres jeux gardent la configuration faite dans l'émulateur.

L'option **AUTOCONFIGURER LES MANETTES** permet de garder sa propre configuration.

### Pilote des manettes (m2emulator)

m2emulator utilise par défaut le pilote XInput. Si votre manette n'est pas compatible XInput, choisissez **PILOTES > CONTRÔLEUR > DINPUT** dans les options avancées du système. RetroBat passe aussi en DInput tout seul s'il ne trouve aucune manette XInput.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

### Contrôles par jeu (m2emulator)

Pour tous les jeux : **START** = Start, **SELECT** = pièce.

**Jeux de combat**

Déplacements à la croix directionnelle.

| Jeu                           | SUD      | EST     | OUEST | NORD |
| ----------------------------- | -------- | ------- | ----- | ---- |
| Virtua Fighter 2 (`vf2`)      | Garde    | —       | Poing | Pied |
| Dead or Alive (`doa`)         | Pied     | Prise   | Poing | —    |
| Fighting Vipers (`fvipers`)   | Garde    | Garde 2 | Poing | Pied |
| Last Bronx (`lastbrnx`)       | Garde    | —       | Poing | Pied |
| Sonic the Fighters (`schamp`) | Barrière | —       | Poing | Pied |

**Jeux standards**

Déplacements à la croix directionnelle.

| Jeu                         | SUD          | EST | OUEST        | NORD |
| --------------------------- | ------------ | --- | ------------ | ---- |
| Dynamite Cop (`dynamcop`)   | Saut         | —   | Poing        | Pied |
| Pilot Kids (`pltkids`)      | Bombe        | —   | Tir          | —    |
| Virtua Striker (`vstriker`) | Passe longue | Tir | Passe courte | —    |
| Zero Gunner (`zerogun`)     | Bombe        | —   | Tir          | —    |

**DISPOSITION DES BOUTONS** adapte les boutons de ces jeux aux sticks arcade (modern8, 8alternative, 6alternative). Pour plus de détails sur les dispositions arcade, voir la page [**Le Guide Arcade**](../../../arcade-guide.md). Les boutons sont réglés dans le fichier `system\resources\inputmapping\model2.yml`, que vous pouvez copier dans `user\inputmapping` pour le modifier.

**Jeux de course**

Pour tous les jeux de course : stick gauche = direction, **R2** = accélérateur, **L2** = frein.

| Jeu                                                                                           | SUD       | EST | OUEST     | NORD | Rapports                                        |
| --------------------------------------------------------------------------------------------- | --------- | --- | --------- | ---- | ----------------------------------------------- |
| Daytona USA (`daytona`)                                                                       | VR2       | VR4 | VR3       | VR1  | Stick droit : haut 1, bas 2, gauche 3, droite 4 |
| Sega Rally Championship (`srallyc`)                                                           | —         | —   | —         | Vue  | Stick droit : haut 1, bas 2, gauche 3, droite 4 |
| Indianapolis 500 (`indy500`), Sega Touring Car Championship (`stcc`), Super GT 24h (`sgt24h`) | Rapport − | Vue | Rapport + | Vue  | SUD / OUEST                                     |
| Over Rev (`overrev`)                                                                          | Rapport − | Vue | Rapport + | —    | SUD / OUEST                                     |
| Manx TT Superbike (`manxtt`)                                                                  | Rapport − | —   | Rapport + | —    | SUD / OUEST                                     |
| Motor Raid (`motoraid`)                                                                       | Pied      | —   | Poing     | —    | —                                               |

L'option **CONTRÔLES > UTILISER R1/L1 POUR LES JEUX DE COURSE** met l'accélérateur et le frein sur R1 / L1 ; elle ne fonctionne qu'avec la boîte de vitesses automatique du jeu.

**Autres jeux**

| Jeu                               | Commandes                                                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Desert Tank (`desert`)            | Stick gauche : avancer et tourner ; stick droit : tourelle ; L2 : marche arrière ; R2 : canon ; R1 : mitrailleuse ; NORD, SUD, OUEST : boutons VR1, VR2, VR3 |
| Dynamite Baseball 97 (`dynabb97`) | Stick gauche : déplacements ; R2 : frapper / lancer ; SUD : Hold ; OUEST : lancer la balle                                                                   |
| Sega Ski Super G (`skisuprg`)     | Stick gauche : tourner ; stick droit : tourner plus fort ; OUEST, SUD, EST : Select 1, 2, 3                                                                  |
| Sega Water Ski (`segawski`)       | Stick gauche : tourner ; L2 / R2 : pédales gauche / droite                                                                                                   |
| Sky Target (`skytargt`)           | Stick gauche : déplacements ; R2 : mitrailleuse ; L2 : missiles ; NORD : vue                                                                                 |
| Top Skater (`topskatr`)           | Stick gauche : tourner ; stick droit : tourner plus fort ; SUD : ollie ; NORD : nollie ; OUEST / EST : Select gauche / droite                                |
| Virtual On Cybertroopers (`von`)  | Stick gauche et stick droit : les deux manches ; L2 / R2 : armes gauche / droite ; OUEST / EST : turbo gauche / droite                                       |
| Wave Runner (`waverunr`)          | Stick gauche : tourner ; stick droit : tourner plus fort ; R2 : accélérer ; NORD : vue                                                                       |

### Keisho, core libretro sm2 et Supermodel

Keisho, le core libretro sm2 et Supermodel suivent la même logique : direction au stick gauche, accélérateur / frein sur R2 / L2, rapports sur L1 / R1 ou au stick droit pour les boîtes 4 vitesses, Start / pièce sur START / SELECT, Service / Test sur L3 / R3. Les boutons de chaque jeu sont réglés dans `keisho.yml` et `supermodel.yml` (`system\resources\inputmapping`), que vous pouvez copier dans `user\inputmapping` pour les modifier (le core libretro sm2 a sa propre disposition). **DISPOSITION DES BOUTONS** est aussi disponible. Pour plus de détails sur `keisho.yml`, voir la page [**Configuration des touches Keisho**](../../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-keisho.md).

Avec Keisho, les jeux au pistolet se jouent aussi à la manette : stick gauche ou droit = visée, **SUD** ou **R2** = tir, **EST** ou **L2** = recharger / missiles. Dans les jeux de course, les boutons de vue (VR1 à VR4) restent toujours sur les boutons de face. Virtual On, Desert Tank, Sky Target, Ski Super G et Water Ski ont une disposition propre à Keisho, qui ne se modifie pas.

Avec le core libretro sm2 :

* **CONTRÔLES > TEST/SERVICE SUR L3/R3** (activé par défaut) : L3 = Service, R3 = Test.
* **CONTRÔLES > BOÎTE 4 VITESSES** : **GRILLE EN H** (diagonales, comme une vraie grille) ou **DIRECTIONS** (haut 1, bas 2, gauche 3, droite 4). L1 / R1 descendent et montent toujours les rapports.

### Pistolets

Jeux au pistolet : Behind Enemy Lines (`bel`), Gunblade NY (`gunblade`), The House of the Dead (`hotd`), Rail Chase 2 (`rchase2`), Virtua Cop (`vcop`), Virtua Cop 2 (`vcop2`).

Activez **PISTOLETS > ACTIVER LES PISTOLETS**.

**m2emulator**

| Action                    | Commande                       |
| ------------------------- | ------------------------------ |
| Tir                       | Gâchette / clic gauche         |
| Recharger, missiles       | Bouton secondaire / clic droit |
| Start joueur 1 / joueur 2 | 1 / 2                          |
| Pièce joueur 1 / joueur 2 | 5 / 6                          |

* Avec une Wiimote et une DolphinBar : croix droite = Start, croix gauche = pièce (joueur 2 : haut = Start, bas = pièce).
* **PISTOLETS > FORCER LE CLAVIER POUR START/PIÈCE** garde 1 / 2 et 5 / 6 quel que soit le pistolet.
* DemulShooter est lancé automatiquement avec deux pistolets (option **PISTOLETS > UTILISER DEMULSHOOTER**).
* **PISTOLETS > INDEX SOURIS JOUEUR 1** / **JOUEUR 2** choisit le pistolet de chaque joueur s'il n'est pas reconnu correctement.
* **PISTOLETS > AFFICHER CIBLE** affiche le viseur (les types DS ne fonctionnent qu'avec DemulShooter).

**Keisho** : sans l'option **ACTIVER LES PISTOLETS**, Keisho est en mode automatique : il affiche le viseur dans les jeux au pistolet, et l'on vise à la souris ou au stick de la manette. Avec l'option, il utilise les pistolets branchés (joueurs 1 et 2) et cache aussi le curseur dans les autres jeux. Options **AFFICHER CIBLE** et **MASQUER LE FLASH DES TIRS** (avec ou sans pistolet), **TAILLE DE LA BORDURE SINDEN**, **ACTIVER LE RECUL DU PISTOLET**, **PUISSANCE DU RECUL** (avec pistolet). Start et pièce restent au clavier (1 / 5 joueur 1, 2 / 6 joueur 2).

**Core libretro sm2** : options **AFFICHER CIBLE**, **MASQUER LE VISEUR INACTIF**, **MASQUER LE FLASH DES TIRS**. Sans pistolet, il vise au stick (**CONTRÔLES > VISÉE AU STICK** : **RELATIF** ou **ABSOLU**).

Chaque jeu doit être calibré dans son menu de test (voir [**Calibrer les pistolets**](sega-model-2.md#calibrer-les-pistolets) plus bas). Pour plus de détails sur les pistolets, voir la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/).

### Volants

m2emulator, Keisho et Supermodel gèrent les volants, avec l'option **VOLANTS DE COURSE > ACTIVER LES VOLANTS**.

* m2emulator : **ACTIVER LE RETOUR DE FORCE** (activé par défaut avec un volant), **GARDER LES VITESSES** (retour au point mort quand on relâche le levier de vitesses), choix du levier de vitesses séparé. Les commandes sont réglées par type de volant et par jeu dans `model2_wheels.yml`.
* Keisho : **ACTIVER LE RETOUR DE FORCE** et **FORCE DU RETOUR DE FORCE**. Les boutons sont réglés par type de volant dans `keisho_wheels.yml` ; la direction et les pédales sont détectées par Keisho.
* Supermodel : **ACTIVER LE RETOUR DE FORCE**.

Pour plus de détails sur les volants, voir la page [**Volants**](../../../../controleurs/supported-controllers/volants.md).

### Raccourcis

**m2emulator**

<table><thead><tr><th width="177">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>ÉCHAP</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test (option <strong>ÉMULATION > ACTIVER LE MENU SERVICE</strong>)</td><td>9 / 0</td></tr><tr><td>—</td><td>Quitter le plein écran et afficher le menu de l'émulateur</td><td>ALT + ENTRÉE</td></tr></tbody></table>

**Keisho et Supermodel** : mêmes raccourcis que pour le Model 1, voir la page [**Sega Model 1**](sega-model-1.md).

**Cores libretro** : raccourcis RetroArch habituels (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)). **MAME** : voir la page [**MAME**](../mame.md).

## Dossiers

<table><thead><tr><th width="332.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>m2emulator : configuration</td><td><code>emulators\m2emulator\Emulator.ini</code></td></tr><tr><td>m2emulator : contrôles de chaque jeu</td><td><code>emulators\m2emulator\CFG</code> (un fichier <code>.input</code> par jeu)</td></tr><tr><td>m2emulator : modèles de contrôles</td><td><code>emulators\m2emulator\templatescfg\xinput</code>, <code>templatescfg\dinput</code></td></tr><tr><td>m2emulator : NVRAM (réglages et records des bornes)</td><td><code>emulators\m2emulator\NVDATA</code></td></tr><tr><td>m2emulator : scripts des jeux (écran large…)</td><td><code>emulators\m2emulator\scripts</code></td></tr><tr><td>m2emulator : copie du jeu lancé</td><td><code>emulators\m2emulator\roms</code> (vidé à chaque lancement)</td></tr><tr><td>Keisho : NVRAM</td><td><code>saves\model2\keisho</code></td></tr><tr><td>Keisho : sauvegardes instantanées (gérées par RetroBat)</td><td><code>saves\model2\keisho\sstates</code></td></tr><tr><td>Keisho : sauvegardes instantanées (dossier de l'émulateur)</td><td><code>saves\model2\keisho\states</code></td></tr><tr><td>Keisho : captures d'écran</td><td><code>screenshots\keisho</code></td></tr><tr><td>Keisho : configuration</td><td><code>emulators\keisho\keisho.ini</code></td></tr><tr><td>Core libretro sm2 : base des jeux</td><td><code>bios\sm2-emu\games.xml</code></td></tr><tr><td>Supermodel : configuration</td><td><code>emulators\supermodel\Config\Supermodel.ini</code></td></tr><tr><td>Supermodel : NVRAM</td><td><code>emulators\supermodel\NVRAM</code></td></tr><tr><td>Supermodel : sauvegardes instantanées</td><td><code>emulators\supermodel\Saves</code></td></tr><tr><td>Correspondance des boutons par jeu</td><td><code>system\resources\inputmapping\model2.yml</code>, <code>keisho.yml</code>, <code>supermodel.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr><tr><td>Boutons des volants</td><td><code>system\resources\inputmapping\wheels\model2_wheels.yml</code> (m2emulator), <code>keisho_wheels.yml</code> (Keisho)</td></tr></tbody></table>

Pour les dossiers de MAME, voir la page [**MAME**](../mame.md).

## Guides

### Menu Service

Le menu de test de chaque borne donne accès aux réglages du jeu (difficulté, nombre de vies, calibration des pistolets…).

* **m2emulator** : au clavier, **9** (Service) et **0** (Test). Pour utiliser la manette, activez **ÉMULATION > ACTIVER LE MENU SERVICE** : **R3** (Test) ouvre le menu, **L3** (Service) passe d'une ligne à l'autre.
* **Core libretro sm2** : L3 / R3, activé par défaut (**CONTRÔLES > TEST/SERVICE SUR L3/R3**).
* **Keisho**, **Supermodel** : voir la page [**Sega Model 1**](sega-model-1.md).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure></div>

### Calibrer les pistolets

Les jeux au pistolet doivent être calibrés dans le jeu : ouvrez le menu de test, puis **GUN SETTINGS**, et suivez les indications à l'écran.

### Utiliser sa propre configuration de touches (m2emulator)

1. Lancez le jeu, appuyez sur **ALT + ENTRÉE** pour afficher le menu de l'émulateur, puis ouvrez **Game > Configure Controls** et réglez les touches.
2. Quittez l'émulateur : le fichier `<jeu>.input` est enregistré dans `emulators\m2emulator\CFG`.
3. Copiez-le dans `emulators\m2emulator\templatescfg\xinput` ou `templatescfg\dinput`, selon le pilote choisi, en lui donnant **le nom du jeu parent** (par exemple `daytona.input` pour `daytonas`).
4. Dans les options avancées du système, choisissez **CONTRÔLES > MÉTHODE DE CONFIGURATION DES CONTRÔLES > MODÈLES**.

RetroBat copie alors ce fichier à chaque lancement (sauf si les pistolets sont activés). Le guide complet, avec le mapping par jeu `model2.yml`, est sur la page [**Configuration des touches m2emulator**](../../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-m2emulator.md).

### Autres options utiles

**m2emulator**

<table><thead><tr><th width="342.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>HACK ÉCRAN LARGE</strong></td><td>Affiche les jeux en 16/9 (meilleur résultat avec les jeux entièrement en 3D).</td></tr><tr><td><strong>RENDU VISUEL > FORCER LA GESTION DES TEXTURES</strong></td><td>À activer si l'émulateur plante après le chargement ou n'affiche rien.</td></tr><tr><td><strong>RENDU VISUEL > ANTICRÉNELAGE</strong></td><td>Lisse les bords des polygones.</td></tr><tr><td><strong>CONTRÔLES > INVERSER LES INDEX MANETTES</strong></td><td>Échange les manettes des joueurs 1 et 2 (XInput).</td></tr><tr><td><strong>CONTRÔLES > FORCER L'INDEX DE LA MANETTE DU JOUEUR 1</strong> / <strong>JOUEUR 2</strong></td><td>Choisit la manette de chaque joueur, utile sur une borne.</td></tr></tbody></table>

**Keisho et core libretro sm2**

| Option                                           | Effet                                                                                  |
| ------------------------------------------------ | -------------------------------------------------------------------------------------- |
| **RÉSOLUTION INTERNE**                           | Augmente la résolution de rendu (Vulkan et OpenGL).                                    |
| **FRÉQUENCE NATIVE (57,5 HZ)** (core libretro)   | Fréquence d'origine de la borne au lieu de 60 Hz ; peut saccader sur un écran 60 Hz.   |
| **RENDU VISUEL > FILTRE CRT** (Keisho)           | Aspect d'un écran cathodique.                                                          |
| **RENDU VISUEL > TRANSPARENCE** (Keisho)         | **MÉLANGÉE** : transparences lissées au lieu du damier de la borne (Vulkan et OpenGL). |
| **RENDU VISUEL > PROFONDEUR DE VISION** (Keisho) | Affiche le décor jusqu'au bout du circuit dans les jeux compatibles (Daytona USA).     |
| **AUDIO > VOLUME DE LA MUSIQUE** (Keisho)        | Volume de la carte musique (Daytona USA, Sega Rally).                                  |
| **ÉMULATION > REMBOBINAGE** (Keisho)             | Active le retour arrière.                                                              |

Pour les options de Keisho et de Supermodel, voir aussi la page [**Sega Model 1**](sega-model-1.md).

## Problèmes connus

| Problème                                                | Solution                                                                                                                                                                          |
| ------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Message « Network Board Not Present »                   | <p>Ouvrez le menu de test, puis <strong>Game System > Link ID</strong>, et choisissez <strong>Single</strong><br><img src="../../../../.gitbook/assets/image (3).png" alt=""></p> |
| Un clone ne démarre pas                                 | Placez le jeu parent dans `roms\model2`, ou utilisez un [romset non-merged](../../../arcade-guide.md#types-de-romsets).                                                           |
| La manette ne répond pas avec m2emulator                | Choisissez **PILOTES > CONTRÔLEUR > DINPUT**.                                                                                                                                     |
| Les manettes des joueurs 1 et 2 sont inversées          | Activez **CONTRÔLES > INVERSER LES INDEX MANETTES**, ou forcez l'index de chaque manette.                                                                                         |
| Un jeu plante ou reste noir avec m2emulator             | Activez **RENDU VISUEL > FORCER LA GESTION DES TEXTURES**, ou essayez la version **singlecpu**.                                                                                   |
| Des fichiers ont disparu de `emulators\m2emulator\roms` | Ce dossier est vidé à chaque lancement : rangez vos jeux dans `roms\model2`.                                                                                                      |
| Le core libretro sm2 ne lance aucun jeu                 | Vérifiez que `bios\sm2-emu\games.xml` est présent ; mettez le core à jour si besoin.                                                                                              |
