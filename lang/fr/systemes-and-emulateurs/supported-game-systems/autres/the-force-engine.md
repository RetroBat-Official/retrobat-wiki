# The Force Engine

<div align="left"><figure><img src="../../../.gitbook/assets/image (700).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**Star Wars: Dark Forces** (LucasArts, 1995) est un jeu de tir à la première personne dans l'univers de Star Wars.

RetroBat utilise **The Force Engine**, un moteur moderne qui reprend le jeu d'origine : haute résolution, écran large, rendu OpenGL, mods.

Les fichiers du jeu ne sont pas fournis : utilisez ceux de votre propre exemplaire (CD DOS, Steam, GOG).

{% embed url="https://theforceengine.github.io/" %}

## En bref

<table><thead><tr><th width="275.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\theforceengine</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>theforceengine</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Non : commandes de The Force Engine</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire. Copiez les fichiers de Dark Forces (dont `DARK.GOB`) dans `roms\theforceengine`.

## Quel format de jeu ?

Un fichier `.game` placé dans le dossier des fichiers du jeu lance Dark Forces. S'il contient le nom d'un mod sur sa première ligne, le mod est lancé (voir [**Guides**](the-force-engine.md#lancer-un-mod)).

## Contrôles

RetroBat ne configure pas la manette : The Force Engine la reconnaît et ses commandes se changent dans ses options.

**CONTRÔLES > DÉSACTIVER L'AIDE À LA VISÉE** et **DÉSACTIVER LA CIBLE** sont réglables dans RetroBat.

### Raccourcis

<table><thead><tr><th width="221.5">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="261.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeu</td><td><code>roms\theforceengine</code></td></tr><tr><td>Mods</td><td><code>roms\theforceengine\Mods</code></td></tr><tr><td>Sauvegardes et configuration</td><td><code>emulators\theforceengine</code> (<code>settings.ini</code> rend l'installation portable)</td></tr></tbody></table>

## Guides

### Organisation des fichiers

Copiez le jeu DOS d'origine (ou la version Steam / GOG) dans `roms\theforceengine`. Exemple avec la version DOS :

<div align="left"><figure><img src="../../../.gitbook/assets/image (703).png" alt=""><figcaption></figcaption></figure></div>

Créez un fichier texte dans le même dossier que l'exécutable du jeu, puis changez son extension en `.game`.

### Lancer un mod

Placez le mod dans `roms\theforceengine\Mods` :

Créez un fichier texte avec un nom facile à reconnaître (il est affiché dans la liste des jeux), écrivez le nom complet du mod (avec son extension) sur la première ligne, puis changez l'extension en `.game` :

<div align="left"><figure><img src="../../../.gitbook/assets/image (702).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (701).png" alt=""><figcaption></figcaption></figure></div>

### Options

* **RÉSOLUTION INTERNE** de 200p à 2160p (par défaut : résolution de l'écran), **VIDÉO > ÉCRAN LARGE**.
* **ÉMULATION > DÉSACTIVER LES VIDÉOS INTERMÉDIAIRES**, **INTERFACE UTILISATEUR > AFFICHER LES SOUS-TITRES**.

## Problèmes connus

<table><thead><tr><th width="327.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>The Force Engine ne trouve pas le jeu</td><td>Le fichier <code>.game</code> doit être dans le dossier qui contient <code>DARK.GOB</code>.</td></tr></tbody></table>
