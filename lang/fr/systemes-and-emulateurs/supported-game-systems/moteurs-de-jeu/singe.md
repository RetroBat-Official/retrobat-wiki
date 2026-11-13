# Singe

<div align="left"><figure><img src="../../../.gitbook/assets/image (551).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**Singe** (Somewhat Interactive Nostalgic Game Engine) est un moteur de jeu créé par Scott Duensing pour compléter l'émulateur Daphne. Il sert à faire tourner des jeux vidéo filmés qui ne reposent pas sur la ROM d'une borne : le déroulement du jeu est décrit par un script, qui pilote la vidéo.

Singe a d'abord permis de rejouer aux jeux de tir d'**American Laser Games**, apparus en arcade en 1990 avec Mad Dog McCree, puis Who Shot Johnny Rock?, Crime Patrol ou Space Pirates. Il fait aussi tourner Time Gal, Ninja Hayate et de nombreux jeux adaptés par des passionnés.

Dans RetroBat, ces jeux se lancent avec **Hypseus Singe**, qui lit les jeux Singe et Singe 2, ou avec **Singe2**.

Les bornes LaserDisc classiques (Dragon's Lair, Space Ace…) sont sur la page [**LaserDisc**](../arcade/daphne-laserdisc.md).

## En bref

<table><thead><tr><th width="276.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\singe</code></td></tr><tr><td><strong>Extensions</strong></td><td>.hypseus .zip</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>hypseus</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs (joueur 1)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>Hypseus, Singe2</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="111.5">Émulateur</th><th width="166.25">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>hypseus</strong> (défaut)</td><td>Tout le monde</td><td>Lit les jeux au format zip et au format dossier. Manette configurée automatiquement, plusieurs pistolets, décorations.</td><td>—</td></tr><tr><td><strong>singe2</strong></td><td>Jeux proposés sur le site de Singe 2</td><td>L'émulateur de l'auteur de Singe.</td><td>Ne lit que les jeux de son site, dans leur propre format. Demande le mode développeur de Windows.</td></tr></tbody></table>

**En cas de doute, gardez hypseus.**

## BIOS

Aucun BIOS n'est nécessaire.

RetroBat fournit les fichiers `Framework.zip` et `FrameworkKimmy.zip` dans `roms\singe`. Ils servent aux jeux Singe 2 : ne les supprimez pas.

## Quel format de jeu ?

<table><thead><tr><th width="147.75">Format</th><th width="83">hypseus</th><th width="79.25">singe2</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.zip</strong></td><td>✔</td><td>✘</td><td>Méthode la plus simple : le jeu dans <code>roms\singe\roms</code>, les vidéos dans <code>roms\singe\vldp</code>.</td></tr><tr><td>Dossier .hypseus</td><td>✔</td><td>✔</td><td>Ancienne méthode pour Hypseus. Seul format pour Singe2, avec les jeux de son site.</td></tr></tbody></table>

Dans les deux cas, les fichiers vidéo (`.m2v`) et audio (`.ogg`) du jeu sont à fournir.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement la manette du joueur 1 pour les deux émulateurs.

**Hypseus**

<table><thead><tr><th width="177">Action</th><th width="308.75">Manette RetroBat</th><th>Clavier</th></tr></thead><tbody><tr><td>Directions</td><td>Croix directionnelle / stick gauche</td><td>Flèches</td></tr><tr><td>Bouton 1</td><td>SUD</td><td>CTRL gauche</td></tr><tr><td>Bouton 2</td><td>EST</td><td>ALT gauche</td></tr><tr><td>Bouton 3</td><td>R1</td><td>ESPACE</td></tr><tr><td>Skill 1</td><td>OUEST</td><td>MAJ gauche</td></tr><tr><td>Skill 2</td><td>NORD</td><td>Z</td></tr><tr><td>Skill 3</td><td>L1</td><td>X</td></tr><tr><td>Crédit joueur 1</td><td>SELECT</td><td>5</td></tr><tr><td>Start joueur 1</td><td>START</td><td>1</td></tr><tr><td>Crédit joueur 2</td><td>—</td><td>6</td></tr><tr><td>Start joueur 2</td><td>—</td><td>2</td></tr><tr><td>Service</td><td>L3</td><td>9</td></tr><tr><td>Test</td><td>R3</td><td>0</td></tr><tr><td>Pause</td><td>—</td><td>P</td></tr><tr><td>Capture d'écran</td><td>—</td><td>F12</td></tr></tbody></table>

**Singe2**

<table><thead><tr><th width="159.5">Action</th><th width="261.5">Manette RetroBat</th><th>Clavier</th></tr></thead><tbody><tr><td>Directions</td><td>Croix directionnelle / sticks</td><td>Flèches</td></tr><tr><td>Action 1</td><td>SUD</td><td>ESPACE ou CTRL gauche</td></tr><tr><td>Action 2</td><td>EST</td><td>ALT gauche</td></tr><tr><td>Action 3</td><td>OUEST</td><td>MAJ gauche</td></tr><tr><td>Action 4</td><td>NORD</td><td>MAJ droite</td></tr><tr><td>Crédit joueur 1</td><td>SELECT</td><td>5</td></tr><tr><td>Start joueur 1</td><td>START</td><td>1</td></tr><tr><td>Crédit joueur 2</td><td>—</td><td>6</td></tr><tr><td>Start joueur 2</td><td>—</td><td>2</td></tr><tr><td>Pause</td><td>—</td><td>P</td></tr></tbody></table>

Pour configurer vous-même les touches, désactivez **AUTOCONFIGURER LES MANETTES**.

### Pistolets

Les jeux de tir se jouent à la souris ou au pistolet. Pour brancher et régler un pistolet dans RetroBat, voir la page [**Pistolets**](../../../controleurs/supported-controllers/lightguns/).

* **Hypseus** : plusieurs pistolets sont reconnus automatiquement. L'option **PISTOLETS > UN SEUL PISTOLET** n'en garde qu'un. Avec un pistolet Sinden, RetroBat lance le logiciel Sinden et affiche la bordure blanche.
* **Wiimotes sur DolphinBar** (Hypseus) : la croix envoie le crédit (gauche) et le start (droite). Pour une deuxième Wiimote : crédit en bas, start en haut.
* **Singe2** : un seul pistolet. L'option **PISTOLETS > FORCER L'INDEX** choisit la souris utilisée. Le clic gauche est le bouton Action 3, le clic droit Action 1 et le clic du milieu Action 2.

L'option **AFFICHER CIBLE** affiche ou masque le viseur.

### Raccourcis

<table><thead><tr><th width="232.75">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td>ÉCHAP</td><td>Quitter (clavier)</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="304">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux au format zip</td><td><code>roms\singe\roms</code></td></tr><tr><td>Vidéos des jeux au format zip</td><td><code>roms\singe\vldp\&#x3C;jeu></code></td></tr><tr><td>Jeux au format dossier</td><td><code>roms\singe\&#x3C;jeu>.hypseus</code></td></tr><tr><td>Fichiers Framework</td><td><code>roms\singe</code></td></tr><tr><td>Touches de Hypseus</td><td><code>emulators\hypseus\hypinput.ini</code></td></tr><tr><td>Décorations de Hypseus</td><td><code>emulators\hypseus\bezels</code></td></tr><tr><td>Captures d'écran de Hypseus (F12)</td><td><code>emulators\hypseus\screenshots</code></td></tr><tr><td>Touches de Singe2</td><td><code>emulators\singe2\Singe\controls.cfg</code> (copie dans le dossier du jeu)</td></tr></tbody></table>

L'ordre dans lequel RetroBat choisit la décoration de Hypseus est décrit sur la page [**LaserDisc**](../arcade/daphne-laserdisc.md).

## Guides

### Ajouter un jeu au format zip (Hypseus)

C'est la méthode la plus simple, mais tous les jeux ne sont pas encore disponibles en zip.

1. Récupérez le fichier zip du jeu dans le dossier `00-zip-roms` du dépôt `hypseus_singe_data` de Hypseus, sur GitHub : [https://github.com/DirtBagXon/hypseus\_singe\_data/tree/master/00-zip-roms](https://github.com/DirtBagXon/hypseus_singe_data/tree/master/00-zip-roms)
2. Copiez ce zip dans `roms\singe\roms`.
3. Créez un dossier au nom du jeu dans `roms\singe\vldp` et copiez-y le fichier `.txt` et les fichiers vidéo et audio.

```
roms\
└─ singe\
   ├─ roms\
   │  └─ timegal.zip
   └─ vldp\
      └─ timegal\
         ├─ timegal.dat
         ├─ timegal.m2v
         ├─ timegal.ogg
         └─ timegal.txt
```

Le zip, le dossier dans `vldp` et le fichier `.txt` portent le même nom. Dans RetroBat, lancez le fichier zip.

### Ajouter un jeu au format dossier (Hypseus)

Le jeu est un dossier placé dans `roms\singe`, dont le nom se termine par `.hypseus`. Il doit contenir deux fichiers au nom du jeu :

* `<jeu>.singe`
* `<jeu>.txt`

Pour vous simplifier la tâche, partez des fichiers du dépôt `hypseus_singe_data` :

{% embed url="https://github.com/DirtBagXon/hypseus_singe_data/" %}

1. Téléchargez le contenu du dépôt et décompressez-le dans un dossier temporaire.

<div align="left"><figure><img src="../../../.gitbook/assets/image (552).png" alt=""><figcaption></figcaption></figure></div>

2. Ouvrez le dossier du jeu. Exemple : Asterix, dans le sous-dossier `00-singe2`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (553).png" alt=""><figcaption></figcaption></figure></div>

3. Le dossier contient un fichier texte qui indique les fichiers manquants et où les placer. Pour Asterix, il faut mettre `asterix.m2v` dans le dossier `Video`.
4. Ajoutez les fichiers demandés (`.m2v`, ou `.m2v` et `.ogg`).
5. Renommez le dossier en ajoutant `.hypseus` à la fin : `Asterix.hypseus`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (554).png" alt=""><figcaption></figcaption></figure></div>

6. Déplacez ce dossier dans `roms\singe`.

### Passer des paramètres à Hypseus (.commands)

Créez un fichier texte contenant les paramètres à ajouter, sur une seule ligne, et donnez-lui le nom du jeu avec l'extension `.commands` :

* format dossier : à côté du dossier du jeu, par exemple `roms\singe\Asterix.commands` pour `Asterix.hypseus` ;
* format zip : à côté du zip, par exemple `roms\singe\roms\timegal.commands`.

Le nom doit être exactement celui du jeu, sans l'extension `.hypseus` ou `.zip`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (555).png" alt=""><figcaption></figcaption></figure></div>

### Ajouter un jeu pour Singe2

Singe2 ne lit pas les jeux au format Hypseus. Seuls les jeux proposés sur le site de l'émulateur (kangaroopunch.com) fonctionnent.

1. Téléchargez le jeu sur le site de Singe 2.

{% embed url="https://kangaroopunch.com/view/ShowSoftware?id=7" %}

2. Ajoutez les fichiers vidéo et audio demandés.
3. **Gardez le nom du dossier tel qu'il a été téléchargé** et ajoutez `.hypseus` à la fin.

<div align="left"><figure><img src="../../../.gitbook/assets/image (556).png" alt=""><figcaption></figcaption></figure></div>

4. Déplacez le dossier dans `roms\singe` et choisissez l'émulateur **singe2** pour ce jeu.

Singe2 a besoin que le **mode développeur** de Windows soit activé (Paramètres de Windows) : RetroBat crée un lien vers le dossier du jeu dans `emulators\singe2`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (557).png" alt=""><figcaption></figcaption></figure></div>

## Problèmes connus

<table><thead><tr><th width="329">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Un jeu zip ne se lance pas</td><td>Vérifiez que <code>roms\singe\vldp\&#x3C;jeu>\&#x3C;jeu>.txt</code> existe et porte le même nom que le zip.</td></tr><tr><td>Un jeu au format dossier ne se lance pas</td><td>Le dossier doit contenir un fichier <code>.singe</code> et un fichier <code>.txt</code> dont le nom commence par celui du dossier.</td></tr><tr><td>Singe2 affiche une erreur de lien symbolique</td><td>Activez le mode développeur dans les paramètres de Windows.</td></tr><tr><td>Singe2 ne lance pas un jeu qui marche avec Hypseus</td><td>Les formats sont différents : Singe2 ne lit que les jeux de son site.</td></tr><tr><td>La manette ne répond pas avec Singe2</td><td>Choisissez le bon numéro dans <strong>CONTRÔLES > FORCER L'INDEX MANETTE</strong>.</td></tr><tr><td>Le viseur du pistolet gêne</td><td>Désactivez <strong>AFFICHER CIBLE</strong>.</td></tr><tr><td>« Framework » et « FrameworkKimmy » apparaissent dans la liste des jeux</td><td>Ce ne sont pas des jeux, mais ils sont nécessaires. Masquez-les : menu du jeu > <strong>ÉDITER LES MÉTADONNÉES DU JEU</strong> > <strong>CACHÉ</strong>.</td></tr><tr><td>F12 ne crée pas de capture d'écran avec Hypseus</td><td>Les captures ne fonctionnent que sur l'écran principal.</td></tr></tbody></table>
