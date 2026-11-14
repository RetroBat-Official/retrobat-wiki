# Configuration des touches Keisho

## Présentation

Cette page explique comment changer les boutons de **Keisho** (anciennement sm2-emu), l'émulateur des systèmes [**Sega Model 1**](../../systemes-and-emulateurs/supported-game-systems/arcade/sega/sega-model-1.md), [**Sega Model 2**](../../systemes-and-emulateurs/supported-game-systems/arcade/sega/sega-model-2.md) et [**Sega Model 3**](../../systemes-and-emulateurs/supported-game-systems/arcade/sega/sega-model-3.md).

À chaque lancement, RetroBat écrit la configuration des manettes dans `emulators\keisho\keisho.ini`, à partir de deux fichiers :

<table><thead><tr><th width="206.5">Fichier</th><th>Contenu</th></tr></thead><tbody><tr><td><code>keisho.yml</code></td><td>Boutons de la manette, par jeu et par disposition</td></tr><tr><td><code>keisho_wheels.yml</code></td><td>Boutons du volant, par type de volant</td></tr></tbody></table>

Les deux fichiers sont fournis dans `system\resources\inputmapping` (et `wheels` pour le volant). Pour les modifier, copiez-les dans `user\inputmapping` : votre copie est alors utilisée à la place du fichier de RetroBat.

{% hint style="warning" %}
Les dispositions par jeu enregistrées dans le menu de Keisho (**Controls > Gamepad**) sont effacées à chaque lancement, pour que celle de RetroBat s'applique. Pour garder les vôtres, utilisez `keisho.yml`, ou désactivez **AUTOCONFIGURER LES MANETTES**.
{% endhint %}

## Configuration automatique

Sans modifier aucun fichier, RetroBat règle Keisho ainsi pour les joueurs 1 et 2 :

<table><thead><tr><th width="274">Commande</th><th>Manette</th></tr></thead><tbody><tr><td>Directions</td><td>Croix directionnelle et stick gauche</td></tr><tr><td>Start, pièce</td><td>START, SELECT</td></tr><tr><td>Rapport inférieur / supérieur</td><td>L1 / R1</td></tr><tr><td>Direction, visée</td><td>Stick gauche (visée : l'un ou l'autre stick)</td></tr><tr><td>Accélérateur, frein</td><td>R2, L2</td></tr><tr><td>Service, Test</td><td>L3, R3 (clavier : 9, 0)</td></tr><tr><td>Boutons 1 à 4</td><td>Selon le jeu, voir <code>keisho.yml</code></td></tr></tbody></table>

Les options du sous-menu **CONTRÔLES** (zone morte du stick, vibrations) et **DISPOSITION DES BOUTONS** (sticks arcade) s'appliquent aussi. Avec **AUTOCONFIGURER LES MANETTES** désactivé, RetroBat ne touche plus aux manettes : Keisho garde les réglages de son menu.

## Le fichier keisho.yml

### Ordre de recherche

Le fichier contient des conteneurs. RetroBat utilise le premier trouvé, dans cet ordre :

1. avec une **DISPOSITION DES BOUTONS** choisie : `<jeu>_<disposition>`, puis `<famille>_<disposition>`, puis `default_<disposition>` ;
2. puis `<jeu>`, `<famille>`, `default`.

* `<jeu>` est le nom du romset (`vf2a`), `<famille>` celui de son jeu parent (`vf2`) : un conteneur de jeu parent sert donc à tous ses clones.
* `<disposition>` vaut `modern8`, `8alternative` ou `6alternative` (CLASSIQUE 8 BOUTONS utilise `6alternative`).
* Une disposition de sticks arcade choisie par l'utilisateur passe avant la disposition manette du jeu.

### Clés et valeurs

La **clé** est la position du bouton sur la manette :

<table><thead><tr><th width="281.5">Clé</th><th>Bouton</th></tr></thead><tbody><tr><td><code>south</code>, <code>east</code>, <code>west</code>, <code>north</code></td><td>SUD, EST, OUEST, NORD</td></tr><tr><td><code>l1</code>, <code>r1</code>, <code>l2</code>, <code>r2</code></td><td>Gâchettes</td></tr><tr><td><code>l3</code>, <code>r3</code></td><td>Clic des sticks</td></tr><tr><td><code>select</code>, <code>start</code></td><td>SELECT, START</td></tr><tr><td><code>up</code>, <code>down</code>, <code>left</code>, <code>right</code></td><td>Croix directionnelle</td></tr></tbody></table>

La **valeur** est la commande de Keisho : `Button1` à `Button4`, `Up`, `Down`, `Left`, `Right`, `Start`, `Coin`, `GearUp`, `GearDown`.

* Un bouton peut piloter plusieurs commandes, séparées par une virgule : `west: Button1, Coin`.
* Une commande n'est pilotée que par un seul bouton : si elle est listée deux fois, la première l'emporte.
* Les commandes absentes du conteneur gardent leur bouton par défaut (directions, Start, pièce, rapports). Les boutons 1 à 4 non listés n'ont pas de bouton.

Exemple, Virtua Fighter 2 avec la garde sur EST :

```yaml
vf2:
  west: Button1
  north: Button2
  east: Button3
```

### Ce que représentent Button1 à Button4

| Jeux                                                                    | Button1             | Button2                        | Button3    | Button4   |
| ----------------------------------------------------------------------- | ------------------- | ------------------------------ | ---------- | --------- |
| Virtua Fighter, Virtua Fighter 2, Last Bronx, Fighting Vipers (Model 2) | Punch               | Kick                           | Guard      | (Guard 2) |
| Dead or Alive                                                           | Hold                | Punch                          | Kick       | —         |
| Sonic the Fighters                                                      | Punch               | Kick                           | Barrier    | —         |
| Virtua Fighter 3, Fighting Vipers 2                                     | Punch               | Kick                           | Guard      | Escape    |
| Spikeout                                                                | Beat                | Charge                         | Shift      | Jump      |
| Virtua Striker, Virtua Striker 2                                        | Long Pass           | Shoot                          | Short Pass | —         |
| Dynamite Cop                                                            | Punch               | Kick                           | Jump       | —         |
| Pilot Kids, Zero Gunner                                                 | Shot                | Bomb                           | —          | —         |
| Jeux au pistolet                                                        | Tir (aussi R2)      | Recharger / missile (aussi L2) | —          | —         |
| Jeux de course                                                          | VR1                 | VR2                            | VR3        | VR4       |
| Harley-Davidson                                                         | Choix de la musique | Vue                            | —          | —         |
| Star Wars Arcade                                                        | Laser               | Torpille                       | —          | —         |
| Star Wars Trilogy                                                       | Événement 1         | Événement 2                    | —          | —         |
| Sega Bass Fishing                                                       | Lancer              | Select                         | —          | —         |
| Magical Truck Adventure                                                 | Pédale              | —                              | —          | —         |

Les dispositions fournies par RetroBat sont décrites sur les pages [**Sega Model 1**](../../systemes-and-emulateurs/supported-game-systems/arcade/sega/sega-model-1.md), [**Sega Model 2**](../../systemes-and-emulateurs/supported-game-systems/arcade/sega/sega-model-2.md) et [**Sega Model 3**](../../systemes-and-emulateurs/supported-game-systems/arcade/sega/sega-model-3.md). Pour Virtua Fighter 3, Fighting Vipers 2 et Spikeout, elles sont les mêmes que dans `supermodel.yml` (Supermodel).

### Limites

Certaines commandes ne se règlent pas dans `keisho.yml` :

* les boutons de vue (VR1 à VR4) des jeux de course sont toujours les boutons 1 à 4 ;
* Virtual On, Virtual On 2, Desert Tank, Sky Target, Ski Super G, Water Ski et Ski Champ ont une disposition propre à Keisho ;
* Star Wars Trilogy tire avec les gâchettes (Keisho y déplace les commandes Up / Down) ; Sega Bass Fishing utilise les gâchettes pour le moulinet et la tension du fil ;
* les axes (direction, visée, pédales) sont détectés par Keisho.

Pour plus de détails sur les dispositions arcade, voir la page [**Le Guide Arcade**](../../systemes-and-emulateurs/arcade-guide.md).

## Le fichier keisho\_wheels.yml (volants)

Avec **VOLANTS DE COURSE > ACTIVER LES VOLANTS**, RetroBat règle les boutons du volant d'après `system\resources\inputmapping\wheels\keisho_wheels.yml` (copie modifiable : `user\inputmapping\keisho_wheels.yml`).

* Chaque conteneur porte le nom d'un type de volant reconnu par RetroBat : `LogitechG29`, `LogitechG920`, `LogitechG923PS`, `LogitechG923X`, `LogitechDrivingForceGT`, `ThrustmasterT300RSPS3`, `MozaR5`.
* La **clé** est la commande : `Start`, `Coin`, `Button1` à `Button4` (aussi VR1 à VR4), `GearUp`, `GearDown`, `Test`, `Service`, `Menu`, `Gear1` à `Gear4`, `GearNeutral`.
* La **valeur** est le numéro du bouton du volant (ordre DirectInput, le premier bouton vaut 0) ; `-1` laisse la commande sans bouton.
* `Gear1` à `Gear4` sont les positions du levier en H ; elles ne sont pas écrites avec l'option **DÉSACTIVER LE LEVIER DE VITESSE**.
* La direction et les pédales sont toujours détectées par Keisho ; calibrez-les dans son menu si besoin.
* Un volant sans conteneur garde les boutons réglés dans le menu de Keisho (**Controls > Wheel**).

Exemple :

```yaml
LogitechG29:
  Start: 9
  Coin: 8
  Button1: 0
  Button2: 2
  Button3: 1
  Button4: 3
  GearUp: 4
  GearDown: 5
```

Pour la liste des types de volants, voir la page [**Volants**](../supported-controllers/volants.md).

## Problèmes connus

<table><thead><tr><th width="317.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Mes changements dans <code>keisho.yml</code> n'ont pas d'effet</td><td>Vérifiez que le fichier est dans <code>user\inputmapping</code>, le nom du conteneur (romset ou jeu parent) et la <strong>DISPOSITION DES BOUTONS</strong> choisie (un conteneur <code>_&#x3C;disposition></code> passe avant).</td></tr><tr><td>La disposition réglée dans le menu de Keisho est perdue</td><td>RetroBat l'efface à chaque lancement : utilisez <code>keisho.yml</code>, ou désactivez <strong>AUTOCONFIGURER LES MANETTES</strong>.</td></tr><tr><td>Un bouton ne fait rien</td><td>Une même commande ne peut être que sur un seul bouton : vérifiez qu'elle n'est pas déjà listée plus haut dans le conteneur.</td></tr></tbody></table>
