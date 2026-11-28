# Quake

<div align="left"><figure><img src="../../../.gitbook/assets/image (807).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**Quake** (id Software, 1996) est le premier jeu de tir à la première personne entièrement en 3D d'id Software. Il a lancé le jeu en ligne et une très grande scène de mods, encore active aujourd'hui.

Ce système lance **Quake**, ses deux packs de mission officiels (**Scourge of Armagon** et **Dissolution of Eternity**), **Dimension of the Past** et les mods (cartes, épisodes, conversions comme **Quoth**).

RetroBat propose le core libretro **tyrquake** (par défaut) et **vkQuake**, un moteur moderne en Vulkan.

Les fichiers du jeu ne sont pas fournis : utilisez ceux de votre propre exemplaire.

{% embed url="https://docs.libretro.com/library/tyrquake/" %}

{% embed url="https://github.com/Novum/vkQuake" %}

## En bref

<table><thead><tr><th width="304"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\quake</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pak .quake</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: tyrquake</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (core tyrquake : 3 dispositions ; vkQuake : manette du joueur 1)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu (vkQuake : sauvegarde / chargement rapide aux raccourcis)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="178.25">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: tyrquake</strong> (défaut)</td><td>Léger, rendu fidèle, trois dispositions de manette, raccourcis de RetroArch.</td><td>Pas de sauvegardes instantanées. Rendu proche de l'original (résolution interne jusqu'à 1920x1200).</td></tr><tr><td><strong>vkquake</strong></td><td>Moteur moderne (Vulkan) : haute résolution, fréquence d'affichage de l'écran, effets améliorés, compatible avec les gros mods récents. Sauvegarde et chargement rapides aux raccourcis.</td><td>Un seul joueur à la manette.</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire. Il faut en revanche les fichiers du jeu :

<table><thead><tr><th width="375.75">Jeu</th><th width="119.75">Dossier</th><th>Fichiers</th></tr></thead><tbody><tr><td>Quake</td><td><code>id1</code></td><td><code>pak0.pak</code>, <code>pak1.pak</code> (<code>pak0.pak</code> seul = version shareware)</td></tr><tr><td>Scourge of Armagon (pack de mission 1)</td><td><code>hipnotic</code></td><td><code>pak0.pak</code></td></tr><tr><td>Dissolution of Eternity (pack de mission 2)</td><td><code>rogue</code></td><td><code>pak0.pak</code></td></tr><tr><td>Dimension of the Past</td><td><code>dopa</code></td><td><code>pak0.pak</code></td></tr></tbody></table>

Les versions vendues aujourd'hui (Steam, GOG) contiennent ces fichiers.

## Quel format de jeu ?

<table><thead><tr><th width="129">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.pak</strong></td><td>Fichier de données du jeu. Le jeu lancé est celui du dossier du fichier (<code>id1</code>, <code>hipnotic</code>, <code>rogue</code>, mod…).</td></tr><tr><td><strong>.quake</strong></td><td>Fichier de lancement placé dans <code>roms\quake</code> : il indique le dossier du jeu à lancer (voir <a href="quake.md#fichiers-de-lancement-.quake"><strong>Guides</strong></a>).</td></tr></tbody></table>

Organisation conseillée de `roms\quake` : le jeu de base dans `id1`, chaque pack de mission ou mod dans son propre dossier, à côté.

```
roms\quake\
├── id1\
│   ├── pak0.pak
│   ├── pak1.pak
│   └── music\
│       ├── track02.ogg
│       └── ...
├── hipnotic\
│   ├── pak0.pak
│   └── music\
├── rogue\
│   ├── pak0.pak
│   └── music\
├── dopa\
│   └── pak0.pak
├── Quake.quake
└── Scourge of Armagon.quake
```

La musique (pistes du CD) se place en `.ogg` dans le dossier `music` de chaque jeu (`track02.ogg`, `track03.ogg`…).

## Contrôles

### Configuration automatique

**Core tyrquake** : **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit la disposition. Dans les trois dispositions manette, le stick gauche sert à se déplacer et le stick droit à regarder.

| Action                | MANETTE CLASSIQUE (défaut) | MANETTE CLASSIQUE ALT. | MANETTE MODERNE   |
| --------------------- | -------------------------- | ---------------------- | ----------------- |
| Tirer                 | OUEST                      | R1                     | R2                |
| Sauter                | SUD                        | L1                     | L2                |
| Arme suivante         | EST                        | R2                     | R1                |
| Arme précédente       | —                          | R3                     | L1                |
| Croix gauche / droite | Tourner                    | Pas de côté            | Pas de côté       |
| Croix haut / bas      | Avancer / reculer          | Avancer / reculer      | Avancer / reculer |
| Menu                  | START                      | START                  | START             |

CLAVIER ET SOURIS joue au clavier et à la souris : RetroBat donne alors tout le clavier au jeu et capture la souris. La touche `Arrêt défil` rend le clavier aux raccourcis de RetroArch.



**vkQuake** : RetroBat donne au jeu la manette du joueur 1 (vkQuake ne lit qu'une manette). Commandes par défaut :

<table><thead><tr><th width="262.75">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Avancer, reculer, pas de côté</td></tr><tr><td>Stick droit</td><td>Regarder</td></tr><tr><td>R2</td><td>Tirer</td></tr><tr><td>L2</td><td>Sauter</td></tr><tr><td>L1 / R1</td><td>Arme précédente / arme suivante</td></tr><tr><td>START</td><td>Menu</td></tr><tr><td>SELECT</td><td>Scores</td></tr><tr><td>SUD / EST</td><td>Valider / retour (menus)</td></tr></tbody></table>

Les commandes se changent dans les options du menu de vkQuake. **CONTRÔLES > INVERSER L'AXE Y** inverse le regard haut / bas.

### Raccourcis

* **Core tyrquake** : raccourcis de RetroArch (avance rapide, captures…), sans sauvegardes instantanées : sauvegardez depuis le menu du jeu.
* **vkQuake** :

<table><thead><tr><th width="265.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarde rapide</td></tr><tr><td>HOTKEY + NORD</td><td>Chargement rapide</td></tr><tr><td>HOTKEY + R3</td><td>Capture d'écran</td></tr></tbody></table>

Pour plus de détails, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

| Contenu                                                         | Dossier                                                                                                |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Jeux et mods                                                    | `roms\quake`                                                                                           |
| Core tyrquake : sauvegardes et configuration                    | <p><code>saves\quake\&#x3C;dossier du jeu></code></p><p>(par exemple <code>saves\quake\id1</code>)</p> |
| vkQuake : sauvegardes, configuration du jeu et captures d'écran | `roms\quake\<dossier du jeu>`                                                                          |
| vkQuake : configuration vidéo                                   | `roms\quake\vkQuake.cfg`                                                                               |

`roms\quake\id1\retrobat.cfg` est réécrit par RetroBat à chaque lancement de vkQuake : ne le modifiez pas.

## Guides

### Lancer un pack de mission ou un mod

Lancez un fichier `.pak` du dossier du jeu (par exemple `hipnotic\pak0.pak`) : RetroBat lance le jeu de ce dossier. `hipnotic`, `rogue` et `quoth` sont lancés comme packs de mission (barre d'état adaptée), tout autre dossier comme un mod, par-dessus Quake.

Un mod sans fichier `.pak` (fichiers seuls) se lance avec un fichier `.quake`.

### Fichiers de lancement (.quake)

Un fichier `.quake` est un fichier texte placé dans `roms\quake`. Il apparaît dans la liste des jeux avec son nom.

* Sa première ligne donne le dossier du jeu, par exemple `hipnotic`.
* Si le fichier est vide, RetroBat lance le dossier qui porte le même nom que le fichier (`dopa.quake` lance `dopa`).
* Les anciens fichiers de RetroBat continuent de fonctionner (nom contenant `scourge` ou `hipnotic` : Scourge of Armagon ; `dissolution` ou `rogue` : Dissolution of Eternity ; sinon Quake).

<div align="left"><figure><img src="../../../.gitbook/assets/image (806).png" alt=""><figcaption></figcaption></figure></div>

Avec des fichiers `.quake`, les `.pak` des sous-dossiers apparaissent aussi dans la liste : vous pouvez les masquer dans ES.

## Problèmes connus

| Problème                                                      | Solution                                                                                                          |
| ------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Les touches du clavier ne répondent pas avec le core tyrquake | Choisissez **CONTRÔLES > TYPE DE CONTRÔLEUR > CLAVIER ET SOURIS**.                                                |
| vkQuake ignore certains réglages (résolution, VSync)          | Le moteur limite sa ligne de commande à 255 caractères : installez RetroBat dans un dossier au chemin plus court. |
| Pas de musique                                                | Placez les pistes en `.ogg` dans le dossier `music` du jeu.                                                       |
| Avec plusieurs manettes, vkQuake prend la mauvaise            | Deux manettes du même modèle ne se distinguent pas : vkQuake prend la première trouvée.                           |
