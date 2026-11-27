# Power Bomberman

<div align="left"><figure><img src="../../../.gitbook/assets/image (795).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

**Power Bomberman** est un jeu gratuit créé par des fans de Bomberman, sorti en 2013 et toujours mis à jour. Il reprend le mode bataille de la série, avec de nombreux personnages, niveaux et objets (coup de pied, gant, bombes spéciales…), et se joue à plusieurs en local ou en ligne.

RetroBat installe le jeu et le lance comme les autres systèmes.

{% embed url="https://www.bombermanboard.com/viewtopic.php?t=1925" %}

## En bref

<table><thead><tr><th width="295.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\pb</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pb</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>powerbomberman</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Dans le jeu (en ligne)</td></tr></tbody></table>

## Quel émulateur choisir ?

Il n'y a rien à choisir : le jeu lui-même, `emulators\powerbomberman\Power Bomberman.exe`. Ce n'est pas un émulateur.

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

RetroBat lance le jeu à partir d'un **fichier vide** `.pb` placé dans `roms\pb`, par exemple `Power Bomberman.pb`. Si `roms\pb` est vide, créez ce fichier : son nom est celui qui s'affiche dans la liste des jeux.

## Contrôles

RetroBat configure automatiquement les manettes (jusqu'à 16), en commençant par les manettes DirectInput puis les manettes XInput.

<table><thead><tr><th width="310.25">Manette RetroBat</th><th>Power Bomberman</th></tr></thead><tbody><tr><td>Croix directionnelle, stick gauche</td><td>Se déplacer</td></tr><tr><td>START</td><td>Start</td></tr><tr><td>EST</td><td>Bouton d'action 1</td></tr><tr><td>SUD</td><td>Bouton d'action 2</td></tr><tr><td>OUEST</td><td>Bouton d'action 3</td></tr><tr><td>NORD</td><td>Bouton d'action 4</td></tr><tr><td>L1</td><td>Bouton d'action 5</td></tr><tr><td>R1</td><td>Bouton d'action 6</td></tr></tbody></table>

Le rôle de chaque bouton (poser une bombe, frapper, arrêter une bombe…) se voit et se change dans les options du jeu.

Sans manette, le joueur 1 joue au clavier : flèches pour se déplacer, **ENTRÉE** pour Start, **D**, **S**, **Q**, **Z**, **A** et **E** pour les boutons d'action (clavier AZERTY ; **D**, **S**, **A**, **W**, **Q** et **E** en QWERTY).

Pour régler vous-même les touches dans le jeu, désactivez **AUTOCONFIGURER LES MANETTES** : sinon RetroBat remplace les réglages à chaque lancement.

### Raccourcis

<table><thead><tr><th width="195.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="244">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Fichier de lancement</td><td><code>roms\pb</code></td></tr><tr><td>Jeu</td><td><code>emulators\powerbomberman</code></td></tr><tr><td>Réglages et touches</td><td><code>%LOCALAPPDATA%\pb\config.ini</code></td></tr></tbody></table>

Power Bomberman garde ses réglages dans le dossier de Windows `%LOCALAPPDATA%\pb` (en général `C:\Users\<nom>\AppData\Local\pb`), et non dans le dossier de RetroBat. Au premier lancement, RetroBat y copie un fichier de réglages adapté.

## Guides

### Options

<table><thead><tr><th width="317.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>SYNCHRONISATION VERTICALE</strong></td><td>Activée par défaut. Évite les déchirures de l'image.</td></tr><tr><td><strong>VIDÉO > FORCER PLEIN ÉCRAN</strong></td><td>Plein écran même si RetroBat est en fenêtre.</td></tr></tbody></table>

### Jouer en ligne

Le jeu en ligne se lance depuis le menu du jeu. Votre pseudo et vos réglages en ligne sont dans `%LOCALAPPDATA%\pb\config.ini` (section `[NETPLAY]`).

## Problèmes connus

<table><thead><tr><th width="335.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le système n'apparaît pas</td><td>Créez un fichier vide <code>Power Bomberman.pb</code> dans <code>roms\pb</code>.</td></tr><tr><td>Les touches réglées dans le jeu sont perdues</td><td>RetroBat les remplace à chaque lancement : désactivez <strong>AUTOCONFIGURER LES MANETTES</strong>.</td></tr><tr><td>Les joueurs ne sont pas dans l'ordre des manettes</td><td>Le jeu numérote d'abord les manettes DirectInput, puis les manettes XInput.</td></tr></tbody></table>
