# Starship

<div align="left"><figure><img src="../../../../.gitbook/assets/image (645).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

**Starship** est un portage PC de **Star Fox 64** (Nintendo, 1997), réalisé par l'équipe HarbourMasters à partir de la décompilation du jeu. Il ajoute la haute résolution, l'écran large, une fréquence d'images jusqu'à 360 images par seconde, des améliorations et des packs de textures.

Le jeu n'est pas fourni : Starship extrait les données de votre propre ROM du jeu (version américaine).

{% embed url="https://github.com/HarbourMasters/Starship" %}

## En bref

<table><thead><tr><th width="277.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\starship</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>starship</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (ROM du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Non (configuration de Starship)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Starship ne lit que les ROM au format **.z64**. Une ROM `.n64` ou `.v64` doit d'abord être convertie en `.z64` (par exemple avec l'outil en ligne de hack64.net).

{% embed url="https://hack64.net/tools/swapper.php" %}

Versions compatibles :

<table><thead><tr><th width="266.5">Version</th><th>Utilisation</th></tr></thead><tbody><tr><td>Nintendo 64 USA 1.0 et 1.1</td><td>Jeu complet</td></tr><tr><td>Nintendo 64 Japon 1.0</td><td>Voix japonaises seulement</td></tr><tr><td>Nintendo 64 Europe 1.0</td><td>Voix européennes (« Lylat ») seulement</td></tr></tbody></table>

Il faut une version américaine pour jouer. Les versions japonaise et européenne ne servent qu'à remplacer les voix (voir [**Guides**](starship.md#voix-japonaises-ou-europeennes)).

Une seule entrée suffit dans `roms\starship` : une fois les données extraites, la ROM n'est plus lue.

## Contrôles

### Configuration de la manette

RetroBat ne configure pas la manette : Starship utilise sa propre configuration par défaut, qui suit la position des boutons.

<table><thead><tr><th width="250.25">Manette RetroBat</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Stick</td></tr><tr><td>SUD</td><td>A</td></tr><tr><td>OUEST</td><td>B</td></tr><tr><td>NORD ou R2</td><td>C gauche</td></tr><tr><td>EST ou L2</td><td>C bas</td></tr><tr><td>Stick droit (haut / droite)</td><td>C haut / C droite</td></tr><tr><td>L1</td><td>Z</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>Croix</td><td>Croix</td></tr><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>Ouvrir / fermer la barre de menu de Starship</td></tr></tbody></table>

Pour changer les touches, utilisez **Settings > Controller > Controller Mapping** dans la barre de menu de Starship : la configuration est conservée.

**CONTRÔLES > INVERSER L'AXE Y** inverse l'axe vertical pendant le pilotage.

Quand la barre de menu est ouverte, la manette sert à s'y déplacer : la croix pour choisir, SUD pour valider. Le jeu ne reçoit plus les commandes de la manette tant que la barre de menu est affichée.

### Raccourcis

<table><thead><tr><th width="232.75">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td><strong>SELECT</strong></td><td>Ouvrir / fermer la barre de menu de Starship</td></tr></tbody></table>

Au clavier :

<table><thead><tr><th width="111.5">Touche</th><th>Action</th></tr></thead><tbody><tr><td><strong>F1</strong></td><td>Ouvrir / fermer la barre de menu</td></tr><tr><td><strong>F4</strong></td><td>Redémarrer le jeu</td></tr><tr><td><strong>F11</strong></td><td>Plein écran</td></tr><tr><td><strong>Tab</strong></td><td>Activer / désactiver les textures personnalisées</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="261.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegarde</td><td><code>emulators\starship\default.sav</code></td></tr><tr><td>Données extraites du jeu</td><td><code>emulators\starship\sf64.o2r</code></td></tr><tr><td>Mods et packs de textures</td><td><code>emulators\starship\mods</code></td></tr><tr><td>Configuration</td><td><code>emulators\starship\starship.cfg.json</code></td></tr></tbody></table>

## Guides

### Premier lancement

Starship ne reçoit pas la ROM en argument : RetroBat la copie dans `emulators\starship`, puis Starship guide l'extraction.

1. À la question **Please provide a Starfox 64 ROM**, répondez **Yes**.
2. Dans la fenêtre qui s'ouvre (déjà dans `emulators\starship`), choisissez la ROM, puis validez le message de début d'extraction.
3. L'extraction prend quelques minutes. À la question **ROM Extracted. Extract another?**, répondez **No** (ou **Yes** pour ajouter tout de suite les voix japonaises ou européennes).

Les lancements suivants démarrent directement.

### Voix japonaises ou européennes

Avec une ROM japonaise ou européenne, Starship peut remplacer les voix du jeu : utilisez **Settings > Language > Install JP/EU Audio** dans la barre de menu (Starship se ferme, les voix sont prises en compte au lancement suivant), ou répondez **Yes** à **Extract another?** au premier lancement. Choisissez ensuite la langue des voix dans **Settings > Language > Voices**.

### Mods et packs de textures

Placez les mods (fichiers `.o2r` ou `.otr` : textures, modèles, musiques) dans `emulators\starship\mods`, puis lancez le jeu. **Tab** active ou désactive les textures personnalisées en jeu.

### Autres options utiles

<table><thead><tr><th width="360.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Résolution de rendu, de <strong>240p (NATIF)</strong> à <strong>2160p (4K)</strong>. Par défaut : <strong>720p</strong>.</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td>Par défaut, l'image remplit l'écran. <strong>NATIF (4:3)</strong> garde les proportions d'origine, <strong>ÉCRAN LARGE (16:9)</strong>, <strong>3DS (5:3)</strong>, <strong>16:10</strong> ou <strong>ULTRA LARGE (21:9)</strong> élargissent le champ de vision.</td></tr><tr><td><strong>DÉCORATIONS</strong></td><td>Les décorations ne s'affichent qu'avec <strong>RAPPORT D'ASPECT</strong> réglé sur <strong>NATIF (4:3)</strong>.</td></tr><tr><td><strong>MISE À L'ÉCHELLE (NOMBRE ENTIER)</strong></td><td>Agrandit l'image d'un nombre entier de fois, pour des pixels nets.</td></tr><tr><td><strong>SYNCHRONISATION VERTICALE</strong></td><td>Activée par défaut.</td></tr><tr><td><strong>RENDU VISUEL > FPS CIBLE</strong></td><td>Fréquence d'images, de 30 (fréquence d'origine) à 360 images par seconde. Les images intermédiaires sont interpolées. Par défaut, le jeu suit la fréquence de l'écran (60 Hz, 144 Hz…).</td></tr><tr><td><strong>RENDU VISUEL > FILTRAGE DES TEXTURES</strong></td><td><strong>LINÉAIRE</strong> (par défaut), <strong>TROIS POINTS</strong> (comme la N64) ou <strong>AUCUN</strong>.</td></tr><tr><td><strong>RENDU VISUEL > ANTICRÉNELAGE (MSAA)</strong></td><td>Lisse les contours des polygones (1 à 8).</td></tr><tr><td><strong>PILOTES > VIDÉO</strong></td><td><strong>OPENGL</strong> (par défaut) ou <strong>DIRECTX</strong>.</td></tr><tr><td><strong>PILOTES > AUDIO</strong></td><td><strong>WASAPI</strong> (par défaut) ou <strong>SDL</strong>.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="350.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Starship demande une ROM à chaque lancement</td><td>L'extraction n'a pas abouti : choisissez une ROM américaine au format <code>.z64</code> (voir <a href="starship.md#quel-format-de-jeu"><strong>Quel format de jeu ?</strong></a>).</td></tr><tr><td>« Unsupported ROM »</td><td>La ROM n'est pas dans la liste des versions compatibles, ou n'est pas au format <code>.z64</code>.</td></tr><tr><td>Une fenêtre de console s'ouvre avec le jeu</td><td>Elle fait partie de Starship : ne la fermez pas, cela fermerait aussi le jeu.</td></tr><tr><td>Les touches ne conviennent pas</td><td>RetroBat ne configure pas la manette de Starship : changez-les dans <strong>Settings > Controller > Controller Mapping</strong>.</td></tr><tr><td>Écran noir ou plantage au lancement</td><td>Réglez <strong>PILOTES > VIDÉO</strong> sur <strong>DIRECTX</strong>.</td></tr><tr><td>Les décorations ne s'affichent pas</td><td>Réglez <strong>RAPPORT D'ASPECT</strong> sur <strong>NATIF (4:3)</strong>.</td></tr><tr><td>Un mod ne s'affiche pas</td><td>Vérifiez qu'il est dans <code>emulators\starship\mods</code> et qu'il est prévu pour la version de Starship livrée ; appuyez sur <strong>Tab</strong> pour activer les textures personnalisées.</td></tr></tbody></table>
