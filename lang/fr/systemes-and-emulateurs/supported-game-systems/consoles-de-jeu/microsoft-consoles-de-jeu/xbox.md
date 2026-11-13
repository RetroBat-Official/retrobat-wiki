---
description: Microsoft
---

# Xbox

<div align="left"><figure><img src="../../../../.gitbook/assets/image (582).png" alt="" width="425"><figcaption></figcaption></figure></div>

{% embed url="https://fr.wikipedia.org/wiki/Xbox" %}

## Présentation

La **Xbox** est la première console de salon de Microsoft. Elle sort en novembre 2001 aux États-Unis, puis en février 2002 au Japon et en mars 2002 en Europe. Elle est construite comme un PC : un processeur Intel Pentium III à 733 MHz, une puce graphique NVIDIA (NV2A), 64 Mo de mémoire et, pour la première fois sur une console, un disque dur intégré de 8 Go qui garde les sauvegardes et les musiques copiées depuis des CD.

Sa grosse manette d'origine, surnommée « Duke », est vite remplacée par la **Controller S**, plus compacte. En 2002, le service **Xbox Live** ouvre le jeu en ligne sur console grâce au port Ethernet de la machine. La Xbox s'est vendue à environ 24 millions d'exemplaires avant d'être remplacée par la Xbox 360 fin 2005. Parmi ses jeux marquants : Halo: Combat Evolved, Halo 2, Fable, Star Wars: Knights of the Old Republic, Ninja Gaiden, Jet Set Radio Future ou Project Gotham Racing.

RetroBat propose deux émulateurs : **xemu**, qui reproduit le matériel de la console et utilise son BIOS, et **Cxbx-Reloaded**, qui remplace le système de la Xbox par son propre code et n'a pas besoin de BIOS.

## En bref

<table><thead><tr><th width="285.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\xbox</code></td></tr><tr><td><strong>Extensions</strong></td><td>.xbe .iso .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>xemu</td></tr><tr><td><strong>BIOS</strong></td><td><code>mcpx_1.0.bin</code> et <code>Complex_4627.bin</code> (xemu uniquement)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (xemu : snapshots depuis son menu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>cxbx</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>Cerbios.bin</code>, <code>Complex_4627v1.03.bin</code> (xemu, option FORCER LE FIRMWARE)</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                | Points forts                                                                                                                         | Limites                                                                                             |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| **xemu** (défaut)        | Le plus compatible. Émule le vrai matériel : disque dur, EEPROM, tableau de bord. Résolution augmentée, Vulkan ou OpenGL, snapshots. | Demande le BIOS. Ne lit que les images disque au format XISO (`.iso`). Pas de pistolets.            |
| **cxbx** (Cxbx-Reloaded) | Pas de BIOS. Lance les jeux extraits (`.xbe`, dossiers `.decomp`). Gère le pistolet EMS TopGun.                                      | Compatibilité plus faible, plus de bugs graphiques. Les `.iso` demandent l'installation de Dokan 2. |

La liste de compatibilité de xemu ([xemu.app](https://xemu.app/#compatibility)) indique l'état de chaque jeu. En cas de problème avec un jeu, essayez l'autre émulateur.

## BIOS

Seul **xemu** a besoin du BIOS. Cxbx-Reloaded n'en utilise aucun.

<table><thead><tr><th width="211.75">Fichier</th><th width="89">Dossier</th><th>Rôle</th><th>MD5</th></tr></thead><tbody><tr><td><code>mcpx_1.0.bin</code></td><td><code>bios</code></td><td>ROM de démarrage (MCPX), obligatoire</td><td>d49c52a4102f6df7bcf8d0617ac475ed</td></tr><tr><td><code>Complex_4627.bin</code></td><td><code>bios</code></td><td>BIOS (flash) utilisé par défaut</td><td>39cee882148a87f93cb440b99dde3ceb</td></tr><tr><td><code>Cerbios.bin</code></td><td><code>bios</code></td><td>BIOS alternatif, facultatif</td><td></td></tr><tr><td><code>Complex_4627v1.03.bin</code></td><td><code>bios</code></td><td>BIOS alternatif, facultatif</td><td></td></tr></tbody></table>

RetroBat contrôle `mcpx_1.0.bin` et `Complex_4627.bin`. Les BIOS alternatifs ne servent que si vous les choisissez avec l'option **ÉMULATION > FORCER LE FIRMWARE** de xemu.

Le disque dur et l'EEPROM de la console ne sont pas des BIOS à ajouter : au premier lancement, RetroBat crée `xbox_hdd.qcow2` (un disque dur formaté, sans tableau de bord) et `eeprom.bin` dans `saves\xbox`.

Pour plus de détails sur l'installation et la vérification des BIOS, voir la page **Ajouter les BIOS**.

### Langue de la console

La langue des jeux est celle de l'EEPROM de la console. RetroBat l'écrit à chaque lancement, pour les deux émulateurs :

* par défaut, c'est la langue de RetroBat (anglais si elle n'existe pas sur Xbox) ;
* l'option **ÉMULATION > LANGUE** force une langue : anglais, japonais, allemand, français, espagnol, italien, coréen, chinois ou portugais.

Un jeu qui n'existe pas dans la langue choisie s'affiche dans sa langue par défaut, souvent l'anglais.

## Quel format de jeu ?

<table><thead><tr><th width="166.25">Format</th><th width="95.25">xemu</th><th width="78">cxbx</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.iso</strong> (XISO)</td><td>✅</td><td>✅</td><td>Image disque au format Xbox (XISO). Avec Cxbx, l'image est montée comme un lecteur grâce à Dokan 2 (voir <a href="xbox.md#convertir-une-image-redump-en-xiso">Guides</a>).</td></tr><tr><td><strong>.iso</strong> (Redump)</td><td>❌</td><td>❌</td><td>Image complète du disque, avec la partie vidéo : à convertir en XISO (voir <a href="xbox.md#lancer-les-.iso-avec-cxbx">Guides</a>).</td></tr><tr><td><strong>.xbe</strong></td><td>❌</td><td>✅</td><td>Exécutable d'un jeu extrait (souvent <code>default.xbe</code>).</td></tr><tr><td><strong>Dossier <code>.decomp</code></strong></td><td>❌</td><td>✅</td><td>Dossier d'un jeu extrait, renommé avec <code>.decomp</code> à la fin. Cxbx lance le <code>default.xbe</code> qu'il contient.</td></tr></tbody></table>

Les archives `.zip` et `.7z` ne sont pas acceptées : les jeux Xbox doivent rester décompressés.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour les deux émulateurs, jusqu'à 4 joueurs, dans l'ordre des joueurs de RetroBat. L'option **AUTOCONFIGURER LES MANETTES** permet de désactiver cette configuration pour garder celle faite dans l'émulateur.

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
* **Cxbx** émule par défaut une **Controller S**. L'option **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** (à 4) choisit **MANETTE S** ou **MANETTE DUKE**. Les vibrations s'activent avec **CONTRÔLES > ACTIVER LES VIBRATIONS**.

### Clavier

Un clavier attribué à un joueur dans RetroBat est configuré avec ces touches :

| Xbox                                     | xemu                   | cxbx           |
| ---------------------------------------- | ---------------------- | -------------- |
| A, B, X, Y                               | A, B, X, Y             | S, D, W, E     |
| Blanc, Noir                              | 1, 2                   | X, C           |
| Gâchettes gauche, droite                 | W, O                   | Q, R           |
| Back, Start                              | RETOUR ARRIÈRE, ENTRÉE | ESPACE, ENTRÉE |
| Croix directionnelle                     | Flèches                | Flèches        |
| Stick gauche (haut, gauche, bas, droite) | E, S, D, F             | T, F, G, H     |
| Stick droit (haut, gauche, bas, droite)  | I, J, K, L             | I, J, K, L     |
| Clics des sticks                         | 3, 4                   | B, M           |

Les touches sont données pour un clavier QWERTY : les deux émulateurs utilisent la position des touches, pas leur lettre.

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

**xemu**

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

> 📷 **Capture à ajouter** : menu rapide de xemu ouvert en jeu.

**cxbx**

| Raccourci          | Action                                                     | Clavier |
| ------------------ | ---------------------------------------------------------- | ------- |
| **HOTKEY + START** | Quitter                                                    | F6      |
| —                  | Afficher l'interface de Cxbx (compteur d'images, réglages) | F1      |
| —                  | Débloquer la limite d'images par seconde                   | F9      |

## Dossiers

| Contenu                                                           | Dossier                                |
| ----------------------------------------------------------------- | -------------------------------------- |
| BIOS de xemu                                                      | `bios`                                 |
| xemu : disque dur de la console (sauvegardes des jeux, snapshots) | `saves\xbox\xbox_hdd.qcow2`            |
| xemu : EEPROM (langue et réglages de la console)                  | `saves\xbox\eeprom.bin`                |
| xemu : captures d'écran                                           | `screenshots\xemu`                     |
| xemu : configuration                                              | `emulators\xemu\xemu.toml`             |
| cxbx : disque dur émulé (sauvegardes dans `Partition1\UDATA`)     | `emulators\cxbx-reloaded\EmuDisk`      |
| cxbx : EEPROM                                                     | `emulators\cxbx-reloaded\EEPROM.bin`   |
| cxbx : configuration                                              | `emulators\cxbx-reloaded\settings.ini` |

Les sauvegardes des jeux sont dans le disque dur de chaque émulateur : elles ne passent pas de xemu à Cxbx, ni dans l'autre sens.

## Guides

### Ajouter un jeu

1. Vérifiez que le jeu est au format XISO (voir ci-dessous).
2. Copiez le fichier `.iso` dans `roms\xbox`.
3. Pour xemu, ajoutez `mcpx_1.0.bin` et `Complex_4627.bin` dans `bios`.
4. Mettez à jour la liste des jeux de RetroBat et lancez le jeu.

### Convertir une image Redump en XISO

Les images « Redump » contiennent tout le disque, y compris une partie vidéo que la Xbox ne lit pas. Ni xemu ni Cxbx ne les acceptent. Pour les convertir, utilisez [**extract-xiso**](https://github.com/xboxdev/extract-xiso) ou [**xdvdfs**](https://github.com/antangelo/xdvdfs), deux outils gratuits :

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

### Utiliser votre propre disque dur

Le disque dur créé par RetroBat est vide et n'a pas de tableau de bord. Pour utiliser le disque dur d'une console (avec son tableau de bord et ses sauvegardes) ou une image préparée pour xemu, remplacez `saves\xbox\xbox_hdd.qcow2` par votre image, sous le même nom. Gardez une copie de l'ancien fichier : il contient vos sauvegardes.

### Autres options utiles

**xemu**

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

**cxbx**

| Option                                           | Effet                                                                            |
| ------------------------------------------------ | -------------------------------------------------------------------------------- |
| **RÉSOLUTION INTERNE**                           | Augmente la résolution de rendu (jusqu'à 12X).                                   |
| **RAPPORT D'ASPECT**                             | **MAINTENIR LE RATIO D'AFFICHAGE** (par défaut) ou **ÉTIRÉ**.                    |
| **VIDÉO > STANDARD VIDÉO**                       | NTSC-M, NTSC-J ou PAL, écrit dans l'EEPROM.                                      |
| **ÉMULATION > NE PAS VÉRIFIER LA SIGNATURE XBE** | À activer pour les homebrews.                                                    |
| **ÉMULATION > DÉSACTIVER LES SHADERS DE PIXEL**  | Peut éviter le plantage de certains jeux. À n'activer que si le jeu en a besoin. |
| **ÉMULATION > UTILISER TOUS LES COEURS**         | Peut améliorer les performances, mais peut faire planter certains jeux.          |

> 📷 **Capture à ajouter** : options du système Xbox dans RetroBat.

## Problèmes connus

| Problème                                                             | Solution                                                                                                                                                                         |
| -------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| xemu reste sur un écran d'erreur de la Xbox au lieu de lancer le jeu | L'image n'est pas au format XISO : convertissez-la (voir [Guides](xbox.md#convertir-une-image-redump-en-xiso)). Les `.xbe` et les dossiers `.decomp` ne se lancent qu'avec Cxbx. |
| xemu s'arrête au lancement                                           | Vérifiez la présence de `mcpx_1.0.bin` et de `Complex_4627.bin` (ou du BIOS choisi dans FORCER LE FIRMWARE) dans `bios`.                                                         |
| Cxbx ouvre la page de Dokan et le jeu ne démarre pas                 | Dokan 2 n'est pas installé : il est nécessaire pour les `.iso` (voir [Guides](xbox.md#lancer-les-.iso-avec-cxbx)).                                                               |
| Le jeu n'est pas dans la bonne langue                                | Choisissez la langue avec **ÉMULATION > LANGUE**. Certains jeux n'existent qu'en anglais ou dans les langues de leur région.                                                     |
| Saccades au début d'une partie avec xemu                             | Les shaders sont compilés au premier passage : laissez **METTRE EN CACHE LES SHADERS** activé, les parties suivantes seront plus fluides.                                        |
| Bugs graphiques ou plantage avec xemu                                | Changez de pilote vidéo (**PILOTES > VIDÉO**), puis essayez le jeu avec Cxbx.                                                                                                    |
| Les sauvegardes faites avec xemu n'apparaissent pas dans Cxbx        | Chaque émulateur a son propre disque dur : les sauvegardes ne sont pas partagées.                                                                                                |
| Les réglages des manettes faits dans l'émulateur sont perdus         | RetroBat refait la configuration à chaque lancement : désactivez **AUTOCONFIGURER LES MANETTES** pour garder la vôtre.                                                           |

La Sega **Chihiro**, une carte d'arcade basée sur la Xbox, a sa propre page : voir la page [**Sega Chihiro**](../../arcade/sega/sega-chihiro.md).
