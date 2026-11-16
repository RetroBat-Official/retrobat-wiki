---
description: Microsoft
---

# Xbox

<div align="left"><figure><img src="../../../../.gitbook/assets/image (582).png" alt="" width="425"><figcaption></figcaption></figure></div>

{% embed url="https://fr.wikipedia.org/wiki/Xbox" %}

## Présentation

La **Xbox** est la première console de salon de Microsoft. Elle sort en novembre 2001 aux États-Unis, puis en février 2002 au Japon et en mars 2002 en Europe. Elle est construite comme un PC : un processeur Intel Pentium III à 733 MHz, une puce graphique NVIDIA (NV2A), 64 Mo de mémoire et, pour la première fois sur une console, un disque dur intégré de 8 Go qui garde les sauvegardes et les musiques copiées depuis des CD.

Sa grosse manette d'origine, surnommée « Duke », est vite remplacée par la **Controller S**, plus compacte. En 2002, le service **Xbox Live** ouvre le jeu en ligne sur console grâce au port Ethernet de la machine. La Xbox s'est vendue à environ 24 millions d'exemplaires avant d'être remplacée par la Xbox 360 fin 2005. Parmi ses jeux marquants : Halo: Combat Evolved, Halo 2, Fable, Star Wars: Knights of the Old Republic, Ninja Gaiden, Jet Set Radio Future ou Project Gotham Racing.

RetroBat propose trois émulateurs : **xemu**, qui reproduit le matériel de la console et utilise son BIOS, **xbased**, qui réimplémente le système de la Xbox et affiche les jeux avec Vulkan, et **Cxbx-Reloaded**, qui remplace le système de la Xbox par son propre code. xbased et Cxbx-Reloaded n'ont pas besoin de BIOS.

## En bref

<table><thead><tr><th width="274"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\xbox</code></td></tr><tr><td><strong>Extensions</strong></td><td>.xbe .iso .chd .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>xemu</td></tr><tr><td><strong>BIOS</strong></td><td><code>mcpx_1.0.bin</code> et <code>Complex_4627.bin</code> (xemu uniquement)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>xbased (xemu : snapshots depuis son menu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>cxbx</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>Cerbios.bin</code>, <code>Complex_4627v1.03.bin</code> (xemu, option FORCER LE FIRMWARE)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="140.75">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>xemu</strong> (défaut)</td><td>Le plus compatible. Émule le vrai matériel : disque dur, EEPROM, tableau de bord. Résolution augmentée, Vulkan ou OpenGL, snapshots.</td><td>Demande le BIOS. Ne lit que les images disque au format XISO (<code>.iso</code>). Pas de pistolets.</td></tr><tr><td><strong>xbased</strong></td><td>Pas de BIOS. Lit les images Redump et <code>.chd</code> sans conversion. Sauvegardes instantanées gérées par RetroBat. Patchs (60 ips, écran large) et codes de triche intégrés, filtres CRT.</td><td>Émulateur récent (première version en novembre 2026). Demande une carte graphique compatible Vulkan 1.1. Pas de pistolets.</td></tr><tr><td><strong>cxbx</strong> (Cxbx-Reloaded)</td><td>Pas de BIOS. Lance les jeux extraits (<code>.xbe</code>). Gère le pistolet EMS TopGun.</td><td>Compatibilité plus faible, plus de bugs graphiques. Les <code>.iso</code> demandent l'installation de Dokan 2.</td></tr></tbody></table>

La liste de compatibilité de xemu ([xemu.app](https://xemu.app/#compatibility)) indique l'état de chaque jeu. En cas de problème avec un jeu, essayez un autre émulateur.

## BIOS

Seul **xemu** a besoin du BIOS. xbased et Cxbx-Reloaded n'en utilisent aucun.

<table><thead><tr><th width="211.75">Fichier</th><th width="89">Dossier</th><th>Rôle</th><th>MD5</th></tr></thead><tbody><tr><td><code>mcpx_1.0.bin</code></td><td><code>bios</code></td><td>ROM de démarrage (MCPX), obligatoire</td><td>d49c52a4102f6df7bcf8d0617ac475ed</td></tr><tr><td><code>Complex_4627.bin</code></td><td><code>bios</code></td><td>BIOS (flash) utilisé par défaut</td><td>39cee882148a87f93cb440b99dde3ceb</td></tr><tr><td><code>Cerbios.bin</code></td><td><code>bios</code></td><td>BIOS alternatif, facultatif</td><td></td></tr><tr><td><code>Complex_4627v1.03.bin</code></td><td><code>bios</code></td><td>BIOS alternatif, facultatif</td><td></td></tr></tbody></table>

RetroBat contrôle `mcpx_1.0.bin` et `Complex_4627.bin`. Les BIOS alternatifs ne servent que si vous les choisissez avec l'option **ÉMULATION > FORCER LE FIRMWARE** de xemu.

Le disque dur et l'EEPROM de la console ne sont pas des BIOS à ajouter : au premier lancement, RetroBat crée `xbox_hdd.qcow2` (un disque dur formaté, sans tableau de bord) et `eeprom.bin` dans `saves\xbox`. xbased crée de même son propre disque dur, avec son EEPROM, dans `saves\xbox\xbased\hdd`.

Pour plus de détails sur l'installation et la vérification des BIOS, voir la page **Ajouter les BIOS**.

### Langue de la console

La langue des jeux est celle de l'EEPROM de la console. RetroBat la règle à chaque lancement, pour les trois émulateurs :

* par défaut, c'est la langue de RetroBat (anglais si elle n'existe pas sur Xbox) ;
* l'option **ÉMULATION > LANGUE** force une langue : anglais, japonais, allemand, français, espagnol, italien, coréen, chinois ou portugais.

Un jeu qui n'existe pas dans la langue choisie s'affiche dans sa langue par défaut, souvent l'anglais.

## Quel format de jeu ?

<table><thead><tr><th width="152.25">Format</th><th width="61">xemu</th><th width="84">xbased</th><th width="70.25">cxbx</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.iso</strong> (XISO)</td><td>✅</td><td>✅</td><td>✅</td><td>Image disque au format Xbox (XISO). Avec Cxbx, l'image est montée comme un lecteur grâce à Dokan 2 (voir <a href="xbox.md#lancer-les-.iso-avec-cxbx">Guides, « Lancer les .iso avec Cxbx »</a>).</td></tr><tr><td><strong>.iso</strong> (Redump)</td><td>❌</td><td>✅</td><td>❌</td><td>Image complète du disque, avec la partie vidéo. xbased la lit telle quelle ; pour xemu et Cxbx, elle est à convertir en XISO (voir <a href="xbox.md#convertir-une-image-redump-en-xiso">Guides, « Convertir une image Redump en XISO »</a>).</td></tr><tr><td><strong>.chd</strong></td><td>❌</td><td>✅</td><td>❌</td><td>Image compressée, créée avec <code>chdman createdvd</code> à partir d'une image XISO ou Redump.</td></tr><tr><td><strong>.xbe</strong></td><td>❌</td><td>✅</td><td>✅</td><td>Exécutable d'un jeu extrait. xbased ne lance que le fichier <code>default.xbe</code> du jeu, Cxbx accepte tous les <code>.xbe</code>.</td></tr><tr><td><strong>Dossier <code>.decomp</code></strong></td><td>—</td><td>—</td><td>—</td><td>Portage PC d'un jeu (décompilation) : RetroBat lance l'exécutable (<code>.exe</code>) du dossier, quel que soit l'émulateur choisi.</td></tr></tbody></table>

Les archives `.zip` et `.7z` ne sont pas acceptées : les jeux Xbox doivent rester décompressés. Pour gagner de la place, xbased accepte le format `.chd`.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour les trois émulateurs, jusqu'à 4 joueurs, dans l'ordre des joueurs de RetroBat. L'option **AUTOCONFIGURER LES MANETTES** permet de désactiver cette configuration pour garder celle faite dans l'émulateur.

| Xbox                         | Manette                      |
| ---------------------------- | ---------------------------- |
| A                            | SUD                          |
| B                            | EST                          |
| X                            | OUEST                        |
| Y                            | NORD                         |
| Blanc                        | L1                           |
| Noir                         | R1                           |
| Gâchettes gauche et droite   | L2, R2                       |
| Back                         | SELECT                       |
| Start                        | START                        |
| Clics des sticks             | L3, R3                       |
| Croix directionnelle, sticks | Croix directionnelle, sticks |

* **xemu** reprend la disposition de chaque manette reconnue par SDL : les manettes Xbox, DualShock 4, DualSense et Switch Pro fonctionnent sans réglage. Les vibrations sont actives.
* **xbased** reprend aussi la disposition de chaque manette reconnue par SDL. **CONTRÔLES > ZONE MORTE JOYSTICK** règle la zone morte des sticks (10 % par défaut) et **CONTRÔLES > ACTIVER LES VIBRATIONS** les vibrations (activées par défaut). Une configuration des touches faite pour un jeu dans xbased reste prioritaire.
* **Cxbx** émule par défaut une **Controller S**. L'option **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** (à 4) choisit **MANETTE S** ou **MANETTE DUKE**. Les vibrations s'activent avec **CONTRÔLES > ACTIVER LES VIBRATIONS**.

### Clavier

Un clavier attribué à un joueur dans RetroBat est configuré avec ces touches. xbased utilise le clavier pour le joueur 1 quand aucune manette n'est branchée :

| Xbox                                     | xemu                   | xbased                   | cxbx           |
| ---------------------------------------- | ---------------------- | ------------------------ | -------------- |
| A, B, X, Y                               | A, B, X, Y             | ESPACE, MAJ GAUCHE, Q, E | S, D, W, E     |
| Blanc, Noir                              | 1, 2                   | Z, C                     | X, C           |
| Gâchettes gauche, droite                 | W, O                   | 1, 3                     | Q, R           |
| Back, Start                              | RETOUR ARRIÈRE, ENTRÉE | RETOUR ARRIÈRE, ENTRÉE   | ESPACE, ENTRÉE |
| Croix directionnelle                     | Flèches                | Flèches                  | Flèches        |
| Stick gauche (haut, gauche, bas, droite) | E, S, D, F             | W, A, S, D               | T, F, G, H     |
| Stick droit (haut, gauche, bas, droite)  | I, J, K, L             | I, J, K, L               | I, J, K, L     |
| Clics des sticks                         | 3, 4                   | F, H                     | B, M           |

Pour xemu et Cxbx, les touches sont données pour un clavier QWERTY : ces émulateurs utilisent la position des touches, pas leur lettre. xbased utilise la lettre : sur un clavier AZERTY, ce sont les touches marquées de ces lettres.

### Pistolets

Les pistolets ne fonctionnent qu'avec **Cxbx**, qui émule le pistolet **EMS TopGun** sur le port du joueur 1. Il sert à des jeux comme The House of the Dead III, Silent Scope Complete ou Starsky & Hutch.

Activez l'option **PISTOLETS > ACTIVER LES PISTOLETS** (ou choisissez **EMS TOPGUN** dans **TYPE DE CONTRÔLEUR JOUEUR 1**).

| EMS TopGun        | Pistolet / souris                   |
| ----------------- | ----------------------------------- |
| Visée             | Pistolet ou souris                  |
| Gâchette          | Gâchette (clic gauche)              |
| Grip              | Bouton de rechargement (clic droit) |
| START             | Touche 1                            |
| SE/BA             | Touche 5                            |
| A, B              | Touches S, D                        |
| Stick du pistolet | Flèches                             |

* **PISTOLETS > INVERSER GÂCHETTE ET RECHARGE** inverse la gâchette et le grip (utile avec un WiiZapper).
* Avec une Wiimote sur DolphinBar, la croix sert de stick, START est sur le bouton 1 ou sur + selon le mode de la DolphinBar, et SE/BA sur le bouton 2 (mode 1 seulement).
* Avec un pistolet Sinden, RetroBat lance automatiquement le logiciel Sinden.

Pour plus de détails sur les pistolets, voir la page [**Pistolets**](xbox.md#pistolets).

### Raccourcis

#### **xemu**

| Raccourci                        | Action                                                            | Clavier       |
| -------------------------------- | ----------------------------------------------------------------- | ------------- |
| **HOTKEY + START**               | Quitter                                                           | CTRL + Q      |
| **GUIDE**, ou **SELECT + START** | Menu rapide de xemu (capture, snapshot, pause, réglages, quitter) | F2            |
| —                                | Menu principal de xemu (réglages, snapshots)                      | F1            |
| —                                | Charger le snapshot associé à la touche                           | F5 à F8       |
| —                                | Créer le snapshot associé à la touche                             | MAJ + F5 à F8 |
| —                                | Capture d'écran                                                   | F12           |
| —                                | Pause                                                             | CTRL + P      |
| —                                | Redémarrer                                                        | CTRL + R      |
| —                                | Plein écran                                                       | F11           |

#### **xbased**

| Raccourci                      | Action                                                                   | Clavier                        |
| ------------------------------ | ------------------------------------------------------------------------ | ------------------------------ |
| **HOTKEY + START**             | Quitter                                                                  | —                              |
| **HOTKEY + SUD**               | Menu de xbased (sauvegardes instantanées, réglages, redémarrer, quitter) | F1                             |
| **HOTKEY + OUEST**             | Sauvegarde instantanée                                                   | F2 (MAJ + F2 : 2e emplacement) |
| **HOTKEY + NORD**              | Charger la sauvegarde instantanée                                        | F4 (MAJ + F4 : 2e emplacement) |
| **HOTKEY + DROITE** (maintenu) | Avance rapide                                                            | L (maintenu)                   |
| **HOTKEY + R3**                | Capture d'écran                                                          | F8                             |
| —                              | Pause                                                                    | P                              |
| —                              | Plein écran                                                              | F ou ALT + ENTRÉE              |

Le bouton GUIDE n'est pas utilisé dans RetroBat : le menu de xbased s'ouvre avec **HOTKEY + SUD**.

#### **cxbx**

| Raccourci          | Action                                                     | Clavier |
| ------------------ | ---------------------------------------------------------- | ------- |
| **HOTKEY + START** | Quitter                                                    | F6      |
| —                  | Afficher l'interface de Cxbx (compteur d'images, réglages) | F1      |
| —                  | Débloquer la limite d'images par seconde                   | F9      |

## Dossiers

| Contenu                                                             | Dossier                                                 |
| ------------------------------------------------------------------- | ------------------------------------------------------- |
| BIOS de xemu                                                        | `bios`                                                  |
| xemu : disque dur de la console (sauvegardes des jeux, snapshots)   | `saves\xbox\xbox_hdd.qcow2`                             |
| xemu : EEPROM (langue et réglages de la console)                    | `saves\xbox\eeprom.bin`                                 |
| xemu : captures d'écran                                             | `screenshots\xemu`                                      |
| xemu : configuration                                                | `emulators\xemu\xemu.toml`                              |
| xbased : disque dur et EEPROM (sauvegardes dans `Partition1\UDATA`) | `saves\xbox\xbased\hdd`                                 |
| xbased : sauvegardes instantanées gérées par RetroBat               | `saves\xbox\xbased\sstates`                             |
| xbased : sauvegardes instantanées de l'émulateur                    | `emulators\xbased\states`                               |
| xbased : cache des shaders                                          | `saves\xbox\xbased\hle`                                 |
| xbased : captures d'écran (`.bmp`)                                  | `emulators\xbased\screenshots`                          |
| xbased : patchs (IPS) et codes de triche                            | `emulators\xbased\mods`, `emulators\xbased\cheats`      |
| xbased : configuration (générale, par jeu)                          | `emulators\xbased\xbased.ini`, `emulators\xbased\games` |
| cxbx : disque dur émulé (sauvegardes dans `Partition1\UDATA`)       | `emulators\cxbx-reloaded\EmuDisk`                       |
| cxbx : EEPROM                                                       | `emulators\cxbx-reloaded\EEPROM.bin`                    |
| cxbx : configuration                                                | `emulators\cxbx-reloaded\settings.ini`                  |

Les sauvegardes des jeux sont dans le disque dur de chaque émulateur : elles ne passent pas d'un émulateur à l'autre.

## Guides

### Ajouter un jeu

1. Pour xemu et Cxbx, vérifiez que le jeu est au format XISO (voir ci-dessous). xbased lit aussi les images Redump et `.chd`.
2. Copiez le fichier `.iso` dans `roms\xbox`.
3. Pour xemu, ajoutez `mcpx_1.0.bin` et `Complex_4627.bin` dans `bios`.
4. Mettez à jour la liste des jeux de RetroBat et lancez le jeu.

### Convertir une image Redump en XISO

Les images « Redump » contiennent tout le disque, y compris une partie vidéo que la Xbox ne lit pas. xbased les lit telles quelles, mais ni xemu ni Cxbx ne les acceptent. Pour les convertir, utilisez [**extract-xiso**](https://github.com/xboxdev/extract-xiso) ou [**xdvdfs**](https://github.com/antangelo/xdvdfs), deux outils gratuits :

* avec extract-xiso : `extract-xiso -r "Nom du jeu.iso"` réécrit l'image au format XISO ;
* avec xdvdfs : `xdvdfs pack "Nom du jeu.iso" "Nom du jeu (xiso).iso"` crée une nouvelle image.

Ces deux outils savent aussi créer une image XISO à partir d'un dossier de jeu extrait, pour le lancer avec xemu.

### Lancer les .iso avec Cxbx

Cxbx ne lit pas directement les images disque : RetroBat les monte comme un lecteur avec l'outil `xbox-iso-vfs`, qui demande **Dokan 2**.

1. Installez Dokan 2 (programme d'installation « DokanSetup » sur la [page des versions du projet dokany](https://github.com/dokan-dev/dokany/releases)).
2. Lancez le jeu depuis RetroBat. Le lecteur est monté pendant la partie puis retiré à la fermeture du jeu.

Si Dokan 2 n'est pas installé, RetroBat ouvre la page de téléchargement de Dokan et le jeu ne démarre pas.

### Snapshots de xemu

xemu peut enregistrer l'état complet de la console (« snapshot »). RetroBat ne les gère pas depuis la liste des jeux : tout se fait dans xemu.

* Pour créer un snapshot : ouvrez le menu rapide (**GUIDE** ou **SELECT + START**) et choisissez **Save Snapshot**.
* Pour en charger un : ouvrez le menu principal (**F1**), onglet **Snapshots**. Vous pouvez aussi associer un snapshot aux touches F5 à F8 pour le charger au clavier.

Les snapshots sont enregistrés dans le disque dur `saves\xbox\xbox_hdd.qcow2`.

### Sauvegardes instantanées de xbased

Les sauvegardes instantanées de xbased sont gérées par RetroBat :

* en jeu, **HOTKEY + OUEST** crée une sauvegarde. RetroBat la copie aussitôt dans `saves\xbox\xbased\sstates`, avec une image, comme nouvel emplacement ;
* depuis la liste des jeux, le menu des sauvegardes instantanées affiche ces sauvegardes : le jeu démarre directement à l'endroit choisi ;
* **HOTKEY + NORD** recharge la dernière sauvegarde faite avec **HOTKEY + OUEST**.

Le menu de xbased (**HOTKEY + SUD**) propose aussi 10 emplacements : les sauvegardes faites depuis ce menu sont copiées de la même façon.

Une sauvegarde de xbased a besoin du dossier `blobs` placé à côté d'elle (il contient les disques cache du jeu) : ne le supprimez pas.

### Patchs et codes de triche de xbased

xbased intègre des patchs par jeu (60 ips, écran large, 480p…) et les codes de triche de plus de 500 jeux. Ils s'activent jeu par jeu dans l'interface de xbased :

1. Lancez xbased depuis le menu RetroBat : sa bibliothèque affiche les jeux de `roms\xbox` (après un premier lancement d'un jeu depuis RetroBat).
2. Choisissez le jeu, puis **Mods et correctifs**.
3. Activez les patchs ou codes voulus. Ils sont gardés pour les parties lancées depuis RetroBat.

Vous pouvez ajouter vos propres patchs IPS dans `emulators\xbased\mods\<TITLE ID>` et vos codes de triche dans `emulators\xbased\cheats\<TITLE ID>`.

L'option **FRÉQUENCE D'IMAGES** lève la limite d'images par seconde pour tous les jeux ; un patch 60 ips est plus sûr quand il existe pour le jeu.

### Utiliser votre propre disque dur

Le disque dur créé par RetroBat est vide et n'a pas de tableau de bord. Pour utiliser le disque dur d'une console (avec son tableau de bord et ses sauvegardes) ou une image préparée pour xemu, remplacez `saves\xbox\xbox_hdd.qcow2` par votre image, sous le même nom. Gardez une copie de l'ancien fichier : il contient vos sauvegardes.

### Autres options utiles

#### **xemu**

| Option                                         | Effet                                                                                                                       |
| ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **RÉSOLUTION INTERNE**                         | Augmente la résolution de rendu (jusqu'à 10X). La résolution native est 640x480.                                            |
| **RAPPORT D'ASPECT**                           | **NATIF**, **4:3** ou **16:9**. Par défaut, xemu choisit automatiquement.                                                   |
| **ÉMULATION > MÉMOIRE**                        | 128 Mo (par défaut dans RetroBat, comme les kits de développement) ou 64 Mo (console d'origine).                            |
| **ÉMULATION > PASSER L'ANIMATION**             | Activé par défaut : passe l'animation de démarrage de la Xbox.                                                              |
| **VIDÉO > MODE D'AFFICHAGE**                   | Placement de l'image : mise à l'échelle (par défaut), centrée ou étirée.                                                    |
| **VIDÉO > SIGNAL VIDÉO ÉMULÉ**                 | Câble vidéo émulé : HDTV (par défaut), SCART, VGA, RFU, S-VIDEO ou COMPOSITE.                                               |
| **RENDU VISUEL > METTRE EN CACHE LES SHADERS** | Activé par défaut : moins de saccades une fois les shaders enregistrés.                                                     |
| **AUDIO > ÉMULATION DSP**                      | Son plus fidèle (effets, réverbération), mais plus gourmand. **MOTEUR JIT DU DSP** accélère cette émulation (expérimental). |
| **PILOTES > VIDÉO**                            | OPENGL (par défaut) ou VULKAN.                                                                                              |
| **INTERFACE UTILISATEUR > AFFICHER LE MENU**   | Affiche la barre de menus de xemu en haut de l'écran.                                                                       |

#### **xbased**

<table><thead><tr><th width="304">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu (jusqu'à 8X). La résolution native est 640x480.</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td><strong>AUTO</strong> (par défaut), <strong>4:3</strong>, <strong>16:9</strong> ou <strong>ETIRÉ</strong>. Les bezels ne s'affichent qu'en AUTO ou 4:3, sans ÉCRAN LARGE.</td></tr><tr><td><strong>FRÉQUENCE D'IMAGES</strong></td><td><strong>ORIGINAL</strong> (par défaut), <strong>JUSQU'À 60 IPS</strong>, <strong>JUSQU'À 120 IPS</strong> ou <strong>ILLIMITÉ</strong>, quand le jeu le permet. Tout autre réglage qu'original peut casser un jeu.</td></tr><tr><td><strong>ÉMULATION > MÉMOIRE</strong></td><td>64 Mo (par défaut, console d'origine) ou 128 Mo (kits de développement, pour les versions de développement).</td></tr><tr><td><strong>ÉMULATION > LECTURE RAPIDE DU DISQUE</strong></td><td>Chargements plus rapides. Certains jeux peuvent ne pas le supporter.</td></tr><tr><td><strong>VIDÉO > ÉCRAN LARGE</strong></td><td>Règle la console en écran large (16:9), pour les jeux qui le gèrent.</td></tr><tr><td><strong>VIDÉO > MODES VIDÉO HD</strong></td><td>Modes proposés aux jeux : 480P (par défaut), 480P + 720P ou 480P + 720P + 1080I. Les modes HD demandent le signal <strong>HDTV</strong>.</td></tr><tr><td><strong>VIDÉO > SIGNAL VIDÉO ÉMULÉ</strong></td><td>Câble vidéo émulé : HDTV (par défaut), COMPOSITE, S-VIDEO, SCART ou VGA.</td></tr><tr><td><strong>VIDÉO > FRÉQUENCE DES JEUX PAL</strong></td><td>60 Hz (par défaut) ou 50 Hz.</td></tr><tr><td><strong>RENDU VISUEL > FILTRE DE MISE À L'ÉCHELLE</strong></td><td>BILINÉAIRE (par défaut), AMD FSR 1 ou AU PLUS PROCHE.</td></tr><tr><td><strong>RENDU VISUEL > FILTRE CRT</strong></td><td>Scanlines douces, téléviseur classique ou moniteur d'arcade.</td></tr><tr><td><strong>RENDU VISUEL > SURBALAYAGE</strong></td><td>Masque les bords de l'image comme un téléviseur, ou ajoute une bordure (valeurs négatives).</td></tr><tr><td><strong>RENDU VISUEL > SHADERS ASYNCHRONES</strong></td><td>Moins de saccades, mais des objets peuvent manquer un instant.</td></tr><tr><td><strong>AUDIO > NOMBRE DE CANAUX AUDIO</strong></td><td>STÉRÉO (par défaut) ou SURROUND 5.1.</td></tr></tbody></table>

#### **cxbx**

| Option                                           | Effet                                                                            |
| ------------------------------------------------ | -------------------------------------------------------------------------------- |
| **RÉSOLUTION INTERNE**                           | Augmente la résolution de rendu (jusqu'à 12X).                                   |
| **RAPPORT D'ASPECT**                             | **MAINTENIR LE RATIO D'AFFICHAGE** (par défaut) ou **ÉTIRÉ**.                    |
| **VIDÉO > STANDARD VIDÉO**                       | NTSC-M, NTSC-J ou PAL, écrit dans l'EEPROM.                                      |
| **ÉMULATION > NE PAS VÉRIFIER LA SIGNATURE XBE** | À activer pour les homebrews.                                                    |
| **ÉMULATION > DÉSACTIVER LES SHADERS DE PIXEL**  | Peut éviter le plantage de certains jeux. À n'activer que si le jeu en a besoin. |
| **ÉMULATION > UTILISER TOUS LES COEURS**         | Peut améliorer les performances, mais peut faire planter certains jeux.          |

## Problèmes connus

<table><thead><tr><th width="325.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>xemu reste sur un écran d'erreur de la Xbox au lieu de lancer le jeu</td><td>L'image n'est pas au format XISO : convertissez-la (voir <a href="xbox.md#convertir-une-image-redump-en-xiso">Guides</a>) ou lancez le jeu avec xbased. Les <code>.xbe</code> ne se lancent qu'avec xbased (<code>default.xbe</code>) et Cxbx.</td></tr><tr><td>xemu s'arrête au lancement</td><td>Vérifiez la présence de <code>mcpx_1.0.bin</code> et de <code>Complex_4627.bin</code> (ou du BIOS choisi dans FORCER LE FIRMWARE) dans <code>bios</code>.</td></tr><tr><td>xbased affiche une erreur au lancement ou reste sur un écran noir</td><td>xbased demande une carte graphique compatible Vulkan 1.1 (1.3 conseillé) avec des pilotes à jour. Sinon, utilisez xemu ou Cxbx.</td></tr><tr><td>Un réglage changé dans le menu de xbased n'est pas gardé</td><td>RetroBat applique ses options à chaque lancement : changez le réglage dans les options du système Xbox de RetroBat. Les patchs, codes de triche et touches réglés pour un jeu dans xbased sont conservés.</td></tr><tr><td>Cxbx ouvre la page de Dokan et le jeu ne démarre pas</td><td>Dokan 2 n'est pas installé : il est nécessaire pour les <code>.iso</code> (voir <a href="xbox.md#lancer-les-.iso-avec-cxbx">Guides</a>).</td></tr><tr><td>Le jeu n'est pas dans la bonne langue</td><td>Choisissez la langue avec <strong>ÉMULATION > LANGUE</strong>. Certains jeux n'existent qu'en anglais ou dans les langues de leur région.</td></tr><tr><td>Saccades au début d'une partie avec xemu</td><td>Les shaders sont compilés au premier passage : laissez <strong>METTRE EN CACHE LES SHADERS</strong> activé, les parties suivantes seront plus fluides.</td></tr><tr><td>Bugs graphiques ou plantage avec xemu</td><td>Changez de pilote vidéo (<strong>PILOTES > VIDÉO</strong>), puis essayez le jeu avec xbased ou Cxbx.</td></tr><tr><td>Les sauvegardes faites avec un émulateur n'apparaissent pas dans un autre</td><td>Chaque émulateur a son propre disque dur : les sauvegardes ne sont pas partagées. L'import des sauvegardes de xemu proposé par xbased ne cherche xemu que dans <code>AppData</code> : il ne trouve pas le xemu de RetroBat.</td></tr><tr><td>Les réglages des manettes faits dans l'émulateur sont perdus</td><td>RetroBat refait la configuration à chaque lancement : désactivez <strong>AUTOCONFIGURER LES MANETTES</strong> pour garder la vôtre.</td></tr></tbody></table>

La Sega **Chihiro**, une carte d'arcade basée sur la Xbox, a sa propre page : voir la page [**Sega Chihiro**](../../arcade/sega/sega-chihiro.md).
