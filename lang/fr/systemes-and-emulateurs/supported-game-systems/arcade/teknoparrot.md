---
description: TeknoGods
---

# TeknoParrot

<div align="left"><figure><img src="../../../.gitbook/assets/image (778).png" alt="" width="295"><figcaption></figcaption></figure></div>

## Présentation

Depuis le milieu des années 2000, beaucoup de bornes d'arcade sont de vrais PC : Sega Lindbergh, RingEdge et RingWide, Taito Type X, Namco System ES, NesicaxLive, Raw Thrills… **TeknoParrot** fait tourner ces jeux sous Windows en émulant les cartes d'entrées-sorties (JVS), les cartes de crédit et les périphériques de la borne : **Mario Kart Arcade GP DX**, **Initial D**, **Wangan Midnight Maximum Tune**, **The House of the Dead 4**, **Tekken 7**, **BlazBlue**, **Street Fighter V Type Arcade**…

TeknoParrot est développé par TeknoGods. Certains jeux et fonctions ne sont disponibles qu'avec un abonnement Patreon (Retrobat ne recommande pas l'abonnement !).

{% embed url="https://teknogods.github.io/index.html" %}

## En bref

<table><thead><tr><th width="264"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\teknoparrot</code></td></tr><tr><td><strong>Extensions</strong></td><td>.teknoparrot .parrot .game (dossiers) .zip .7z .rar</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>teknoparrot</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, jeu par jeu (fichier <code>teknoparrot.yml</code>) ; joueur 1 seulement pour les jeux absents du fichier</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>Oui, jusqu'à 4 (DemulShooter pour les jeux compatibles)</td></tr><tr><td><strong>Volants</strong></td><td>Oui</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="153.25">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>teknoparrot</strong> (seul émulateur)</td><td>Lance chaque jeu avec son profil TeknoParrot. Manettes, pistolets et volants configurés par RetroBat, plein écran, résolution, région et jeu gratuit réglés depuis RetroBat.</td><td>Pas de sauvegardes instantanées. Certains jeux demandent un abonnement Patreon TeknoParrot.</td></tr></tbody></table>

TeknoParrot sert aussi à d'autres systèmes de RetroBat, avec son propre émulateur intégré :

<table><thead><tr><th width="346.5">Système</th><th>Page</th></tr></thead><tbody><tr><td>Sega Lindbergh</td><td><a href="sega/lindbergh.md">Sega Lindbergh</a></td></tr><tr><td>Sega Chihiro (Cxbx)</td><td><a href="sega/sega-chihiro.md">Sega Chihiro</a></td></tr><tr><td>Triforce (Dolphin)</td><td><a href="sega/triforce.md">Triforce</a></td></tr><tr><td>Namco System 246/256 (PCSX2x6, Play!)</td><td><a href="namco-246-256.md">Namco 246/256</a></td></tr><tr><td>Namco System 357/369 (RPCS3)</td><td><a href="namco-357-369.md">Namco 357/369</a></td></tr></tbody></table>

## Installer TeknoParrot

TeknoParrot n'est pas fourni avec RetroBat.

1. Téléchargez **TeknoParrot Installer** sur la [page de téléchargement de TeknoParrot](https://teknoparrot.com/en/Home/Download).
2. Extrayez l'archive dans le dossier `emulators\teknoparrot` et lancez l'installeur : il télécharge TeknoParrot et les composants nécessaires.
3. Lancez une première fois `emulators\teknoparrot\TeknoParrotUi.exe` et installez toutes les mises à jour proposées.

<div align="left"><figure><img src="../../../.gitbook/assets/image (779).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (780).png" alt=""><figcaption><p>Mises à jour de TeknoParrot</p></figcaption></figure></div>

TeknoParrot recommande aussi d'installer **DirectX (juin 2010)** et les **Visual C++ Redistributable** (liens sur sa page de téléchargement).

{% hint style="warning" %}
Votre antivirus peut signaler des fichiers de TeknoParrot : il s'agit de faux positifs (fichiers qui modifient les jeux pour les lancer). Ajoutez une exception pour le dossier `emulators\teknoparrot`.
{% endhint %}

{% hint style="info" %}
**TeknoParrot UI 2.0** (version expérimentale proposée sur la même page) n'est pas encore prise en charge par RetroBat : utilisez **TeknoParrot Installer**.
{% endhint %}

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Chaque jeu est un **dossier** (copie du disque dur de la borne). Renommez le dossier avec l'extension `.teknoparrot`, `.parrot` ou `.game`, et placez-le dans `roms\teknoparrot`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (781).png" alt=""><figcaption></figcaption></figure></div>

Le nom du dossier (sans l'extension) permet à RetroBat de trouver le **profil TeknoParrot** du jeu. Le plus simple est d'utiliser le nom du profil, c'est-à-dire le nom du fichier `.xml` du jeu dans `emulators\teknoparrot\GameProfiles` (ou du fichier `.json` dans `emulators\teknoparrot\Metadata`).

Par exemple, pour _Mario Kart Arcade GP DX_ (profil `MKDX.xml`) : `MKDX.teknoparrot`, `MKDX.parrot` ou `MKDX.game`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (782).png" alt=""><figcaption></figcaption></figure></div>

RetroBat reconnaît aussi :

* le **nom du jeu** indiqué dans le fichier `Metadata` du profil (majuscules, `:`, `-`, `.` et `'` ignorés), par exemple `Mario Kart Arcade GP DX.teknoparrot` ;
* le **nom du dossier d'origine** de nombreux jeux, par exemple `Mario kart dx.teknoparrot`.

Si le profil n'est pas trouvé, RetroBat affiche le message « Unable to find game profile » : renommez le dossier avec le nom du profil.

```
roms\
└─ teknoparrot\
   └─ MKDX.teknoparrot\
      └─ MK_AGP3_FINAL.exe (et les autres fichiers du jeu)
```

### Jeux compressés

Un jeu peut aussi être compressé en `.zip`, `.7z` ou `.rar` : donnez à l'archive le nom du profil (`MKDX.zip`). RetroBat le décompresse dans un dossier temporaire avant de le lancer (ou le monte comme un lecteur si WinFsp ou Dokan est installé).

{% hint style="info" %}
Les jeux TeknoParrot sont volumineux : la décompression peut être longue. Un dossier non compressé démarre plus vite.
{% endhint %}

La liste des jeux compatibles est sur le [site de TeknoParrot](https://teknoparrot.com/).

## Contrôles

RetroBat configure les manettes **jeu par jeu** avec le fichier `system\resources\inputmapping\teknoparrot.yml` (plus de 1 000 entrées). Pour modifier le mappage d'un jeu, voir la page [**Configuration des touches TeknoParrot**](../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-teknoparrot.md).

Boutons communs à la plupart des jeux, comme sur les autres émulateurs arcade (voir le [guide arcade](../../arcade-guide.md)) :

<table><thead><tr><th width="232.75">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Crédit</td><td>SELECT</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Test (menu opérateur)</td><td>R3</td></tr><tr><td>Service</td><td>L3</td></tr><tr><td>Quitter</td><td>HOTKEY + START</td></tr></tbody></table>

Dans le menu opérateur, Service (L3) déplace le curseur et Test (R3) valide, sur la plupart des jeux.

Pour un jeu absent du fichier, RetroBat configure le joueur 1 :

| Action                                       | Manette                        |
| -------------------------------------------- | ------------------------------ |
| Directions                                   | Croix (ou stick gauche)        |
| Volant, accélérateur, frein (jeux de course) | Stick gauche, R2, L2           |
| Boutons 1 à 4                                | SUD, EST, NORD, OUEST          |
| Boutons 5 et 6                               | L1, R1 (L3, R3 en DirectInput) |
| Crédit / Start                               | SELECT / START                 |

**CONTRÔLES > DISPOSITION DES BOUTONS** permet de choisir une disposition adaptée à votre stick arcade pour les jeux qui en ont une dans le fichier (voir le guide arcade).

**PILOTES > MANETTES** choisit l'API des manettes : XInput est choisi automatiquement pour une manette XInput, DirectInput sinon.

## Pistolets

Jusqu'à 4 pistolets : activez **PISTOLETS > ACTIVER LES PISTOLETS**. Les jeux de tir ont un mappage pistolet dédié (entrée `<jeu>_gun` du fichier `teknoparrot.yml`). Voir la page [**Contrôle des pistolets**](../../../controleurs/pistolets_controles.md).

<table><thead><tr><th width="269">Action</th><th>Pistolet</th></tr></thead><tbody><tr><td>Tirer</td><td>Clic gauche</td></tr><tr><td>Recharger / bouton 2</td><td>Clic droit</td></tr><tr><td>Bouton 3 (grenade…)</td><td>Clic milieu</td></tr><tr><td>Start joueur 1 / joueur 2</td><td>Clavier 1 / 2</td></tr><tr><td>Crédit joueur 1 / joueur 2</td><td>Clavier 5 / 6</td></tr><tr><td>Test / Service</td><td>Clavier 0 / 9</td></tr></tbody></table>

Options utiles (sous-menu **PISTOLETS**) :

| Option                                                                     | Effet                                                               |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| **BOUTONS CRÉDIT/START**                                                   | SUR LE PISTOLET, SUR LE CLAVIER ou TEST/SERVICE SUR LE CLAVIER.     |
| **MASQUER LE VISEUR** / **MASQUER L'ARME**                                 | Masque le viseur ou le modèle de l'arme (selon le jeu).             |
| **HACK DE RECHARGEMENT HORS ÉCRAN**                                        | Recharger en tirant hors de l'écran (activé par défaut).            |
| **UTILISER DEMULSHOOTER**                                                  | Lance DemulShooter pour les jeux compatibles.                       |
| **INDEX DU 1ER PISTOLET** … **INDEX DU 4E PISTOLET**, **INDEX DU CLAVIER** | Ordre des pistolets et clavier associé, si plusieurs sont branchés. |

## Volants

Activez **VOLANTS DE COURSE > ACTIVER LES VOLANTS** : RetroBat configure le volant, le pédalier et le levier de vitesse pour les jeux de course. Voir la page [**Volants**](../../../controleurs/supported-controllers/volants.md).

| Option (sous-menu **VOLANTS DE COURSE**)           | Effet                                                          |
| -------------------------------------------------- | -------------------------------------------------------------- |
| **BOUTONS COIN & START**                           | Où placer Crédit et Start.                                     |
| **BOUTONS TEST & SERVICE**                         | Sur le volant, sur la manette (R3 / L3) ou au clavier (0 / 9). |
| **DÉSACTIVER LE LEVIER DE VITESSE**                | N'utilise pas le levier de vitesse.                            |
| **CONVERTISSEUR GEARUP/GEARDOWN VERS GEAR3/GEAR4** | Simule une boîte séquentielle sur un levier en H.              |
| **MODE SHIFT BATTLEGEAR4TUNED**                    | Mode de changement de vitesse de Battle Gear 4 Tuned.          |
| **PROFIL PERSONNALISÉ**                            | Charge un profil de mappage volant personnalisé (1 à 4).       |
| **FORCER L'ID DU LEVIER DE VITESSE**               | Choisit le levier de vitesse à utiliser.                       |

## Décorations

**DÉCORATIONS** affiche un bezel autour du jeu. Pour les jeux listés dans `system\tools\teknoparrotReshade.yml` (jeux de tir surtout, pour la bordure Sinden), le bezel passe par ReShade ; pour les autres, RetroBat l'affiche par-dessus la fenêtre du jeu.

## Raccourcis

<table><thead><tr><th width="242.75">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr></tbody></table>

Pas de sauvegardes instantanées.

## Dossiers

<table><thead><tr><th width="225.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\teknoparrot</code></td></tr><tr><td>TeknoParrot</td><td><code>emulators\teknoparrot</code></td></tr><tr><td>Profils des jeux</td><td><code>emulators\teknoparrot\GameProfiles</code> (et <code>Metadata</code>)</td></tr><tr><td>Réglages par jeu (écrits par RetroBat)</td><td><code>emulators\teknoparrot\UserProfiles</code></td></tr><tr><td>Réglages généraux de TeknoParrot</td><td><code>emulators\teknoparrot\ParrotData.xml</code></td></tr><tr><td>Mappage des manettes et des pistolets</td><td><code>system\resources\inputmapping\teknoparrot.yml</code> (copie modifiable : <code>user\inputmapping\teknoparrot.yml</code>)</td></tr><tr><td>Mappage des volants</td><td><code>system\resources\inputmapping\wheels\teknoparrot_wheels.yml</code>, <code>system\resources\inputmapping\teknoparrot_wheel_mapping.yml</code></td></tr><tr><td>Bezels ReShade, profils et exécutables particuliers</td><td><code>system\tools\teknoparrotReshade.yml</code>, <code>system\tools\teknoparrotInfo.yml</code></td></tr></tbody></table>

## Options utiles

| Option                                                              | Effet                                                                                                                                    |
| ------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **ÉMULATION > RÉGION/LANGUE**                                       | USA/ANGLAIS, EXPORT/ANGLAIS ou JAPONAIS, pour les jeux qui le proposent.                                                                 |
| **ÉMULATION > JEU GRATUIT**                                         | Jeu sans crédit (activé par défaut).                                                                                                     |
| **ÉMULATION > DÉSACTIVER DROITS ADMIN.**                            | Ne lance pas le jeu en administrateur, même si son profil le demande (plus de demande de Windows, mais certains jeux ne démarrent plus). |
| **VIDÉO > TYPE DE PLEIN ÉCRAN**                                     | FENÊTRÉ, PLEIN ÉCRAN FENÊTRÉ ou PLEIN ÉCRAN EXCLUSIF. Par défaut, plein écran fenêtré quand le jeu le propose.                           |
| **VIDÉO > UTILISER LA RÉSOLUTION DE L'ÉCRAN**                       | Force la résolution de l'écran actuel pour les jeux qui acceptent une résolution personnalisée.                                          |
| **VIDÉO > UTILISER UNE RÉSOLUTION PERSONNALISÉE**                   | Utilise la résolution de **VIDÉO > RÉSOLUTION DE L'ÉCRAN**.                                                                              |
| **PILOTES > MANETTES**                                              | XINPUT, DIRECTINPUT, RAW INPUT ou ENTRÉES FUSIONNÉES, pour les jeux qui le proposent.                                                    |
| **CONTRÔLES > ZONE MORTE JOYSTICK**                                 | Zone morte du stick pour les jeux de conduite (évite les à-coups du volant à la manette).                                                |
| **CONTRÔLES > FORCER L'INDEX DE LA MANETTE DU JOUEUR 1 / 2**        | Utile en XInput si les manettes sont inversées.                                                                                          |
| **INTERFACE UTILISATEUR > MASQUER TEKNOPARROT AU DÉMARRAGE DU JEU** | La fenêtre de TeknoParrot est masquée par défaut ; à désactiver si un jeu ne démarre pas correctement.                                   |
| **INTERFACE UTILISATEUR > AFFICHER LA CONSOLE**                     | Affiche la console de TeknoParrot (débogage).                                                                                            |
| **INTERFACE UTILISATEUR > AFFICHER LE CURSEUR DE LA SOURIS**        | Affiche le curseur (masqué par défaut).                                                                                                  |
| **INTERFACE UTILISATEUR > APM3ID (NÉCESSITE UN PROFIL EN LIGNE)**   | Identifiant APM3 pour les jeux en ligne de TeknoParrot.                                                                                  |
| **INTERFACE UTILISATEUR > NOTIFICATIONS DISCORD**                   | Affiche le jeu en cours sur Discord.                                                                                                     |

## Problèmes connus

| Problème                                  | Solution                                                                                                                                                                                 |
| ----------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Message « Unable to find game profile »   | Renommez le dossier du jeu avec le nom de son profil (voir [**Quel format de jeu ?**](teknoparrot.md#quel-format-de-jeu)).                                                               |
| Le jeu ne démarre pas, rien ne s'affiche  | Lancez le jeu une fois depuis `TeknoParrotUi.exe` pour voir le message d'erreur, puis désactivez **MASQUER TEKNOPARROT AU DÉMARRAGE DU JEU**. Vérifiez aussi l'exception de l'antivirus. |
| Écran noir en plein écran                 | Réglez **VIDÉO > TYPE DE PLEIN ÉCRAN** sur FENÊTRÉ ou PLEIN ÉCRAN FENÊTRÉ.                                                                                                               |
| Windows demande les droits administrateur | Normal pour certains jeux ; **ÉMULATION > DÉSACTIVER DROITS ADMIN.** supprime la demande, si le jeu le supporte.                                                                         |
| Les commandes ne répondent pas            | Laissez **PILOTES > MANETTES** en automatique ; si plusieurs manettes XInput sont branchées, utilisez **FORCER L'INDEX DE LA MANETTE DU JOUEUR 1**.                                      |
| Le menu opérateur s'ouvre par erreur      | Test est sur R3 : évitez d'appuyer sur le stick droit, ou utilisez une disposition arcade.                                                                                               |
| Jeu réservé aux abonnés                   | Certains jeux demandent un abonnement Patreon TeknoParrot.                                                                                                                               |

