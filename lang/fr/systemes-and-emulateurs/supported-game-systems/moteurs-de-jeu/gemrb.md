# GemRB

<div align="left"><figure><img src="../../../.gitbook/assets/image (803).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**GemRB** est une version libre du moteur **Infinity Engine** de BioWare. Il lance les jeux de rôle **Baldur's Gate**, **Baldur's Gate II**, **Icewind Dale**, **Icewind Dale II** et **Planescape: Torment**, avec leurs extensions et des mods.

GemRB est développé depuis plus de 20 ans : la compatibilité est bonne, mais les jeux peuvent encore avoir des défauts.

Les jeux ne sont pas fournis : il faut les versions d'origine (BioWare, Black Isle), de vos propres exemplaires.

{% embed url="https://gemrb.org/" %}

## En bref

<table><thead><tr><th width="299"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\gemrb</code></td></tr><tr><td><strong>Extensions</strong></td><td>.auto .bg1 .bg2 .how .iwd .iwd2 .pst</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>gemrb</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique : le stick gauche déplace le pointeur</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Compatibilité

<table><thead><tr><th width="296">Jeu</th><th width="132.75">Jouable</th><th width="113">Complet</th><th>Abouti</th></tr></thead><tbody><tr><td>Baldur's Gate</td><td>OUI</td><td>OUI</td><td>OUI</td></tr><tr><td>Baldur's Gate II</td><td>OUI</td><td>OUI</td><td>OUI</td></tr><tr><td>Icewind Dale</td><td>OUI</td><td>OUI</td><td>OUI</td></tr><tr><td>Icewind Dale II</td><td>OUI</td><td>NON</td><td>NON</td></tr><tr><td>Planescape: Torment</td><td>OUI</td><td>OUI</td><td>NON</td></tr><tr><td>Éditions Enhanced (Beamdog)</td><td>NON</td><td>NON</td><td>NON</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Chaque jeu est un dossier qui contient tous les fichiers du jeu installé. Le nom du dossier se termine par un point suivi de l'identifiant du jeu :

<table><thead><tr><th width="474">Jeu</th><th>Identifiant</th></tr></thead><tbody><tr><td>Baldur's Gate (avec ou sans Tales of the Sword Coast)</td><td><code>bg1</code></td></tr><tr><td>Baldur's Gate II: Shadows of Amn (avec ou sans Throne of Bhaal)</td><td><code>bg2</code></td></tr><tr><td>Icewind Dale (sans extension)</td><td><code>iwd</code></td></tr><tr><td>Icewind Dale: Heart of Winter (avec ou sans Trials of the Luremaster)</td><td><code>how</code></td></tr><tr><td>Icewind Dale II</td><td><code>iwd2</code></td></tr><tr><td>Planescape: Torment</td><td><code>pst</code></td></tr><tr><td>Détection automatique (pour essayer)</td><td><code>auto</code></td></tr></tbody></table>

Exemple pour Baldur's Gate :

<div align="left"><figure><img src="../../../.gitbook/assets/image (805).png" alt=""><figcaption></figcaption></figure></div>

## Contrôles

Les jeux se jouent à la souris et au clavier (pointer et cliquer). Les écrans tactiles servent de souris.

RetroBat active la manette : le stick gauche déplace le pointeur, le stick droit fait défiler la carte. **CONTRÔLES > VITESSE DU POINTEUR** et **ZONE MORTE JOYSTICK** la règlent. Avec plusieurs manettes, seule celle du joueur 1 est utilisée.

### Raccourcis

<table><thead><tr><th width="265.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="242.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\gemrb\&#x3C;jeu>.&#x3C;identifiant></code></td></tr><tr><td>Sauvegardes</td><td><code>saves\gemrb\&#x3C;jeu></code></td></tr><tr><td>Configuration</td><td><code>emulators\gemrb\GemRB.cfg</code></td></tr></tbody></table>

## Guides

### Changer la résolution

Sans mod écran large, les jeux s'affichent dans leurs résolutions d'origine :

| Jeu                                                   | Résolutions d'origine                |
| ----------------------------------------------------- | ------------------------------------ |
| Baldur's Gate (avec ou sans Tales of the Sword Coast) | 640x480                              |
| Baldur's Gate II (avec ou sans Throne of Bhaal)       | 640x480, 800x600, 1024x768, 1280x960 |
| Icewind Dale (sans extension)                         | 640x480                              |
| Icewind Dale: Heart of Winter                         | 640x480, 800x600, 1024x768, 1280x960 |
| Icewind Dale II                                       | 800x600, 1024x768, 1280x960          |
| Planescape: Torment                                   | 640x480                              |

Choisissez la résolution dans **RÉSOLUTION INTERNE DU JEU** (BUREAU = résolution de l'écran) :

<div align="left"><figure><img src="../../../.gitbook/assets/image (804).png" alt=""><figcaption></figcaption></figure></div>

### Mods écran large

Pour une résolution d'écran large, appliquez un mod écran large au jeu (selon le jeu, d'autres mods peuvent être nécessaires pour que l'interface s'affiche bien) :

{% embed url="https://www.gibberlings3.net/mods/tools/widescreen/" %}

Suivez les instructions du mod, puis choisissez dans **RÉSOLUTION INTERNE DU JEU** la résolution réglée avec le mod (BUREAU si c'est celle de l'écran).

### Options

* **RENDU VISUEL > ZOOM** : zoom de la carte à la molette, comme les éditions Enhanced.
* **ÉMULATION > ENCODAGE DE LA LANGUE** : seulement pour les versions asiatiques des jeux.

## Problèmes connus

| Problème                                          | Solution                                           |
| ------------------------------------------------- | -------------------------------------------------- |
| Le mauvais jeu est lancé ou le jeu ne démarre pas | Vérifiez l'identifiant à la fin du nom du dossier. |
| Le pointeur bouge seul                            | Augmentez **ZONE MORTE JOYSTICK**.                 |
