# Sonic 3 AIR

<div align="left"><figure><img src="../../../../.gitbook/assets/image (695).png" alt="" width="349"><figcaption></figcaption></figure></div>

## Présentation

**Sonic 3 A.I.R.** (Angel Island Revisited) est une version PC remaniée de **Sonic 3 & Knuckles** (Sega, 1994), créée par Eukaryot. Elle reprend la physique exacte du jeu d'origine et ajoute l'écran large, la haute résolution, de nombreuses corrections, des options (Tails en assistant, nouveaux modes de jeu), un mode à deux joueurs et la gestion des mods.

Le jeu n'est pas fourni : Sonic 3 A.I.R. lit les données de votre propre ROM de Sonic 3 & Knuckles.

{% embed url="https://sonic3air.org/" %}

## En bref

<table><thead><tr><th width="262.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\sonic3-air</code></td></tr><tr><td><strong>Extensions</strong></td><td>.bin</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>sonic3air</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (ROM de Sonic 3 &#x26; Knuckles à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (2 joueurs)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Une ROM de **Sonic 3 & Knuckles** au format **.bin**. La ROM conseillée est celle de la version Steam de Sonic 3 & Knuckles, `Sonic_Knuckles_wSonic3.bin`. Placez-la dans `roms\sonic3-air` : RetroBat indique son emplacement au jeu à chaque lancement.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (696).png" alt=""><figcaption></figcaption></figure></div>

## Contrôles

RetroBat configure automatiquement les manettes des joueurs 1 et 2 :

<table><thead><tr><th width="247.75">Manette RetroBat</th><th>Sonic 3 A.I.R.</th></tr></thead><tbody><tr><td>Croix</td><td>Déplacement</td></tr><tr><td>SUD, EST, OUEST</td><td>Saut et capacités du personnage</td></tr><tr><td>NORD</td><td>Super transformation</td></tr><tr><td>START</td><td>Pause</td></tr></tbody></table>

Deux manettes du même modèle ne peuvent pas être utilisées en même temps : Sonic 3 A.I.R. les confond.

**CONTRÔLES > PUISSANCE DES VIBRATIONS** règle les vibrations des deux manettes.

### Raccourcis

<table><thead><tr><th width="234">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Quitter</td><td>HOTKEY + START</td></tr></tbody></table>

Pas de sauvegardes instantanées : la progression est enregistrée par le jeu.

## Dossiers

<table><thead><tr><th width="311.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes du jeu</td><td><code>emulators\sonic3air\savedata\storage</code>, copiées par RetroBat dans <code>saves\sonic3air\storage</code></td></tr><tr><td>Réglages (écrits par RetroBat)</td><td><code>emulators\sonic3air\savedata\settings.json</code>, <code>settings_input.json</code></td></tr><tr><td>Mods</td><td><code>emulators\sonic3air\savedata\mods</code></td></tr><tr><td>Bande-son remasterisée (téléchargée depuis le jeu)</td><td><code>emulators\sonic3air\savedata\data</code></td></tr></tbody></table>

## Guides

### Bande-son remasterisée

La bande-son remasterisée n'est plus incluse dans le jeu : elle se télécharge une seule fois depuis le menu **Options** du jeu. Elle reste ensuite dans le dossier `savedata` de l'émulateur.

### Mods

Sonic 3 A.I.R. gère lui-même ses mods. Placez le mod (dossier ou `.zip`) dans `emulators\sonic3air\savedata\mods`, puis activez-le dans le menu **Mods** du jeu.

### Options utiles

<table><thead><tr><th width="295.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>SHADERS</strong></td><td>Filtre d'image (net, doux, xBRZ, HQx).</td></tr><tr><td><strong>RENDU VISUEL > SCANLINES</strong></td><td>Lignes de balayage ; pas avec les filtres HQ et xBRZ.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="310.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu demande la ROM</td><td>Vérifiez que la ROM de Sonic 3 &#x26; Knuckles est bien dans <code>roms\sonic3-air</code> et lancez-la depuis RetroBat.</td></tr><tr><td>Le joueur 2 contrôle aussi le joueur 1</td><td>Les deux manettes sont du même modèle : utilisez deux modèles différents.</td></tr><tr><td>Pas de musique remasterisée</td><td>Téléchargez-la depuis le menu <strong>Options</strong> du jeu (voir <a href="sonic-3-air.md#bande-son-remasterisee"><strong>Bande-son remasterisée</strong></a>).</td></tr></tbody></table>
