---
description: Sega
---

# Sega Chihiro

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/chihiro-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/chihiro.svg" alt=""></picture><figcaption></figcaption></figure></div>

Arcade - Année de création : 2002

{% embed url="https://fr.wikipedia.org/wiki/Chihiro_(syst%C3%A8me_d'arcade)" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>xemu-chihiro</li><li>chihiro (vieux CXBX-Reloaded)</li><li>chihiro-gun (chihiro-ds 1.0)</li><li>cxbx</li><li>Teknoparrot</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> chihiro</td></tr><tr><td><strong>Extensions</strong></td><td>.xbe .iso .bin</td></tr></tbody></table>

L'émulateur par défaut est le fork xemu de Tovarichtch: [https://github.com/Tovarichtch/xemu](https://github.com/Tovarichtch/xemu)

## Bios

<table><thead><tr><th width="216.80555555555554">Fichier</th><th width="558.75">Dossier</th></tr></thead><tbody><tr><td>chihiro_xbox_bios.bin</td><td><code>\bios\chihiro</code></td></tr><tr><td>fpr21042_m29w160et.bin</td><td><p><code>\bios\chihiro</code></p><p><code>\emulators\cxbx-reloaded\EmuMediaBoard</code><br><code>\emulators\chihiro\EmuMediaBoard</code><br><code>\emulators\chihiro-ds\EmuMediaBoard</code><br><code>\emulators\teknoparrot\cxbxr\TeknoParrot\EmuMediaBoard</code></p></td></tr><tr><td>ic10_g24lc64.bin</td><td><p><code>\bios\chihiro</code></p><p><code>\emulators\cxbx-reloaded\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro-ds\EmuMediaBoard\chihiro</code><br><code>\emulators\teknoparrot\cxbxr\TeknoParrot\EmuMediaBoard\Chihiro</code></p></td></tr><tr><td>ic11_24lc024.bin</td><td><p><code>\bios\chihiro</code></p><p><code>\emulators\cxbx-reloaded\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro-ds\EmuMediaBoard\chihiro</code><br><code>\emulators\teknoparrot\cxbxr\TeknoParrot\EmuMediaBoard\Chihiro</code></p></td></tr><tr><td>pc20_g24lc64.bin</td><td><p><code>\bios\chihiro</code></p><p><code>\emulators\cxbx-reloaded\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro\EmuMediaBoard\chihiro</code><br><code>\emulators\chihiro-ds\EmuMediaBoard\chihiro</code><br><code>\emulators\teknoparrot\cxbxr\TeknoParrot\EmuMediaBoard\Chihiro</code></p></td></tr></tbody></table>

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
