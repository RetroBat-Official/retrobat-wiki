---
description: >-
  Utiliser une Wiimote comme pistolet avec une DolphinBar Mayflash (modes 1 et
  2).
---

# Wiimote et DolphinBar

Cette page explique comment utiliser une Wiimote comme pistolet avec une **DolphinBar Mayflash** en **mode 1 ou mode 2**, et comment les boutons de la Wiimote sont affectés dans chaque émulateur.

{% hint style="info" %}
RetroBat utilise **la même disposition dans tous les émulateurs** : gâchette pour tirer, A pour recharger, croix Droite pour Start, croix Gauche pour Coin (crédit). Une seule disposition à retenir.
{% endhint %}

{% hint style="warning" %}
Pour le **mode 4** (WiimoteGun ou Wiimote4Guns), voir [WiimoteGun](wiimotegun.md). La disposition de cette page ne s'applique pas au mode 4.
{% endhint %}

### Réglage de la DolphinBar

1. Placez la DolphinBar sous (ou au-dessus de) l'écran et réglez l'interrupteur à l'arrière sur **BOTTOM** (ou **TOP**) selon sa position.
2. Appairez la Wiimote : appuyez sur le bouton **SYNC** de la DolphinBar, puis sur les boutons **1** et **2** de la Wiimote.
3. Choisissez le mode avec le bouton **MODE** de la DolphinBar, ou avec une combinaison de boutons de la Wiimote :

<table><thead><tr><th width="186.5">Mode DolphinBar</th><th width="262.75">Combinaison sur la Wiimote</th><th width="97">LEDs de la Wiimote</th><th>Utilisation dans RetroBat</th></tr></thead><tbody><tr><td><strong>Mode 2 – Jeu</strong> (recommandé)</td><td>Maintenir <strong>Home</strong> + appuyer sur <strong>croix Gauche</strong></td><td>1 + 4</td><td>Pistolet (par défaut)</td></tr><tr><td>Mode 1 – Normal</td><td>Maintenir <strong>Home</strong> + appuyer sur <strong>croix Bas</strong></td><td>1 + 2</td><td>Pistolet</td></tr><tr><td>Mode 1 – Multimédia</td><td>Appuyer à nouveau sur <strong>Home</strong> + <strong>croix Bas</strong> en mode 1</td><td>1 + 3</td><td>❌ Non pris en charge (la croix envoie des touches multimédia)</td></tr><tr><td>Mode 3 – Manette</td><td>Maintenir <strong>Home</strong> + appuyer sur <strong>croix Haut</strong></td><td>1 à 4</td><td>❌ Pas un pistolet</td></tr><tr><td>Mode 4 – Émulateur Wii</td><td>Maintenir <strong>Home</strong> + appuyer sur <strong>croix Droite</strong></td><td>1 à 4</td><td>WiimoteGun, Wiimote4Guns et Dolphin uniquement</td></tr></tbody></table>

Le mode choisi est mémorisé par la DolphinBar.

{% hint style="warning" %}
En mode 1 et en mode 2, une DolphinBar ne gère **qu'une seule Wiimote** : pour jouer à deux, il faut **une DolphinBar par Wiimote**.
{% endhint %}

### Réglages dans RetroBat

Dans EmulationStation, ouvrez [**MENU PRINCIPAL**](../../../navigation/main-menu.md#parametres-des-jeux) **> PARAMÈTRES DES JEUX > PISTOLETS > WIIMOTE** :

* **WIIMOTE CONNECTION MODE** (mode de connexion de la Wiimote) : choisissez le mode de votre DolphinBar.
  * **MODE 1 (NORMAL)** : à choisir si votre DolphinBar est en mode 1.
  * **MODE 2 (GAME)** : également utilisé si l'option n'est pas réglée.

<div align="left"><figure><img src="../../../.gitbook/assets/image (358).png" alt=""><figcaption></figcaption></figure></div>

Puis, dans la [configuration avancée du système](../../../navigation/configuration-des-systemes-et-des-jeux.md#pour-un-systeme) ou du [jeu](../../../navigation/configuration-des-systemes-et-des-jeux.md#pour-un-jeu), sous-menu **PISTOLETS** :

* **ACTIVER LES PISTOLETS** : activé automatiquement pour les jeux au pistolet, à régler sur **ON** pour les autres jeux.
* **INVERSER GÂCHETTE ET RECHARGE** : à activer si la gâchette recharge au lieu de tirer (Wii Zapper, Nunchuk…).

<div align="left"><figure><img src="../../../.gitbook/assets/image (359).png" alt=""><figcaption></figcaption></figure></div>

Start, Coin, tir et rechargement sont **identiques en modes 1 et 2**. Le mode ne change que quelques boutons supplémentaires (1, 2, +).

### Disposition des boutons

| Bouton de la Wiimote                     | Fonction                                            |
| ---------------------------------------- | --------------------------------------------------- |
| **B** (gâchette)                         | Tir                                                 |
| **A**                                    | Rechargement (ou second bouton du pistolet)         |
| **Croix Droite**                         | Start                                               |
| **Croix Gauche**                         | Coin / Select                                       |
| **Croix Bas**                            | Action secondaire (grenade, pédale, arme spéciale…) |
| **Croix Haut**                           | Premier bouton spécifique au jeu                    |
| **1** / **2** (mode 1) ou **+** (mode 2) | Boutons supplémentaires spécifiques au jeu          |
| **Home**                                 | ⚠️ À éviter : agit comme la touche Windows          |

Les touches clavier **1-4** (Start) et **5-8** (Coin) restent actives dans tous les émulateurs.

{% hint style="warning" %}
**Effets de la DolphinBar** (indépendants de RetroBat) :

* Mode 2 : les boutons **1** et **2** envoient les touches Windows _volume + / volume −_.
* Mode 2 : le bouton **−** envoie _Échap_, ce qui **ferme** de nombreux émulateurs.
{% endhint %}

#### Deux Wiimotes

Chaque Wiimote a besoin de sa propre DolphinBar (voir plus haut).

Dans la plupart des émulateurs, tous les claviers sont vus comme un seul : les deux Wiimotes envoient les mêmes touches. RetroBat donne alors **d'autres directions au joueur 2** :

|       | Wiimote du joueur 1 | Wiimote du joueur 2 |
| ----- | ------------------- | ------------------- |
| Start | Croix **Droite**    | Croix **Haut**      |
| Coin  | Croix **Gauche**    | Croix **Bas**       |

**Chaque joueur doit utiliser uniquement ses propres directions** : croix Haut sur la Wiimote du joueur 1 lance le joueur 2.

Quelques émulateurs savent distinguer les claviers (**TeknoParrot**, **Supermodel**, **Flycast** avec 2 pistolets). Les deux Wiimotes y utilisent la même disposition (Droite = Start, Gauche = Coin).

### Émulateurs arcade

#### TeknoParrot

| Wiimote                                | Fonction                                                             |
| -------------------------------------- | -------------------------------------------------------------------- |
| B / A                                  | Tir / Rechargement                                                   |
| Droite / Gauche                        | Start / Coin                                                         |
| Bas                                    | Action secondaire (bouton milieu de la souris dans le profil du jeu) |
| Haut, puis 1, 2 (mode 1) ou + (mode 2) | Boutons supplémentaires du jeu                                       |

* Les **boutons supplémentaires** (sélection dans _Time Crisis 3/4_, pédales dans _2 Spicy_ et _Time Crisis 5_…) sont placés automatiquement dans l'ordre défini dans `system\resources\inputmapping\teknoparrot.yml`. S'il n'y a pas assez de boutons libres (par exemple _Police 911_), les restants sont sur les flèches du clavier.
* Si les joueurs 1 et 2 sont inversés, activez **WIIMOTE ASSOCIATION ALTERNATIVE**.
* **BOUTONS CRÉDIT/START** réglé sur _SUR LE CLAVIER_ remet Start/Coin sur le clavier (1-4 / 5-8).

#### Model 2

Deux Wiimotes utilisent la disposition partagée (joueur 2 : Haut = Start, Bas = Coin). **FORCER LE CLAVIER POUR START/PIÈCE** remet Start/Coin sur le clavier uniquement.

#### Model 3 (Supermodel)

| Wiimote         | Fonction           |
| --------------- | ------------------ |
| B / A           | Tir / Rechargement |
| Droite / Gauche | Start / Coin       |

Avec deux pistolets, Supermodel lit chaque clavier séparément : les deux Wiimotes utilisent Droite/Gauche.

#### Flycast (Naomi, Atomiswave)

| Wiimote         | Fonction           |
| --------------- | ------------------ |
| B / A           | Tir / Rechargement |
| Droite / Gauche | Start / Coin       |
| Bas             | Bouton B           |
| Haut            | Bouton X           |

Avec une seule Wiimote, Start/Coin sont uniquement sur la Wiimote (Flycast n'accepte qu'une touche par bouton).

#### MAME

| Wiimote                 | Fonction            |
| ----------------------- | ------------------- |
| B / A                   | Bouton 1 / Bouton 2 |
| Droite / Gauche         | Start / Coin        |
| Bas (une seule Wiimote) | Bouton 3            |

Deux Wiimotes : le joueur 2 utilise Haut/Bas pour Start/Coin.

#### ArcadeDuck

| Wiimote         | Fonction                                            |
| --------------- | --------------------------------------------------- |
| B / A           | Tir / Rechargement                                  |
| Droite / Gauche | Start / Coin                                        |
| Bas             | _Judge Dredd_ : arme secondaire (une seule Wiimote) |

Avec deux Wiimotes, l'arme secondaire de _Judge Dredd_ est sur **1** (mode 1) ou **+** (mode 2) pour le joueur 1, et sur **2** pour le joueur 2 (mode 1 uniquement).

#### PCSX2 arcade (pcsx2x6 : Namco System 246/256)

Start et Coin passent par les entrées de la borne : joueur 1 Droite/Gauche, joueur 2 Haut/Bas.

#### xemu (Chihiro)

| Wiimote      | Une Wiimote         | Deux Wiimotes                          |
| ------------ | ------------------- | -------------------------------------- |
| B            | Tir                 | Tir                                    |
| A            | Rechargement        | Pédale / changement                    |
| Start / Coin | Droite / Gauche     | J1 : Droite / Gauche – J2 : Haut / Bas |
| Bas          | Pédale / changement | –                                      |
| Haut         | Capteur de corps    | –                                      |

Avec deux Wiimotes, rechargez en visant hors de l'écran.

#### Lindbergh (Linuxloader)

| Wiimote                 | Une Wiimote             | Deux Wiimotes           |
| ----------------------- | ----------------------- | ----------------------- |
| B / A                   | Tir / Rechargement      | Tir / Rechargement      |
| Droite / Gauche         | Start (+ action) / Coin | Start (+ action) / Coin |
| Bas                     | Bouton du pistolet      | Coin J2                 |
| Haut                    | Pédale gauche           | Start J2                |
| 1 (mode 1) / + (mode 2) | Pédale droite           | Bouton du pistolet      |
| 2 (mode 1)              | –                       | Pédale gauche           |

Le pistolet du joueur 2 nécessite **UTILISER DEMULSHOOTER**.

#### Hypseus (jeux de tir Singe)

Start / Coin : joueur 1 Droite/Gauche, joueur 2 Haut/Bas. B tire, A est le second bouton du pistolet.

### Émulateurs console

Sur console, le pistolet a souvent sa propre croix directionnelle : la croix de la Wiimote reste alors une croix.

#### RetroArch (cores Libretro)

| Wiimote                 | Fonction                           |
| ----------------------- | ---------------------------------- |
| B / A                   | Tir / Rechargement (selon le core) |
| Droite / Gauche         | Gun Start / Gun Select             |
| Bas / Haut              | Aux A / Aux B                      |
| 1 (mode 1) / + (mode 2) | Aux C                              |

* Seul le **joueur 1** utilise les boutons de la Wiimote (RetroArch fusionne tous les claviers).
* **MAPPING DES BOUTONS A/B** : laissez la valeur par défaut (ou **MANETTE GAUCHE/DROITE**) pour avoir Aux A/B/C sur la croix.

#### Flycast (Dreamcast)

| Wiimote      | Mode 2             | Mode 1             |
| ------------ | ------------------ | ------------------ |
| B / A        | Tir / Rechargement | Tir / Rechargement |
| Croix        | Croix du pistolet  | Croix du pistolet  |
| Start        | **+**              | **1**              |
| Bouton A / B | **1** / **2**      | –                  |

{% hint style="danger" %}
Avec une seule Wiimote en mode 2, le bouton **−** ferme Flycast (Échap).
{% endhint %}

#### DuckStation (GunCon PlayStation)

| Wiimote          | Joueur 1                      | Joueur 2                      |
| ---------------- | ----------------------------- | ----------------------------- |
| B                | Tir                           | Tir                           |
| A                | Tir hors écran (rechargement) | Tir hors écran (rechargement) |
| GunCon A (Start) | Droite                        | Haut                          |
| GunCon B         | Gauche                        | Bas                           |

L'option **MAPPING DES BOUTONS A/B** remplace cette disposition si elle est réglée.

#### PCSX2 (GunCon 2 PlayStation 2)

| Wiimote         | Fonction           |
| --------------- | ------------------ |
| B / A           | Tir / Rechargement |
| Droite / Gauche | Start / Select     |
| Bas / Haut      | GunCon 2 A / B     |

L'option **MAPPING DES BOUTONS GUNCON** remplace cette disposition si elle est réglée.

#### Xbox (Cxbx-Reloaded, EMS TopGun)

| Wiimote | Mode 2            | Mode 1            |
| ------- | ----------------- | ----------------- |
| B / A   | Gâchette / Grip   | Gâchette / Grip   |
| Croix   | Stick du pistolet | Stick du pistolet |
| Start   | **+**             | **1**             |
| Back    | Clavier 5         | **2**             |

#### BizHawk

| Système (pistolet)           | Droite | Gauche | Bas     |
| ---------------------------- | ------ | ------ | ------- |
| NES (Zapper)                 | Start  | Select | –       |
| SNES (Super Scope)           | Pause  | –      | Curseur |
| Saturn (Stunner)             | Start  | –      | –       |
| Master System (Light Phaser) | Pause  | –      | –       |

#### Jgenesis

| Système (pistolet) | Droite | Gauche | Bas             | A              |
| ------------------ | ------ | ------ | --------------- | -------------- |
| NES (Zapper)       | Start  | Select | –               | Tir hors écran |
| SNES (Super Scope) | Pause  | –      | Turbo (bascule) | Curseur        |

#### Snes9x

| Pistolet    | Droite | Bas             | A       |
| ----------- | ------ | --------------- | ------- |
| Super Scope | Pause  | Turbo (bascule) | Curseur |
| Justifier   | Start  | –               | Start   |

### Dépannage

<table><thead><tr><th width="264">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Start/Coin ne répondent pas</td><td>Vérifiez les LEDs de la Wiimote (mode 2 : 1 + 4, mode 1 : 1 + 2) et l'option <strong>WIIMOTE CONNECTION MODE</strong>.</td></tr><tr><td>La croix lance/met en pause la musique</td><td>La DolphinBar est en mode 1 Multimédia (LEDs 1 + 3) : appuyez sur <strong>Home + croix Bas</strong>.</td></tr><tr><td>Le volume du PC change</td><td>Normal en mode 2 en appuyant sur <strong>1</strong> ou <strong>2</strong>.</td></tr><tr><td>Le menu Démarrer de Windows s'ouvre</td><td><strong>Home</strong> a été pressé : il agit comme la touche Windows.</td></tr><tr><td>L'émulateur se ferme en appuyant sur <strong>−</strong></td><td>Le mode 2 envoie Échap sur <strong>−</strong>. Évitez ce bouton ou passez en mode 1.</td></tr><tr><td>La gâchette recharge au lieu de tirer</td><td>Certaines configurations (Nunchuk, Wii Zapper) inversent les clics : activez <strong>INVERT TRIGGER/RELOAD</strong>.</td></tr><tr><td>Joueurs 1 et 2 inversés (TeknoParrot)</td><td>Activez <strong>WIIMOTE FIX ASSOCIATION</strong>.</td></tr><tr><td>Croix Droite déplace aussi le personnage</td><td>Le clavier est configuré comme manette du joueur 1 : utilisez une manette en joueur 1.</td></tr></tbody></table>
