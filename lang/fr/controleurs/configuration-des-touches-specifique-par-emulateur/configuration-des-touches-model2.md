# Configuration des touches m2emulator

## Présentation

Cette page explique comment régler soi-même les contrôles de **m2emulator**, l'émulateur Model 2 par défaut de RetroBat. Pour les autres émulateurs Model 2 (Keisho, Supermodel, MAME), voir la page [**Sega Model 2**](../../systemes-and-emulateurs/supported-game-systems/arcade/sega/sega-model-2.md).

m2emulator enregistre les touches de chaque jeu dans un fichier `.input` du dossier `emulators\m2emulator\CFG`. RetroBat propose trois façons de le remplir :

<table><thead><tr><th width="162">Méthode</th><th width="373">Pour qui</th><th>Fichier</th></tr></thead><tbody><tr><td><strong>Configuration automatique</strong> (défaut)</td><td>La plupart des joueurs : RetroBat écrit les touches de chaque jeu à chaque lancement.</td><td>—</td></tr><tr><td><strong>Mapping par jeu</strong></td><td>Changer l'emplacement des boutons d'un jeu de combat ou d'un jeu « standard », en gardant la configuration automatique.</td><td><code>model2.yml</code></td></tr><tr><td><strong>Modèles</strong></td><td>Utiliser sa propre configuration, faite dans m2emulator, pour un jeu précis.</td><td><code>templatescfg\&#x3C;pilote>\&#x3C;jeu>.input</code></td></tr></tbody></table>

Les volants ont leur propre fichier, `model2_wheels.yml` (voir [**Volants**](configuration-des-touches-model2.md#volants-model2_wheels.yml) plus bas).

## Configuration automatique

À chaque lancement, RetroBat écrit le fichier `.input` du jeu avec la disposition décrite sur la page **Sega Model 2** (contrôles par type de jeu). Les réglages se trouvent dans les options avancées du système, sous-menu **CONTRÔLES** :

| Option                                                                                       | Effet                                                                                                                                               |
| -------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **PILOTES > CONTRÔLEUR**                                                                     | XINPUT (défaut) pour les manettes Xbox et compatibles, DINPUT pour les autres. RetroBat passe aussi en DINPUT s'il ne trouve aucune manette XInput. |
| **DISPOSITION DES BOUTONS**                                                                  | Dispositions pour sticks arcade (modern8, 8alternative, 6alternative), pour les jeux de combat et les jeux « standards ».                           |
| **UTILISER R1/L1 POUR LES JEUX DE COURSE**                                                   | Accélérateur et frein sur R1 / L1 (boîte automatique seulement).                                                                                    |
| **INVERSER LES INDEX MANETTES**, **FORCER L'INDEX DE LA MANETTE DU JOUEUR 1** / **JOUEUR 2** | Choix des manettes de chaque joueur.                                                                                                                |

<div align="left"><figure><img src="../../.gitbook/assets/image (595).png" alt=""><figcaption></figcaption></figure></div>

RetroBat ne gère automatiquement que les jeux listés sur la page [**Sega Model 2**](../../systemes-and-emulateurs/supported-game-systems/arcade/sega/sega-model-2.md). Pour un autre jeu, il ne touche pas au fichier `.input` : réglez les touches une fois dans m2emulator (**Game > Configure Controls**, voir l'étape 1 des modèles), elles sont gardées.

Avec **AUTOCONFIGURER LES MANETTES** désactivé, RetroBat ne modifie aucun fichier `.input` (les pistolets restent configurés).

## Mapping par jeu (model2.yml)

Le fichier `model2.yml` change l'emplacement des boutons des jeux de combat et des jeux « standards », sans quitter la configuration automatique : RetroBat continue de gérer les directions, Start, pièce, Service et Test, le pilote et les index des manettes.

1. Copiez `system\resources\inputmapping\model2.yml` dans `user\inputmapping`. Votre copie est alors utilisée à la place du fichier de RetroBat.
2. Modifiez le conteneur du jeu, puis lancez le jeu : le fichier `.input` est réécrit avec vos boutons.

**Jeux concernés et actions disponibles** (les clones utilisent le conteneur de leur jeu parent) :

<table><thead><tr><th width="185.75">Jeu</th><th width="173.5">Conteneur</th><th>Actions</th></tr></thead><tbody><tr><td>Dead or Alive</td><td><code>doa</code></td><td>Hold, Punch, Kick</td></tr><tr><td>Fighting Vipers</td><td><code>fvipers</code></td><td>Punch, Kick, Guard, Guard 2</td></tr><tr><td>Last Bronx</td><td><code>lastbrnx</code></td><td>Punch, Kick, Guard</td></tr><tr><td>Sonic the Fighters</td><td><code>schamp</code></td><td>Punch, Kick, Barrier</td></tr><tr><td>Virtua Fighter 2</td><td><code>vf2</code></td><td>Punch, Kick, Guard</td></tr><tr><td>Dynamite Cop</td><td><code>dynamcop</code></td><td>Punch, Kick, Jump</td></tr><tr><td>Pilot Kids</td><td><code>pltkids</code></td><td>Shot, Bomb</td></tr><tr><td>Virtua Striker</td><td><code>vstriker</code></td><td>Short Pass, Long Pass, Shoot</td></tr><tr><td>Zero Gunner</td><td><code>zerogun</code></td><td>Shot, Bomb</td></tr></tbody></table>

**Conteneurs** : le conteneur porte le nom du jeu parent (`vf2`). On peut ajouter un conteneur par disposition, `<jeu>_modern8`, `<jeu>_8alternative` ou `<jeu>_6alternative`, utilisé quand cette **DISPOSITION DES BOUTONS** est choisie (CLASSIQUE 8 BOUTONS utilise `_6alternative`). RetroBat cherche `<jeu>_<disposition>`, puis `<jeu>` ; sans conteneur, il garde sa disposition par défaut.

**Valeurs** : la position du bouton sur la manette :

| Valeur                           | Bouton                       |
| -------------------------------- | ---------------------------- |
| `a`                              | SUD                          |
| `b`                              | EST                          |
| `x`                              | OUEST                        |
| `y`                              | NORD                         |
| `leftshoulder` / `rightshoulder` | L1 / R1                      |
| `leftstick` / `rightstick`       | clic du stick gauche / droit |
| `back` / `start`                 | SELECT / START               |

Une action absente du conteneur n'a pas de bouton.

Exemple, Virtua Fighter 2 avec la garde sur EST et le pied sur SUD :

```yaml
vf2:
  Guard: b
  Punch: x
  Kick: a
```

Pour plus de détails sur les dispositions arcade, voir la page [**Le Guide Arcade**](../../systemes-and-emulateurs/arcade-guide.md).

## Modèles (configuration faite dans m2emulator)

Cette méthode remplace la configuration automatique par un fichier préparé dans m2emulator. Elle s'applique à tous les jeux qui ont un modèle, sauf quand les pistolets sont activés.

### Étape 1 : créer la configuration du jeu

1. Dans les options avancées du système, choisissez le pilote de votre manette : **PILOTES > CONTRÔLEUR > XINPUT** (manettes Xbox et compatibles) ou **DINPUT** (les autres).

<div align="left"><figure><img src="../../.gitbook/assets/image (596).png" alt=""><figcaption></figcaption></figure></div>

2. Lancez le jeu, puis appuyez sur **ALT + ENTRÉE** pour quitter le plein écran et afficher le menu de m2emulator.
3. Ouvrez **Game > Configure Controls** et réglez les touches.

<div align="left"><figure><img src="../../.gitbook/assets/image (597).png" alt=""><figcaption></figcaption></figure></div>

4. Fermez la fenêtre et quittez l'émulateur : le fichier `<jeu>.input` est enregistré dans `emulators\m2emulator\CFG`.

<div align="left"><figure><img src="../../.gitbook/assets/image (598).png" alt=""><figcaption></figcaption></figure></div>

### Étape 2 : copier le fichier dans le dossier des modèles

Copiez le fichier dans le dossier du pilote choisi à l'étape 1 :

* `emulators\m2emulator\templatescfg\xinput` pour XINPUT ;
* `emulators\m2emulator\templatescfg\dinput` pour DINPUT.

<div align="left"><figure><img src="../../.gitbook/assets/image (599).png" alt=""><figcaption></figcaption></figure></div>

Le modèle doit porter **le nom du jeu parent** : `daytona.input` sert aussi pour `daytonas` ou `daytonam`. RetroBat fournit déjà des modèles pour les manettes XInput, et pour les manettes PlayStation 4 et 5 en DInput : vous pouvez les remplacer par les vôtres.

### Étape 3 : activer les modèles

Dans les options avancées du système, choisissez **CONTRÔLES > MÉTHODE DE CONFIGURATION DES CONTRÔLES > MODÈLES**. À chaque lancement, RetroBat copie le modèle du jeu dans `emulators\m2emulator\CFG`.

<div align="left"><figure><img src="../../.gitbook/assets/image (600).png" alt=""><figcaption></figcaption></figure></div>

## Volants (model2\_wheels.yml)

Avec **VOLANTS DE COURSE > ACTIVER LES VOLANTS**, RetroBat règle le volant d'après `system\resources\inputmapping\wheels\model2_wheels.yml`. Chaque conteneur porte le nom d'un type de volant reconnu par RetroBat (`LogitechG29`, `LogitechG920`, `LogitechG923PS`, `LogitechG923X`, `ThrustmasterT300RSPS3`…). Un conteneur `<volant>_<jeu>` (par exemple `LogitechG29_daytona`) est prioritaire pour un jeu.

<table><thead><tr><th width="331.5">Clé</th><th>Rôle</th></tr></thead><tbody><tr><td><code>Steer</code>, <code>Throttle</code>, <code>Brake</code></td><td>Axes du volant et des pédales : <code>axis0</code>, <code>axis1</code>… (<code>axisinv1</code> inverse l'axe)</td></tr><tr><td><code>Up</code>, <code>Down</code>, <code>Left</code>, <code>Right</code></td><td>Croix : <code>hatup</code>, <code>hatdown</code>…</td></tr><tr><td><code>ShiftUp</code>, <code>ShiftDown</code>, <code>Gear1</code> à <code>Gear4</code>, <code>GearN</code></td><td>Palettes et levier de vitesses : <code>button4</code>…</td></tr><tr><td><code>South</code>, <code>East</code>, <code>West</code>, <code>North</code>, <code>Start</code>, <code>Select</code>, <code>Service</code>, <code>Test</code></td><td>Boutons</td></tr><tr><td><code>DeportedShifter</code></td><td><code>true</code> seulement pour les Thrustmaster dont le levier de vitesses est vu comme un appareil séparé</td></tr></tbody></table>

Votre propre version se place dans `user\inputmapping\model2_wheels.yml` (prioritaire sur le fichier de RetroBat). Pour la liste des types de volants et les autres options, voir la page [**Volants**](../supported-controllers/volants.md).

## Problèmes connus

<table><thead><tr><th width="322.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Mon modèle n'est pas utilisé</td><td>Vérifiez le nom (celui du jeu parent), le dossier (celui du pilote choisi), l'option <strong>MODÈLES</strong>, et que les pistolets ne sont pas activés.</td></tr><tr><td>Mes boutons changent à chaque lancement</td><td>La configuration automatique réécrit le fichier <code>.input</code> : utilisez <code>model2.yml</code> ou les modèles, ou désactivez <strong>AUTOCONFIGURER LES MANETTES</strong>.</td></tr><tr><td><code>model2.yml</code> n'a aucun effet sur un jeu de course ou de tir</td><td>Le mapping par jeu ne concerne que les jeux de combat et les jeux « standards » <a href="configuration-des-touches-model2.md#mapping-par-jeu-model2.yml">listés plus haut</a>.</td></tr></tbody></table>
