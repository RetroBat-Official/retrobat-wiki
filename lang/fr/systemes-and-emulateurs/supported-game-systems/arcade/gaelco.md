---
description: Gaelco, S.A.
---

# Gaelco

<div align="left"><figure><img src="../../../.gitbook/assets/image (613).png" alt="" width="341"><figcaption></figcaption></figure></div>

## Présentation

**Gaelco** est un développeur espagnol de jeux d'arcade, installé à Barcelone, connu pour Big Karnak, World Rally ou Radikal Bikers. Au début des années 2000, ses jeux en 3D tournent sur des cartes construites autour d'une puce graphique PowerVR (carte Neon 250).

Le système **Gaelco PowerVR** de RetroBat regroupe ces jeux : **Smashing Drive** (2000), **ATV Track** (2002) et **Gaelco Football** (2002).

RetroBat propose deux émulateurs : **Odin** (par défaut), un émulateur bas niveau des cartes Gaelco et Hikaru, et **Demul**.

{% embed url="https://fr.wikipedia.org/wiki/Gaelco" %}

## En bref

<table><thead><tr><th width="286.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\gaelco</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>odin</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Odin ; Demul par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Volants</strong></td><td>Odin (ATV Track, Smashing Drive)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="142">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>odin</strong> (défaut)</td><td>Émulateur bas niveau des cartes Gaelco : les trois jeux, commandes réglées par jeu, résolution augmentée, filtres CRT des moniteurs Gaelco, sauvegardes instantanées, volant à retour de force, vibrations de la manette.</td><td>Prise en charge des jeux Gaelco toute récente (Odin 0.1.1).</td></tr><tr><td><strong>demul</strong></td><td>Émulateur historique, aussi utilisé pour la Naomi et l'Atomiswave.</td><td>Même disposition des boutons pour tous les jeux. Sauvegardes instantanées non gérées par RetroBat.</td></tr></tbody></table>

MAME n'émule pas encore ces jeux (marqués non fonctionnels et sans son).

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Les jeux sont des archives `.zip` au format MAME, à garder sans les décompresser et sans les renommer (`atvtrack.zip`, `gfootbal.zip`, `smashdrv.zip`).

Les versions `atvtracka`, `smashdrvb` et `smashdrvs` ont besoin de leur jeu parent (`atvtrack`, `smashdrv`) dans le même dossier, sauf avec un romset non-merged.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour les deux émulateurs. L'option **AUTOCONFIGURER LES MANETTES** permet de garder sa propre configuration.

Pour tous les jeux : **SELECT** = pièce, **L3** = Service, **R3** = Test. Au clavier : 1 = Start, 5 = pièce, 9 = Service, 0 = Test. Les bornes Gaelco n'ont qu'une entrée de pièce et un bouton Service.

### Odin

Les boutons sont réglés par jeu dans `odin.yml` (`system\resources\inputmapping`, copie modifiable dans `user\inputmapping`) :

<table><thead><tr><th width="322.75">Jeu</th><th>Commandes</th></tr></thead><tbody><tr><td>ATV Track (<code>atvtrack</code>, <code>atvtracka</code>)</td><td>Stick gauche : guidon ; R2 : accélérateur ; L2 / R1 : freins gauche / droit ; START : Start</td></tr><tr><td>Gaelco Football (<code>gfootbal</code>), 2 joueurs</td><td>Croix ou stick gauche : déplacements ; SUD, EST, OUEST : boutons 1, 2, 3 ; stick droit : frapper le ballon (tirez d'abord le stick vers vous pour lever le ballon) ; START : Start</td></tr><tr><td>Smashing Drive (<code>smashdrv</code>, <code>smashdrvb</code>, <code>smashdrvs</code>)</td><td>Stick gauche : direction ; R2 / L2 : accélérer / freiner ; START : klaxon (Start) ; croix haut / bas : volume</td></tr></tbody></table>

Dans Gaelco Football, le stick droit sert à frapper : **R3** n'ouvre pas le menu de test, utilisez la touche **0** du clavier.

Options du menu **CONTRÔLES** :

* **ZONE MORTE JOYSTICK** : zone morte des sticks (3 % par défaut).
* **ACTIVER LES VIBRATIONS** : la manette vibre comme la borne, par exemple le siège vibrant d'ATV Track (activé par défaut).
* **SORTIES EXTERNES** : envoie les lampes et la carte de retour de force à des outils externes (Hook Of The Reaper, QMamehook…).

### Demul

Demul utilise la même disposition pour tous les jeux :

<table><thead><tr><th width="269">Bouton de la borne</th><th>Manette</th></tr></thead><tbody><tr><td>Boutons 1 à 4</td><td>SUD, EST, OUEST, NORD</td></tr><tr><td>Boutons 5 à 8</td><td>L1, R1, L2, R2</td></tr><tr><td>Commandes analogiques</td><td>Stick gauche et stick droit</td></tr><tr><td>Direction</td><td>Croix directionnelle</td></tr><tr><td>Start</td><td>START</td></tr></tbody></table>

L'option **CONTRÔLES > ZONE MORTE ANALOGIQUE** règle la zone morte des sticks.

### Volants

ATV Track et Smashing Drive se jouent au volant avec Odin, avec retour de force. Activez **VOLANTS DE COURSE > ACTIVER LES VOLANTS** : le volant devient le joueur 1.

* ATV Track : le volant sert de guidon ; la pédale de frein et la palette droite actionnent le frein droit, la palette gauche le frein gauche.
* **ROTATION DU VOLANT** : angle de rotation pour braquer à fond (270° par défaut).
* **FORCE DU RETOUR DE FORCE** : de 50 à 200 %, ou désactivé.
* Les boutons sont réglés par type de volant dans `model3_wheels.yml` (le même fichier que Supermodel). Odin lit d'abord `odin_wheels.yml` s'il existe.

Pour plus de détails sur les volants, voir la page [**Volants**](../../../controleurs/supported-controllers/volants.md).

### Raccourcis

#### **Odin**

<table><thead><tr><th width="193.25">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>Échap</td></tr><tr><td><strong>HOTKEY + SUD</strong></td><td>Menu d'Odin</td><td>F10</td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement de la sauvegarde instantanée</td><td>F4</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test</td><td>9 / 0</td></tr><tr><td>—</td><td>Pause</td><td>P</td></tr><tr><td>—</td><td>Réinitialiser</td><td>Ctrl + R</td></tr><tr><td>—</td><td>Plein écran</td><td>F11 ou Alt + Entrée</td></tr></tbody></table>

Les raccourcis d'Odin restent aussi disponibles à la manette avec le bouton **Guide** : Guide seul = menu, Guide + SELECT = pause, Guide + R1 / L1 = sauvegarde / chargement, Guide + START = quitter.

Les touches du clavier sont personnalisables, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

#### **Demul**

<table><thead><tr><th width="190.75">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td></td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée de Demul</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement instantané de Demul</td><td>F4</td></tr><tr><td><strong>HOTKEY + L3</strong></td><td>Plein écran</td><td>Alt + Entrée</td></tr></tbody></table>

Les sauvegardes instantanées de Demul restent dans Demul : elles n'apparaissent pas dans le gestionnaire de sauvegardes.

## Dossiers

<table><thead><tr><th width="300.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Odin : NVRAM (réglages et records des bornes)</td><td><code>saves\gaelco\odin</code></td></tr><tr><td>Odin : sauvegardes instantanées (gérées par RetroBat)</td><td><code>saves\gaelco\odin\sstates</code></td></tr><tr><td>Odin : sauvegardes instantanées (dossier de l'émulateur, une par jeu)</td><td><code>saves\gaelco\odin\states</code></td></tr><tr><td>Odin : configuration</td><td><code>emulators\odin\odin.ini</code></td></tr><tr><td>Odin : journal (erreurs au lancement)</td><td><code>emulators\odin\odin.log</code></td></tr><tr><td>Odin : correspondance des boutons</td><td><code>system\resources\inputmapping\odin.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr><tr><td>Odin : boutons des volants</td><td><code>system\resources\inputmapping\wheels\model3_wheels.yml</code> (ou <code>user\inputmapping\odin_wheels.yml</code>)</td></tr><tr><td>Demul : NVRAM</td><td><code>saves\gaelco\demul</code></td></tr><tr><td>Demul : configuration</td><td><code>emulators\demul\Demul.ini</code>, <code>padDemul.ini</code></td></tr></tbody></table>

## Guides

### Menu Service

Le menu de test de chaque borne donne accès aux réglages du jeu (difficulté, crédits, volume…). **R3** (ou **0** au clavier) ouvre le menu de test, **L3** (ou **9**) s'y déplace.

### Volume de Smashing Drive (Odin)

Smashing Drive règle son volume à chaque mise sous tension (75 par défaut). Changez-le avec la croix haut / bas pendant la partie.

### Sauvegardes instantanées (Odin)

Odin garde une seule sauvegarde par jeu, remplacée à chaque **HOTKEY + OUEST**.

RetroBat copie chaque nouvelle sauvegarde dans un nouvel emplacement : vous les retrouvez toutes dans le gestionnaire de sauvegardes et pouvez lancer le jeu depuis l'une d'elles.

### Autres options utiles (Odin)

<table><thead><tr><th width="302.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu (jusqu'à 6x).</td></tr><tr><td><strong>RENDU VISUEL > FILTRE CRT</strong></td><td>Aspect d'un moniteur Gaelco (28 ou 34 pouces).</td></tr><tr><td><strong>AUDIO > CARTES SON</strong></td><td>Caisson de basses des bornes Gaelco : carte principale seule, mixage ou 4 canaux.</td></tr><tr><td><strong>UTILISER LES BEZELS DE L'ÉMULATEUR</strong></td><td>Bezels du pack Odin-Artwork (à extraire dans <code>emulators\odin</code>) au lieu des décorations RetroBat.</td></tr><tr><td><strong>PILOTES > VIDÉO</strong></td><td>OpenGL (défaut) ou Vulkan.</td></tr></tbody></table>

#### **Demul**

**RÉSOLUTION INTERNE**, **RAPPORT D'ASPECT** (4:3, 16:9 ou étiré). Demul utilise toujours son ancien plugin graphique pour ces jeux.

## Problèmes connus

<table><thead><tr><th width="347.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td><code>atvtracka</code>, <code>smashdrvb</code> ou <code>smashdrvs</code> ne démarre pas</td><td>Placez le jeu parent (<code>atvtrack</code>, <code>smashdrv</code>) dans <code>roms\gaelco</code>, ou utilisez un romset non-merged.</td></tr><tr><td>Gaelco Football : R3 n'ouvre pas le menu de test</td><td>Le stick droit sert à frapper : utilisez la touche <strong>0</strong> du clavier.</td></tr><tr><td>Odin ne s'affiche pas sur le bon écran</td><td>Activez <strong>VIDÉO > DÉSACTIVER PLEIN ÉCRAN</strong>.</td></tr></tbody></table>
