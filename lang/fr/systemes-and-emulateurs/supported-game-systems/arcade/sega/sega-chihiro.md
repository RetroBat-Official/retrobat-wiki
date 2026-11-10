---
description: Sega
---

# Sega Chihiro

<div align="left"><figure><img src="../../../../.gitbook/assets/image (511).png" alt="" width="557"><figcaption></figcaption></figure></div>

## Présentation

La **Chihiro** est un système d'arcade conçu par **Sega** avec **Microsoft** et sorti en **2002**. Il reprend l'architecture de la Xbox (processeur Intel Pentium III à 733 MHz, puce graphique NVIDIA NV2A) avec deux fois plus de mémoire vive (128 Mo). Son nom vient de l'héroïne du film _Le Voyage de Chihiro_.

Comme les systèmes Naomi et Triforce, la Chihiro lit ses jeux sur un **GD-ROM** : le disque est entièrement copié dans la mémoire d'une carte DIMM au démarrage, ce qui supprime les temps de chargement pendant la partie. C'est le dernier système d'arcade de Sega dérivé d'une console de salon ; son successeur, la Lindbergh, repose sur une architecture PC.

On lui doit notamment **The House of the Dead III**, **Virtua Cop 3**, **Ghost Squad**, **OutRun 2**, **Crazy Taxi High Roller**, **Ollie King** et, chez Namco, **Wangan Midnight Maximum Tune** 1 et 2. Plusieurs de ces jeux ont été adaptés ensuite sur Xbox, grâce à leur matériel commun.

{% embed url="https://fr.wikipedia.org/wiki/Chihiro_(syst%C3%A8me_d'arcade)" %}

## En bref <a href="#en-bref" id="en-bref"></a>

<table><thead><tr><th width="262.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\chihiro</code></td></tr><tr><td><strong>Extensions</strong></td><td>.xbe .iso .bin</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>xemu-chihiro</td></tr><tr><td><strong>BIOS</strong></td><td><code>chihiro_xbox_bios.bin</code>, <code>fpr21042_m29w160et.bin</code>, <code>ic10_g24lc64.bin</code>, <code>ic11_24lc024.bin</code>, <code>pc20_g24lc64.bin</code> dans <code>bios\chihiro</code></td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs (xemu-chihiro : jeux reconnus)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>xemu-chihiro, chihiro et chihiro-gun (DemulShooter), TeknoParrot</td></tr><tr><td><strong>Volants</strong></td><td>xemu-chihiro, TeknoParrot</td></tr></tbody></table>

L'émulateur par défaut est le fork xemu de Tovarichtch: [https://github.com/Tovarichtch/xemu](https://github.com/Tovarichtch/xemu)

## BIOS

Placez les fichiers suivants dans `bios\chihiro`. RetroBat vérifie leur présence.

| Fichier                  | Obligatoire                                                                   |
| ------------------------ | ----------------------------------------------------------------------------- |
| `chihiro_xbox_bios.bin`  | Oui                                                                           |
| `ic10_g24lc64.bin`       | Oui                                                                           |
| `ic11_24lc024.bin`       | Oui                                                                           |
| `pc20_g24lc64.bin`       | Oui                                                                           |
| `fpr21042_m29w160et.bin` | Oui (xemu-chihiro accepte aussi `fpr-23887_29lv160te.ic4` ou `fpr-23887.bin`) |

Avec **xemu-chihiro** (émulateur par défaut), il n'y a rien d'autre à faire : RetroBat utilise directement les fichiers du dossier `bios\chihiro`.

### Émulateurs basés sur CXBX (chihiro, chihiro-gun, cxbx, TeknoParrot)

Ces émulateurs lisent les fichiers de la carte dans leur propre dossier `EmuMediaBoard`. Copiez-les depuis `bios\chihiro` :

| Fichier                                                    | Destination              |
| ---------------------------------------------------------- | ------------------------ |
| `fpr21042_m29w160et.bin`                                   | `EmuMediaBoard\`         |
| `ic10_g24lc64.bin`, `ic11_24lc024.bin`, `pc20_g24lc64.bin` | `EmuMediaBoard\chihiro\` |

Le dossier `EmuMediaBoard` se trouve dans le dossier de chaque émulateur : `emulators\chihiro`, `emulators\chihiro-ds` (chihiro-gun), `emulators\cxbx-reloaded` et TeknoParrot.

## Contrôles

### Xemu-chihiro

RetroBat configure automatiquement les contrôles Chihiro pour les jeux pris en charge par xemu-chihiro :

| Type     | Jeux                                                             |
| -------- | ---------------------------------------------------------------- |
| Pistolet | The House of the Dead III, Virtua Cop 3, Ghost Squad             |
| Conduite | Crazy Taxi High Roller, OutRun 2, Wangan Midnight Maximum Tune 2 |
| Autres   | Ollie King, Gundam Battle Operating Simulator                    |

{% hint style="info" %}
* Seule la **manette du joueur 1** (la première manette dans EmulationStation) est utilisée pour les contrôles du jeu. Le joueur 2 n'a que **Start / Coin au clavier**, sauf dans les jeux de tir avec deux pistolets.
* **Test** (`0`) et **Service** (`9`) sont toujours au clavier.
* Pour utiliser votre propre configuration, réglez **AUTOCONFIGURE CONTROLLERS** sur OFF et configurez les contrôles dans xemu-chihiro.
{% endhint %}

{% hint style="info" %}
Les noms des options peuvent différer légèrement selon la langue choisie dans EmulationStation.
{% endhint %}

#### Manette (joueur 1)

Les boutons portent les noms Xbox (A = bouton du bas). Avec une manette à disposition Nintendo, activez **INVERT FACE BUTTONS** (Contrôles) pour inverser A/B et X/Y.

**Boutons système (tous les jeux)**

| Manette       | Fonction                                                                                           |
| ------------- | -------------------------------------------------------------------------------------------------- |
| Start         | Start                                                                                              |
| Back / Select | Coin (crédit)                                                                                      |
| B             | Insertion de carte (jeux à carte : un appui insère la carte, Maximum Tune la rend au second appui) |

**Jeux de conduite** (Crazy Taxi High Roller, OutRun 2, Maximum Tune 2)

| Manette              | Fonction                      |
| -------------------- | ----------------------------- |
| Stick gauche         | Direction                     |
| Gâchette droite (RT) | Accélérateur                  |
| Gâchette gauche (LT) | Frein                         |
| RB / LB              | Rapport supérieur / inférieur |

| Manette | Crazy Taxi High Roller | OutRun 2          | Maximum Tune 2     |
| ------- | ---------------------- | ----------------- | ------------------ |
| A       | Saut                   | –                 | –                  |
| B       | Marche avant           | –                 | Insertion de carte |
| X       | Marche arrière         | –                 | Intrude change     |
| Y       | –                      | Changement de vue | Changement de vue  |

**Ollie King**

| Manette                      | Fonction                      |
| ---------------------------- | ----------------------------- |
| Stick gauche gauche / droite | Balancement gauche / droite   |
| Stick gauche haut / bas      | Avant / arrière de la planche |
| LB / RB                      | Grab gauche / Grab droit      |

**Gundam Battle Operating Simulator** (cockpit à deux leviers)

| Manette      | Fonction                           |
| ------------ | ---------------------------------- |
| Stick gauche | Levier gauche                      |
| LT / LB      | Gâchette / bouton du levier gauche |
| Stick droit  | Levier droit                       |
| RT / RB      | Gâchette / bouton du levier droit  |
| A            | Pédale                             |

#### Clavier

Sans manette, le clavier est utilisé :

| Touche  | Fonction                                      |
| ------- | --------------------------------------------- |
| 1 / 5   | Start / Coin joueur 1                         |
| 2 / 6   | Start / Coin joueur 2                         |
| 0 / 9   | Test / Service                                |
| Flèches | Direction, accélérateur (Haut) et frein (Bas) |
| Z / X   | Rapport supérieur / inférieur                 |
| C       | Insertion de carte                            |

Les touches propres à chaque jeu sont celles par défaut de xemu-chihiro (par exemple Espace pour la pédale de Virtua Cop 3 et le changement d'arme de Ghost Squad, W A S D + flèches pour Gundam). Elles se modifient dans le menu des contrôles de xemu-chihiro.

{% hint style="info" %}
Les touches indiquées sont celles d'un clavier QWERTY : sur un clavier AZERTY, Z, W, A et Q correspondent aux touches W, Z, Q et A.
{% endhint %}

#### Jeux de tir

Activez **ENABLE GUN** (Guns). xemu-chihiro lit chaque souris ou pistolet séparément : avec deux pistolets, chaque joueur a le sien.

| Pistolet               | The House of the Dead III      | Virtua Cop 3                   | Ghost Squad                    |
| ---------------------- | ------------------------------ | ------------------------------ | ------------------------------ |
| Gâchette (clic gauche) | Tir                            | Tir                            | Tir                            |
| Clic droit             | Bouton du pistolet             | Bouton du pistolet             | Bouton du pistolet             |
| Clic milieu            | –                              | Pédale (se mettre à couvert)   | Changement d'arme              |
| Rechargement           | Viser hors de l'écran et tirer | Viser hors de l'écran et tirer | Viser hors de l'écran et tirer |

* **Start / Coin** : touches `1` / `5` pour le joueur 1, `2` / `6` pour le joueur 2 (la plupart des pistolets savent envoyer ces touches).
* **RELOAD WITH BUTTON** : pour les pistolets qui ne savent pas tirer hors de l'écran. Le clic milieu recharge, et la pédale / le changement d'arme passe au clavier (`Q` pour le joueur 1, `S` pour le joueur 2).
* **INVERT TRIGGER/RELOAD** : inverse les clics gauche et droit.
* **USE ONE GUN ONLY** : seul le joueur 1 utilise un pistolet.
* **Sinden** : la bordure blanche est dessinée par l'émulateur (**SINDEN BORDER**, **SINDEN BORDER SIZE**).
* **CROSSHAIR** : choisissez _custom_ et sélectionnez une image avec **CUSTOM CROSSHAIR FILE**.

{% hint style="info" %}
**Wiimote avec une DolphinBar** : Start / Coin sont sur la croix de la Wiimote. Voir Wiimote & DolphinBar.
{% endhint %}

#### Volants et retour de force

Un volant utilisé comme manette du joueur 1 se pilote avec les mêmes commandes qu'une manette (direction, pédales, palettes sur RB / LB). Options dans **Wheels** :

| Option                                   | Description                                                                                                |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ENABLE FORCE FEEDBACK                    | Retour de force de la carte de pilotage (OutRun 2, Maximum Tune), sur un volant ou en vibration de manette |
| FORCE FEEDBACK STRENGTH                  | Intensité des effets                                                                                       |
| INVERT FORCE FEEDBACK                    | À activer si le volant est poussé loin du centre au lieu d'y revenir                                       |
| WHEEL ROTATION                           | Degrés de rotation pour le braquage maximal (270 = borne d'arcade)                                         |
| WHEEL AUTO-CENTER / AUTO-CENTER STRENGTH | Ressort de rappel au centre quand le jeu n'envoie pas de retour de force                                   |

### CXBX

Les contrôles doivent être paramétrés directement dans l'émulateur CXBX-Reloaded, l'exécutable de l'émulateur se trouve dans le dossier `\emulators\cxbx-reloaded`.

<div align="left"><figure><img src="https://i.imgur.com/W2oGLGE.png" alt=""><figcaption></figcaption></figure></div>

Pour Teknoparrot, les contrôles sont gérés par Teknoparrot: [détails ici](../teknoparrot.md#controles)

## Informations spécifiques au système

### ROMs

#### XEMU-CHIHIRO

Xemu-Chihiro nécessite des roms de jeu au format bin (netboot), l'outil en lien permet de convertir des romsets MAME vers le format attendu:

{% embed url="https://github.com/Tovarichtch/chihiro-netboot" %}

#### CXBX

Les ROMs Chihiro sont fournies sous forme d'un dossier contenant plusieurs fichiers et sous-dossiers, dont des fichiers de type .xbe.

Le dossier du jeu doit être placé dans le répertoire `\roms\chihiro`.

<div align="left"><figure><img src="https://i.imgur.com/K61I22N.png" alt=""><figcaption></figcaption></figure></div>

En règle générale, les fichiers .xbe terminant par \_t (par exemple `vc3_t.xbe`) permettent d'accéder au menu TEST du jeu.

### Le menu TEST

Le menu TEST permet d'accéder à diverses options de paramétrages propres au jeu, telles que la calibration du lightGun ou encore le niveau de difficulté.

* **Pour xemu-chihiro**: accéder au menu test à l'aide des touches 0 et 9 du clavier
* **Pour CXBX**: démarrer le fichier .xbe terminant par "\_t" pour accéder au menu TEST.

<div align="left"><figure><img src="https://i.imgur.com/V1mJQyY.png" alt=""><figcaption></figcaption></figure></div>

### Utiliser le bios Cerbios (XEMU)

Télécharger le firmware cerbios et renommez-le en _Cerbios.bin_, puis placez-le dans le dossier `retrobat\bios`.

Sélectionnez ensuite le bios Cerbios dans les options RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/1WzUULh.png" alt=""><figcaption></figcaption></figure></div>
