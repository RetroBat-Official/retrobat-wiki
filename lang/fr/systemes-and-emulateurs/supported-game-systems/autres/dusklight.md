# Dusklight

<div align="left"><figure><img src="../../../.gitbook/assets/image (537).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

**Dusklight** est un portage PC de **The Legend of Zelda: Twilight Princess**, sorti fin 2006 sur GameCube et sur Wii. Ce n'est pas un émulateur : le jeu a été reconstruit à partir du travail de décompilation de la version GameCube et tourne directement sur le PC.

Le portage reste fidèle au jeu d'origine et ajoute des options modernes : haute résolution, écran large, fréquence d'images plus élevée, améliorations de confort (transformation rapide, sauvegarde automatique, escalade plus rapide…), visée gyroscopique, packs de textures et mods.

Dusklight ne contient aucune donnée du jeu : il faut fournir l'image disque de votre propre exemplaire.

{% embed url="https://github.com/TwilitRealm/dusklight" %}

{% embed url="https://twilitrealm.dev/" %}

## En bref

<table><thead><tr><th width="259"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\dusklight</code></td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .iso .rvz</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>dusklight</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (image disque du jeu original à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

Dusklight est le seul programme proposé pour ce système.

Pour jouer à Twilight Princess avec un émulateur, voir les pages [**GameCube**](../consoles-de-jeu/nintendo-consoles-de-jeu/gamecube.md) et [**Wii**](../consoles-de-jeu/nintendo-consoles-de-jeu/wii.md).

## Versions du jeu reconnues

<table><thead><tr><th width="207">Version</th><th width="158.75">Identifiant</th><th>Langues</th></tr></thead><tbody><tr><td>GameCube Europe</td><td>GZ2P01</td><td>Anglais, français, allemand, espagnol, italien</td></tr><tr><td>GameCube USA</td><td>GZ2E01</td><td>Anglais</td></tr><tr><td>GameCube Japon</td><td>GZ2J01</td><td>Japonais</td></tr><tr><td>Wii Europe</td><td>RZDP01</td><td>Anglais, français, allemand, espagnol, italien</td></tr><tr><td>Wii USA</td><td>RZDE01</td><td>Anglais (et français, espagnol selon la révision du disque)</td></tr><tr><td>Wii Japon</td><td>RZDJ01</td><td>Japonais</td></tr></tbody></table>

La version Wii coréenne n'est pas prise en charge.

Même avec un disque Wii, Dusklight affiche l'interface de la version GameCube.

### Langue du jeu

La langue se choisit avec l'option **ÉMULATION > LANGUE**. Les langues disponibles dépendent du disque : pour jouer en français, utilisez une version européenne.

## Quel format de jeu ?

<table><thead><tr><th width="136.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.rvz</strong></td><td>Image compressée, plus légère. Dolphin sait convertir un <code>.iso</code> en <code>.rvz</code>.</td></tr><tr><td>.iso</td><td>Image complète.</td></tr><tr><td>.m3u</td><td>Fichier texte qui donne le chemin de l'image disque. Évite de copier le jeu s'il est déjà dans <code>roms\gamecube</code> ou <code>roms\wii</code> (voir <a href="dusklight.md#utiliser-un-jeu-deja-present-dans-gamecube-ou-wii">Guides</a>).</td></tr></tbody></table>

## Contrôles

### Configuration automatique

RetroBat attribue automatiquement les manettes aux ports 1 à 4 du jeu, dans l'ordre des joueurs de RetroBat. Les boutons sont ceux prévus par Dusklight, selon le type de manette :

| Manette GameCube     | Manette Xbox         | Autres manettes (PlayStation, Switch Pro…) |
| -------------------- | -------------------- | ------------------------------------------ |
| A                    | SUD                  | SUD                                        |
| B                    | OUEST                | EST                                        |
| X                    | EST                  | OUEST                                      |
| Y                    | NORD                 | NORD                                       |
| Z                    | R1                   | R1                                         |
| L / R                | L2 / R2              | L2 / R2                                    |
| START                | START                | START                                      |
| Stick de contrôle    | Stick gauche         | Stick gauche                               |
| Stick C              | Stick droit          | Stick droit                                |
| Croix directionnelle | Croix directionnelle | Croix directionnelle                       |

Le bouton **SELECT** ouvre le menu de Dusklight. Vous pouvez y modifier les boutons, gérer les mods et régler le jeu. Dans ce menu, **A** valide et **B** revient en arrière (boutons GameCube du tableau).

<div align="left"><figure><img src="../../../.gitbook/assets/image (538).png" alt=""><figcaption></figcaption></figure></div>

Deux options utiles dans **CONTRÔLES** : **CAMÉRA LIBRE** (caméra au stick droit) et **VISÉE GYROSCOPIQUE** (visée en bougeant une manette DualSense, DualShock 4, Switch Pro…).

Pour que RetroBat ne touche pas à l'attribution des manettes, désactivez **AUTOCONFIGURER LES MANETTES**.

### Raccourcis

<table><thead><tr><th width="227.75">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td>SELECT ou F1</td><td>Menu de Dusklight</td></tr><tr><td>F11</td><td>Plein écran / fenêtré</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="315.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes et réglages</td><td><code>emulators\dusklight\data</code></td></tr><tr><td>Fichier de réglages</td><td><code>emulators\dusklight\data\config.json</code></td></tr><tr><td>Attribution des manettes aux ports</td><td><code>emulators\dusklight\data\controller_ports.dat</code></td></tr><tr><td>Mods communs à tous les jeux</td><td><code>emulators\dusklight\data\mods</code></td></tr><tr><td>Mods d'un seul jeu</td><td><code>roms\dusklight\&#x3C;nom du jeu></code> (dossier du même nom que le fichier lancé)</td></tr><tr><td>Packs de textures</td><td><code>emulators\dusklight\data\texture_replacements</code></td></tr></tbody></table>

## Guides

### Utiliser un jeu déjà présent dans GameCube ou Wii

Inutile de copier l'image disque une deuxième fois.

1. Dans `roms\dusklight`, créez un fichier texte, par exemple `Twilight Princess.m3u`.
2. Écrivez-y le chemin complet de l'image disque :

```
D:\RetroBat\roms\gamecube\Zelda Twilight Princess (Europe).rvz
```

3. Lancez le fichier `.m3u` depuis RetroBat.

### Jeu d'origine ou jeu amélioré ?

L'option **ÉMULATION > AMÉLIORATIONS** règle d'un coup les améliorations de confort :

<table><thead><tr><th width="257.75">Choix</th><th>Effet</th></tr></thead><tbody><tr><td><strong>DUSKLIGHT (RECOMMANDÉ)</strong></td><td>Transformation rapide, bourses plus grandes, escalade rapide, sauvegardes instantanées, sauvegarde automatique, cartes améliorées…</td></tr><tr><td><strong>CLASSIQUE (GAMECUBE)</strong></td><td>Le jeu se comporte comme sur GameCube.</td></tr><tr><td>Non réglé</td><td>Les réglages faits dans le menu de Dusklight sont conservés.</td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (539).png" alt=""><figcaption></figcaption></figure></div>

L'option **MODE MIROIR** inverse le monde de gauche à droite, comme dans la version Wii.

### Mods

Les mods sont des fichiers `.dusk`. Un mod présent dans le dossier de mods est chargé et activé automatiquement au lancement.

**Mods pour tous les jeux** : copiez les fichiers `.dusk` dans `emulators\dusklight\data\mods`.

**Mods pour un seul jeu** : dans `roms\dusklight`, créez un dossier portant le même nom que le fichier du jeu, sans l'extension, et copiez-y les fichiers `.dusk`. Quand ce dossier existe, RetroBat charge uniquement les mods qu'il contient.

Vous pouvez ainsi avoir plusieurs entrées dans RetroBat, chacune avec ses mods :

```
roms\dusklight\Twilight Princess.m3u
roms\dusklight\Twilight Princess Rando.m3u
roms\dusklight\Twilight Princess Rando\randomizer.dusk
```

Ici, `Twilight Princess` se lance avec les mods communs et `Twilight Princess Rando` avec le mod de son dossier.

**Jouer sans mods** : désactivez l'option **ÉMULATION > ACTIVER LES MODS**.

Pour désactiver un seul mod, ou en installer depuis le catalogue, ouvrez le menu de Dusklight (**SELECT**). Un mod installé depuis ce menu va dans le dossier de mods utilisé par le jeu lancé.

## Problèmes connus

<table><thead><tr><th width="325.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Dusklight ne reconnaît pas le jeu</td><td>Utilisez une image non modifiée d'une des versions reconnues (voir <a href="dusklight.md#versions-du-jeu-reconnues">versions reconnues</a>). La version Wii coréenne ne fonctionne pas.</td></tr><tr><td>Le jeu est en anglais, le français n'est pas proposé</td><td>La langue dépend du disque : utilisez une version européenne, puis choisissez <strong>LANGUE</strong>.</td></tr><tr><td>Le fichier <code>.m3u</code> ne se lance pas</td><td>Le fichier doit contenir le chemin complet de l'image disque, sur la première ligne.</td></tr><tr><td>Un menu s'ouvre quand j'appuie sur SELECT</td><td>C'est le menu de Dusklight. Fermez-le avec le bouton <strong>B</strong> de la manette GameCube (voir <a href="dusklight.md#controles">Contrôles</a>).</td></tr><tr><td>Les boutons B et X ne sont pas où je veux</td><td>Changez-les dans le menu de Dusklight (<strong>SELECT</strong>).</td></tr><tr><td>Un mod reste actif alors que <strong>ACTIVER LES MODS</strong> est désactivé</td><td>Les mods placés dans <code>emulators\dusklight\mods</code> sont toujours chargés. Déplacez-les dans <code>emulators\dusklight\data\mods</code>.</td></tr><tr><td>Écran noir ou plantage au lancement</td><td>Dusklight demande une carte graphique compatible Direct3D 12 ou Vulkan. Essayez <strong>PILOTES > VIDÉO</strong> : DIRECT3D 11.</td></tr></tbody></table>

##

<table><thead><tr><th width="295.25">Version</th><th>SHA-1 hash</th></tr></thead><tbody><tr><td>GameCube USA</td><td><code>75edd3ddff41f125d1b4ce1a40378f1b565519e7</code></td></tr><tr><td>GameCube EUR</td><td><code>2601822a488eeb86fb89db16ca8f29c2c953e1ca</code></td></tr></tbody></table>
