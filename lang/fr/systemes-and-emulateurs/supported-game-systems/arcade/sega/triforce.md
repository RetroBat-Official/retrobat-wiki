---
description: Namco, Sega, Nintendo
---

# Triforce

<div align="left"><figure><img src="../../../../.gitbook/assets/image (517).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

**Triforce** est un système d'arcade conçu ensemble par **Nintendo**, **Namco** et **Sega**, d'où son nom : trois entreprises, comme les trois triangles de la Triforce de Zelda. Le premier jeu, Virtua Striker 2002, sort en 2002.

Le système reprend l'architecture de la **GameCube** (processeur IBM « Gekko », puce graphique ATI « Flipper »), avec plus de mémoire et l'électronique d'une borne d'arcade. Comme les systèmes Naomi et Chihiro, la plupart des jeux sont livrés sur **GD-ROM** : le disque est copié en entier dans la mémoire d'une carte DIMM au démarrage, ce qui supprime les temps de chargement.

Sa ludothèque est courte mais mémorable:

* **F-Zero AX** et **F-Zero AX Monster Ride** (Sega / Nintendo) : F-Zero AX pouvait échanger des données avec F-Zero GX sur GameCube, grâce à la carte mémoire ;
* **Mario Kart Arcade GP** et **Mario Kart Arcade GP 2** (Namco / Nintendo) ;
* **Virtua Striker 2002**, **Virtua Striker 4** et **Virtua Striker 4 Ver. 2006** (Sega) ;
* **Gekitou Pro Yakyuu** (Sega).

{% embed url="https://fr.wikipedia.org/wiki/Triforce_(syst%C3%A8me_d'arcade)" %}

## En bref

<table><thead><tr><th width="254"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\triforce</code></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .zip .cue .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>dolphin</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun obligatoire (<code>segaboot.gcm</code> optionnel, pour le menu de test)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, Dolphin</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Volants</strong></td><td>TeknoParrot</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="132.75">Émulateur</th><th width="158">Pour qui ?</th><th width="250.5">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>dolphin</strong> (par défaut)</td><td>Tout le monde</td><td>Version actuelle de Dolphin, qui émule la Triforce. HD, écran large, disposition des commandes adaptée à chaque jeu, menu de test, patchs de jeux.</td><td>—</td></tr><tr><td><strong>lr-dolphin</strong></td><td>Utilisateurs de RetroArch</td><td>Fonctions de RetroArch (shaders, menu RetroArch).</td><td>Moins de réglages.</td></tr><tr><td><strong>dolphin-triforce</strong></td><td>Cas particuliers</td><td>Ancienne version de Dolphin spécialisée Triforce (version « Crediar »), gardée pour les jeux qui y tournent mieux.</td><td>Version figée, plus mise à jour.</td></tr><tr><td><strong>TeknoParrot</strong></td><td>Utilisateurs de volant</td><td>Volants et retour de force pour F-Zero AX et Mario Kart Arcade GP.</td><td>Nécessite l'installation de TeknoParrot (voir la <a href="../teknoparrot.md">page <strong>TeknoParrot</strong></a>).</td></tr></tbody></table>

**Dans le doute, gardez dolphin.**

## BIOS

Aucun BIOS n'est nécessaire pour jouer.

<table><thead><tr><th width="153.25">Fichier</th><th width="405.75">Rôle</th><th>Emplacement</th></tr></thead><tbody><tr><td><code>segaboot.gcm</code></td><td>Optionnel : menu de test de la borne, avec Dolphin</td><td><code>bios\triforce</code></td></tr></tbody></table>

* RetroBat copie lui-même `segaboot.gcm` dans `emulators\dolphin-emu\User\Triforce` au lancement d'un jeu avec Dolphin.
* RetroBat vérifie la présence de ce fichier.
* dolphin-triforce n'en a pas besoin.

## Quel format de jeu ?

| Format     | dolphin                      | lr-dolphin | dolphin-triforce             | Remarques             |
| ---------- | ---------------------------- | ---------- | ---------------------------- | --------------------- |
| **.iso**   | ✔                            | ✔          | ✔                            | Image du jeu.         |
| .zip / .7z | ✔ (décompressé au lancement) | ✘          | ✔ (décompressé au lancement) | Chargement plus lent. |

Pour TeknoParrot, voir la [page **TeknoParrot**](../teknoparrot.md).

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes des joueurs 1 et 2, pour tous les émulateurs. Avec Dolphin et dolphin-triforce, la disposition des commandes est **choisie automatiquement selon le jeu** : Mario Kart, F-Zero, Virtua Striker ou disposition standard.

L'option **CONTRÔLES > DISPOSITION DES BOUTONS** force une disposition : **STANDARD**, **MARIO KART GP**, **F ZERO**, **VIRTUA STRIKER** ou **VIRTUA STRIKER 2002**.

### Boutons de la borne

<table><thead><tr><th width="164">Manette RetroBat</th><th width="170.5">Dolphin</th><th width="168.5">dolphin-triforce</th><th width="211.25">lr-dolphin</th></tr></thead><tbody><tr><td>SELECT</td><td>Crédit (Coin)</td><td>Crédit (Coin)</td><td>Crédit (Coin)</td></tr><tr><td>START</td><td>Start</td><td>Start</td><td>Start</td></tr><tr><td>L3</td><td>Service</td><td>—</td><td>—</td></tr><tr><td>R3</td><td>Test (menu de la borne)</td><td>Test (menu de la borne)</td><td>—</td></tr><tr><td>L1</td><td>—</td><td>—</td><td>Test (menu de la borne)</td></tr></tbody></table>

### Commandes de jeu

Les commandes sont placées de la même façon avec Dolphin et dolphin-triforce :

<table><thead><tr><th width="302.75">Jeu</th><th>Commandes</th></tr></thead><tbody><tr><td><strong>Mario Kart Arcade GP 1 et 2</strong></td><td>Volant = stick gauche, accélérer = R2, freiner = L2, objet = EST, annuler = SUD.</td></tr><tr><td><strong>F-Zero AX</strong>, <strong>F-Zero AX Monster Ride</strong></td><td>Volant = stick gauche, accélérer = R2, freiner = L2, palettes gauche / droite = L1 / R1, boost = OUEST, vues = croix directionnelle.</td></tr><tr><td><strong>Virtua Striker 4</strong>, <strong>Virtua Striker 4 Ver. 2006</strong></td><td>Déplacement = stick gauche, passe courte = SUD, passe longue = OUEST, tir = EST, sprint = NORD, tactiques = croix haut / droite / bas.</td></tr><tr><td><strong>Virtua Striker 2002</strong></td><td>Déplacement = croix directionnelle, passe courte = SUD, passe longue = EST, tir = OUEST.</td></tr><tr><td><strong>Gekitou Pro Yakyuu</strong></td><td>Croix directionnelle, boutons EST et SUD, OUEST = Gekitou.</td></tr><tr><td>Autres jeux (STANDARD)</td><td>Disposition d'une manette GameCube : A = EST, B = SUD, Y = OUEST, gâchettes L / R = L2 / R2, sticks et croix directionnelle.</td></tr></tbody></table>

Pour configurer vous-même vos manettes, désactivez **AUTOCONFIGURER LES MANETTES**.

### Raccourcis

**Dolphin** et **dolphin-triforce** utilisent les mêmes raccourcis que sur GameCube : **HOTKEY + START** pour quitter, **HOTKEY + OUEST** / **HOTKEY + NORD** pour les sauvegardes d'état (Dolphin)…

**lr-dolphin** utilise les raccourcis de RetroArch (voir la [page Raccourcis](../../../../navigation/hotkeys.md)).

## Dossiers

<table><thead><tr><th width="364">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes d'état Dolphin</td><td><code>saves\triforce\dolphin</code></td></tr><tr><td>Sauvegardes d'état lr-dolphin</td><td><code>saves\triforce\libretro.dolphin</code></td></tr><tr><td>Données de la borne (Dolphin)</td><td><code>emulators\dolphin-emu\User\Triforce</code></td></tr><tr><td>Réglages et patchs par jeu (Dolphin)</td><td><code>emulators\dolphin-emu\User\GameSettings</code></td></tr><tr><td>Liste des patchs proposés par RetroBat</td><td><code>system\tools\triforce_patches.json</code></td></tr><tr><td>dolphin-triforce</td><td><code>emulators\dolphin-triforce</code></td></tr></tbody></table>

## Guides

### Patchs de jeux

Certains jeux bloquent au démarrage, attendent du matériel de la borne absent (moteur du siège de F-Zero, caméra de Mario Kart GP 2, liaison entre bornes…) ou ralentissent. RetroBat propose des patchs pour ces jeux, dans les options du jeu, sous **PATCHS DE JEUX** :

<table><thead><tr><th width="257.75">Jeu</th><th>Patchs</th></tr></thead><tbody><tr><td>F-Zero AX</td><td>Désactiver la configuration du moteur (rev D ou rev E, selon votre version).</td></tr><tr><td>F-Zero AX Monster Ride</td><td>Désactiver le moteur, contourner le siège Cycraft, corriger les ralentissements.</td></tr><tr><td>Mario Kart Arcade GP</td><td>Corriger la boucle, ignorer la liaison entre bornes, corriger les ralentissements, ignorer la vérification au démarrage.</td></tr><tr><td>Mario Kart Arcade GP 2</td><td>Désactiver la caméra (NamCam), corriger la boucle, les ralentissements, ignorer la liaison entre bornes et les vérifications au démarrage (versions US ou JAP).</td></tr><tr><td>Virtua Striker 4 / Ver. 2006</td><td>Passer le démarrage (version 2006 : US ou JAP).</td></tr></tbody></table>

Tous les patchs sont désactivés par défaut : activez seulement ceux qui correspondent à votre jeu et à sa version.

## Problèmes connus

| Problème                                                                  | Solution                                                                                            |
| ------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Le jeu reste bloqué sur un écran de vérification ou d'erreur au démarrage | Activez le patch correspondant dans **PATCHS DE JEUX** (voir [Guides](triforce.md#patchs-de-jeux)). |
| Le menu de test ne s'ouvre pas avec Dolphin                               | Placez `segaboot.gcm` dans `bios\triforce`.                                                         |
| Les commandes ne correspondent pas au jeu                                 | Choisissez la bonne **DISPOSITION DES BOUTONS** dans les options du jeu.                            |
| Un jeu ne fonctionne pas avec Dolphin                                     | Essayez **dolphin-triforce**.                                                                       |
| lr-dolphin ne lance pas le jeu                                            | lr-dolphin ne lit pas les jeux en .zip ou .7z : décompressez-les, ou utilisez Dolphin.              |
