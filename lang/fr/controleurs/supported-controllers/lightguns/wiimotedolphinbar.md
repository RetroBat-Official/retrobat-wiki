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
Pour la configuration en **mode 4** avec le logiciel WiimoteGun, voir WiimoteGun. La disposition de cette page ne s'applique pas au mode 4.
{% endhint %}

### Réglage de la DolphinBar

| Mode DolphinBar               | Comment le sélectionner                                  | LEDs de la Wiimote | Utilisation dans RetroBat                                     |
| ----------------------------- | -------------------------------------------------------- | ------------------ | ------------------------------------------------------------- |
| **Mode 2 – Jeu** (recommandé) | Maintenir **Home** + appuyer sur **croix Gauche**        | 1 + 4              | Pistolet (par défaut)                                         |
| Mode 1 – Normal               | Maintenir **Home** + appuyer sur **croix Bas**           | 1 + 2              | Pistolet                                                      |
| Mode 1 – Multimédia           | Appuyer à nouveau sur **Home** + **croix Bas** en mode 1 | 1 + 3              | ❌ Non pris en charge (la croix envoie des touches multimédia) |
| Mode 3 – Manette              | Maintenir **Home** + appuyer sur **croix Haut**          | 1 à 4              | ❌ Pas un pistolet                                             |
| Mode 4 – Émulateur Wii        | Maintenir **Home** + appuyer sur **croix Droite**        | 1 à 4              | WiimoteGun et Dolphin uniquement                              |

Le bouton **MODE** de la DolphinBar permet aussi de passer d'un mode à l'autre. Le mode choisi est mémorisé.

### Réglages dans RetroBat

Dans EmulationStation, ouvrez les options du système ou du jeu, puis **Options avancées → Guns** :

* **ENABLE GUN** (activer le pistolet) : ON.
* **WIIMOTE CONNECTION MODE** (mode de connexion de la Wiimote) : choisissez le mode de votre DolphinBar.
  * **MODE 2 (GAME)** : également utilisé si l'option n'est pas réglée.
  * **MODE 1 (NORMAL)** : à choisir si votre DolphinBar est en mode 1.
* **INVERT TRIGGER/RELOAD** (inverser tir/rechargement) : à activer si la gâchette recharge au lieu de tirer (voir Dépannage).

{% hint style="info" %}
Les noms des options peuvent différer légèrement selon la langue choisie dans EmulationStation.
{% endhint %}

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
* **Deux Wiimotes** : chaque Wiimote a sa propre disposition. Si les joueurs 1 et 2 sont inversés, activez **WIIMOTE FIX ASSOCIATION**.
* **COIN\START BUTTONS** réglé sur _ON KEYBOARD_ remet Start/Coin sur le clavier (1-4 / 5-8).

#### Model 2

Deux Wiimotes utilisent la disposition partagée (joueur 2 : Haut = Start, Bas = Coin). **FORCE KEYBOARD FOR START/COIN** remet Start/Coin sur le clavier uniquement.

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

Le pistolet du joueur 2 nécessite **DEMULSHOOTER**.

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
* **GUN A/B BUTTONS MAPPING** : laissez la valeur par défaut (ou _directions_) pour avoir Aux A/B/C sur la croix.

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

L'option **GUN A/B BUTTONS** remplace cette disposition si elle est réglée.

#### PCSX2 (GunCon 2 PlayStation 2)

| Wiimote         | Fonction           |
| --------------- | ------------------ |
| B / A           | Tir / Rechargement |
| Droite / Gauche | Start / Select     |
| Bas / Haut      | GunCon 2 A / B     |

L'option **GUN MAPPING** remplace cette disposition si elle est réglée.

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

| Problème                                   | Solution                                                                                                  |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------- |
| Start/Coin ne répondent pas                | Vérifiez les LEDs de la Wiimote (mode 2 : 1 + 4, mode 1 : 1 + 2) et l'option **WIIMOTE CONNECTION MODE**. |
| La croix lance/met en pause la musique     | La DolphinBar est en mode 1 Multimédia (LEDs 1 + 3) : appuyez sur **Home + croix Bas**.                   |
| Le volume du PC change                     | Normal en mode 2 en appuyant sur **1** ou **2**.                                                          |
| Le menu Démarrer de Windows s'ouvre        | **Home** a été pressé : il agit comme la touche Windows.                                                  |
| L'émulateur se ferme en appuyant sur **−** | Le mode 2 envoie Échap sur **−**. Évitez ce bouton ou passez en mode 1.                                   |
| La gâchette recharge au lieu de tirer      | Certaines configurations (Nunchuk, Wii Zapper) inversent les clics : activez **INVERT TRIGGER/RELOAD**.   |
| Joueurs 1 et 2 inversés (TeknoParrot)      | Activez **WIIMOTE FIX ASSOCIATION**.                                                                      |
| Croix Droite déplace aussi le personnage   | Le clavier est configuré comme manette du joueur 1 : utilisez une manette en joueur 1.                    |
