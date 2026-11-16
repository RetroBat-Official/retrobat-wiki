---
description: Sega
---

# Sega Hikaru

<div align="left"><figure><img src="../../../../.gitbook/assets/image (614).png" alt="" width="300"><figcaption></figcaption></figure></div>

## Présentation

Le **Sega Hikaru** est une carte d'arcade sortie en 1999. Dérivée de la Naomi, elle ajoute un processeur graphique conçu par Sega, capable d'effets de lumière très en avance pour l'époque (éclairage par pixel, reflets). Trop chère à produire, elle est vite remplacée par la Naomi 2 : seuls six jeux sortent sur ce système.

La ludothèque : **Brave Firefighters**, **Air Trix**, **NASCAR Arcade**, **Planet Harriers**, **Star Wars Racer Arcade** et **Cyber Troopers Virtual-On Force**.

RetroBat propose deux émulateurs : **Odin** (par défaut), un émulateur dédié au Hikaru, et **Demul**.

{% embed url="https://fr.wikipedia.org/wiki/Hikaru_(syst%C3%A8me_d'arcade)" %}

## En bref

<table><thead><tr><th width="272.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\hikaru</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>odin</td></tr><tr><td><strong>BIOS</strong></td><td><code>hikaru.zip</code> et <code>mie.zip</code> dans <code>bios</code></td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Odin ; Demul par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>Odin (Brave Firefighters)</td></tr><tr><td><strong>Volants</strong></td><td>Odin (NASCAR Arcade)</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>jvs13551.zip</code>, <code>18wheelr.zip</code>, <code>srally2.zip</code> (Odin)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="143.25">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>odin</strong> (défaut)</td><td>Émulateur bas niveau dédié au Hikaru : les six jeux, résolution augmentée, filtre CRT, sauvegardes instantanées, pistolets (Brave Firefighters), volant à retour de force (NASCAR Arcade), vibrations de la manette.</td><td>Émulateur récent (version 0.1).</td></tr><tr><td><strong>demul</strong></td><td>Émulateur historique, aussi utilisé pour la Naomi et l'Atomiswave.</td><td>Compatibilité plus faible. Sauvegardes instantanées non gérées par RetroBat.</td></tr></tbody></table>

## BIOS

Les jeux ont besoin de deux archives au format MAME, communes à tous les jeux du système :

<table><thead><tr><th width="148.25">Fichier</th><th>Dossier</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>hikaru.zip</code></td><td><code>bios</code> (ou <code>roms\hikaru</code>)</td><td>Odin, Demul</td></tr><tr><td><code>mie.zip</code></td><td><code>bios</code> (ou <code>roms\hikaru</code>)</td><td>Odin, Demul</td></tr></tbody></table>

Les deux émulateurs cherchent ces archives dans `bios`, puis dans le dossier des jeux. Leur contenu dépend de la version de MAME : il n'y a pas de MD5 de référence pour les archives.

Odin peut aussi utiliser les sets `jvs13551.zip`, `18wheelr.zip` et `srally2.zip`, facultatifs.

Si un fichier manque, Odin affiche son nom et celui de l'archive qui le contient (par exemple « missing files : 93c46.ic115 (hikaru.zip) »).

## Quel format de jeu ?

Les jeux sont des archives `.zip` au format MAME, à garder sans les décompresser et sans les renommer (`airtrix.zip`, `braveff.zip`, `pharrier.zip`, `sgnascar.zip`, `swracer.zip`, `von4.zip`).

Les versions d'origine `airtrixo` et `sgnascaro` ont besoin de leur jeu parent (`airtrix`, `sgnascar`) dans le même dossier, sauf avec un [romset non-merged](../../../arcade-guide.md#types-de-romsets).

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour les deux émulateurs. L'option **AUTOCONFIGURER LES MANETTES** permet de garder sa propre configuration.

Pour tous les jeux : **START** = Start, **SELECT** = pièce, **L3** = Service, **R3** = Test. Au clavier : 1 / 2 = Start des joueurs 1 / 2, 5 / 6 = pièce, 9 = Service, 0 = Test.

### Odin

Odin reconnaît les manettes et les joysticks. Chaque joueur garde sa manette d'une partie à l'autre, même avec deux manettes identiques. Brave Firefighters se joue à deux sur la même borne ; les autres jeux sont à un joueur (les bornes reliées en réseau ne sont pas émulées).

Les boutons sont réglés par jeu dans `odin.yml` (`system\resources\inputmapping`, copie modifiable dans `user\inputmapping`) :

<table><thead><tr><th width="335.25">Jeu</th><th>Commandes</th></tr></thead><tbody><tr><td>Air Trix (<code>airtrix</code>, <code>airtrixo</code>)</td><td>Stick gauche : tourner ; stick droit : incliner la planche ; croix gauche / droite : gauche / droite ; L1 / R1 : haut / bas</td></tr><tr><td>Brave Firefighters (<code>braveff</code>)</td><td>Stick gauche, pistolet ou souris : viser avec la lance ; R2 : eau ; L2 : brouillard</td></tr><tr><td>Planet Harriers (<code>pharrier</code>)</td><td>Stick gauche : manche ; R2 : tir ; L2 : missile ; SUD : bombe ; L1 / R1 : boutons VR gauche / droit</td></tr><tr><td>Star Wars Racer Arcade (<code>swracer</code>)</td><td>Stick gauche (haut / bas) : manette gauche ; stick droit (haut / bas) : manette droite ; SUD : boost ; R2 : frein ; croix gauche / droite : boutons gauche / droit</td></tr><tr><td>NASCAR Arcade (<code>sgnascar</code>, <code>sgnascaro</code>)</td><td>Stick gauche : direction ; R2 / L2 : accélérer / freiner ; R1 / L1 : rapport supérieur / inférieur ; NORD : vue</td></tr><tr><td>Cyber Troopers Virtual-On Force (<code>von4</code>)</td><td>Stick gauche : manche gauche ; stick droit : manche droit ; L2 / R2 : gâchettes gauche / droite ; L1 / R1 : turbo gauche / droit ; NORD : bouton PIB</td></tr></tbody></table>

Options du menu **CONTRÔLES** :

* **ZONE MORTE JOYSTICK** : zone morte des sticks (3 % par défaut).
* **INVERSER L'AXE Y** : dans Planet Harriers, la borne monte quand on tire le manche vers soi ; l'option fait monter en poussant le stick vers le haut.
* **ACTIVER LES VIBRATIONS** : la manette vibre comme la borne (activé par défaut).
* **SORTIES EXTERNES** : envoie les lampes, les vibrations de la lance et la carte de retour de force à des outils externes (Hook Of The Reaper, QMamehook…).

### Demul

Demul utilise la même disposition pour tous les jeux :

<table><thead><tr><th width="286.5">Bouton de la borne</th><th>Manette</th></tr></thead><tbody><tr><td>Boutons 1 à 4</td><td>SUD, EST, OUEST, NORD</td></tr><tr><td>Boutons 5 à 8</td><td>L1, R1, L2, R2</td></tr><tr><td>Commandes analogiques</td><td>Stick gauche et stick droit</td></tr><tr><td>Direction</td><td>Croix directionnelle</td></tr></tbody></table>

L'option **CONTRÔLES > ZONE MORTE ANALOGIQUE** règle la zone morte des sticks.

### Pistolets

Brave Firefighters se joue au pistolet avec Odin, jusqu'à deux joueurs. Activez **PISTOLETS > ACTIVER LES PISTOLETS**.

* Clic gauche (gâchette) : eau ; clic droit : brouillard ; clic du milieu : Start.
* Sans pistolet, la souris vise pour le joueur 1 (et le stick gauche de la manette).
* Avec une DolphinBar, les boutons de la Wiimote servent de pièce et de Start (premier pistolet : gauche / droite, second pistolet : bas / haut).
* **UN SEUL PISTOLET** ne configure qu'un pistolet, **INVERSER GÂCHETTE ET RECHARGE** échange l'eau et le brouillard, **TAILLE DE LA BORDURE SINDEN** élargit la bordure blanche des pistolets Sinden.

Pour plus de détails sur les pistolets, voir la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/).

### Volants

NASCAR Arcade se joue au volant avec Odin, avec retour de force. Activez **VOLANTS DE COURSE > ACTIVER LES VOLANTS** : le volant devient le joueur 1.

* **ROTATION DU VOLANT** : angle de rotation pour braquer à fond (270° par défaut, comme la borne).
* **FORCE DU RETOUR DE FORCE** : de 50 à 200 %, ou désactivé.
* Les boutons sont réglés par type de volant dans `model3_wheels.yml` (le même fichier que Supermodel). Odin lit d'abord `odin_wheels.yml` s'il existe.

Pour plus de détails sur les volants, voir la page [**Volants**](../../../../controleurs/supported-controllers/volants.md).

### Raccourcis

#### **Odin**

| Raccourci          | Action                                  | Clavier             |
| ------------------ | --------------------------------------- | ------------------- |
| **HOTKEY + START** | Quitter                                 | Échap               |
| **HOTKEY + SUD**   | Menu d'Odin                             | F10                 |
| **HOTKEY + OUEST** | Sauvegarde instantanée                  | F2                  |
| **HOTKEY + NORD**  | Chargement de la sauvegarde instantanée | F4                  |
| **L3** / **R3**    | Service / Test                          | 9 / 0               |
| —                  | Pause                                   | P                   |
| —                  | Réinitialiser                           | Ctrl + R            |
| —                  | Plein écran                             | F11 ou Alt + Entrée |
| —                  | Carte (Virtual-On Force)                | F6                  |
| —                  | Afficher / masquer le curseur           | F7                  |

Les raccourcis d'Odin restent aussi disponibles à la manette avec le bouton **Guide** : Guide seul = menu, Guide + SELECT = pause, Guide + R1 / L1 = sauvegarde / chargement, Guide + START = quitter.

Les touches du clavier sont personnalisables, voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

#### **Demul**

<table><thead><tr><th width="207">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td></td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée de Demul</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement instantané de Demul</td><td>F4</td></tr><tr><td><strong>HOTKEY + L3</strong></td><td>Plein écran</td><td>Alt + Entrée</td></tr></tbody></table>

Les sauvegardes instantanées de Demul restent dans Demul : elles n'apparaissent pas dans le gestionnaire de sauvegardes.

## Dossiers

<table><thead><tr><th width="362.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS</td><td><code>bios</code> (<code>hikaru.zip</code>, <code>mie.zip</code>)</td></tr><tr><td>Odin : NVRAM (réglages et records des bornes)</td><td><code>saves\hikaru\odin</code></td></tr><tr><td>Odin : sauvegardes instantanées (gérées par RetroBat)</td><td><code>saves\hikaru\odin\sstates</code></td></tr><tr><td>Odin : sauvegardes instantanées (dossier de l'émulateur, une par jeu)</td><td><code>saves\hikaru\odin\states</code></td></tr><tr><td>Odin : configuration</td><td><code>emulators\odin\odin.ini</code></td></tr><tr><td>Odin : journal (erreurs au lancement)</td><td><code>emulators\odin\odin.log</code></td></tr><tr><td>Odin : correspondance des boutons</td><td><code>system\resources\inputmapping\odin.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr><tr><td>Odin : boutons des volants</td><td><code>system\resources\inputmapping\wheels\model3_wheels.yml</code> (ou <code>user\inputmapping\odin_wheels.yml</code>)</td></tr><tr><td>Demul : NVRAM</td><td><code>saves\hikaru\demul</code></td></tr><tr><td>Demul : configuration</td><td><code>emulators\demul\Demul.ini</code>, <code>padDemul.ini</code></td></tr></tbody></table>

## Guides

### Menu Service

Le menu de test de chaque borne donne accès aux réglages du jeu (difficulté, nombre de crédits, calibration…). **R3** (ou **0** au clavier) ouvre le menu de test, **L3** (ou **9**) s'y déplace.

### Sauvegardes instantanées (Odin)

Odin garde une seule sauvegarde par jeu, remplacée à chaque **HOTKEY + OUEST**. RetroBat copie chaque nouvelle sauvegarde dans un nouvel emplacement : vous les retrouvez toutes dans le gestionnaire de sauvegardes et pouvez lancer le jeu depuis l'une d'elles. Odin n'enregistre pas de capture d'écran : le gestionnaire affiche l'icône de sauvegarde de RetroBat.

### Décorations

Par défaut, Odin affiche les décorations de RetroBat. L'option **UTILISER LES BEZELS DE L'ÉMULATEUR** affiche à la place les bezels du pack Odin-Artwork, à extraire dans `emulators\odin`.

### Autres options utiles (Odin)

| Option                                             | Effet                                                                                                    |
| -------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **RÉSOLUTION INTERNE**                             | Augmente la résolution de rendu (jusqu'à 6x).                                                            |
| **SYNCHRONISATION VERTICALE**                      | Désactivée par défaut ; **ADAPTATIF** n'attend pas l'écran quand une image est en retard.                |
| **RENDU VISUEL > FILTRE CRT**                      | Aspect d'un moniteur Sega (29 pouces) ou d'un projecteur Sega (50 pouces).                               |
| **RENDU VISUEL > FILTRAGE ANISOTROPE**             | Améliore les textures vues de biais.                                                                     |
| **RENDU VISUEL > MISE À L'ÉCHELLE DES COUCHES 2D** | Filtre des éléments 2D (interface, décors) quand la résolution est augmentée.                            |
| **AUDIO > CARTES SON**                             | Planet Harriers, NASCAR Arcade, Star Wars Racer Arcade : carte son principale seule, mixage ou 4 canaux. |
| **PILOTES > VIDÉO**                                | OpenGL (défaut) ou Vulkan.                                                                               |

#### **Demul**&#x20;

**RÉSOLUTION INTERNE**, **RAPPORT D'ASPECT** (4:3, 16:9 ou étiré), **ÉMULATION > MODE D'ÉXECUTION CPU**.

## Problèmes connus

<table><thead><tr><th width="344">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Odin affiche « missing files » au lancement</td><td>Le message donne le fichier et l'archive qui manquent : ajoutez <code>hikaru.zip</code> / <code>mie.zip</code> dans <code>bios</code>, ou mettez à jour le romset du jeu.</td></tr><tr><td><code>airtrixo</code> ou <code>sgnascaro</code> ne démarre pas</td><td>Placez le jeu parent (<code>airtrix</code>, <code>sgnascar</code>) dans <code>roms\hikaru</code>, ou utilisez un <a href="../../../arcade-guide.md#types-de-romsets">romset non-merged</a>.</td></tr><tr><td>Planet Harriers : le stick est inversé</td><td>Activez <strong>CONTRÔLES > INVERSER L'AXE Y</strong>.</td></tr><tr><td>Odin ne s'affiche pas sur le bon écran</td><td>Activez <strong>VIDÉO > DÉSACTIVER PLEIN ÉCRAN</strong>.</td></tr></tbody></table>
