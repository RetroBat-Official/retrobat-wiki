---
description: Nintendo
---

# WiiU

<div align="left"><figure><img src="../../../../.gitbook/assets/image (718).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

La **Wii U** est la console de salon de Nintendo qui succède à la Wii (2012-2017). Sa particularité est le **Wii U GamePad**, une manette avec un écran tactile qui sert de second écran ou d'écran principal. Elle reste compatible avec les Wiimotes et accepte aussi une manette classique, la **Wii U Pro Controller**.

Ses ventes (environ 13,5 millions de consoles) ont été faibles, mais beaucoup de ses jeux sont restés célèbres : Mario Kart 8, Super Mario 3D World, Splatoon, The Legend of Zelda: Breath of the Wild ou Xenoblade Chronicles X.

RetroBat utilise **Cemu**, l'émulateur Wii U de référence.

{% embed url="https://fr.wikipedia.org/wiki/Wii_U" %}

## En bref

<table><thead><tr><th width="260.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\wiiu</code></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .rpx .wud .wux .wua .m3u .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>cemu</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (<code>keys.txt</code> pour les jeux chiffrés)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (GamePad, Pro Controller, Wiimotes)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>keys.txt</code> dans <code>bios\cemu</code></td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire pour jouer. En revanche, les jeux **chiffrés** (`.wud`, `.wux` et images `.iso` de disque) demandent les clés de déchiffrement de chaque jeu, dans un fichier `keys.txt`. Sans elles, Cemu affiche « Could not decrypt title ».

<table><thead><tr><th width="137">Fichier</th><th width="153.75">Dossier</th><th>Obligatoire</th></tr></thead><tbody><tr><td><code>keys.txt</code></td><td><code>bios\cemu</code></td><td>Non (jeux chiffrés seulement)</td></tr></tbody></table>

RetroBat copie `bios\cemu\keys.txt` dans le dossier de Cemu (`emulators\cemu\portable\keys.txt`) à chaque lancement, s'il est plus récent. Vous pouvez aussi le placer directement dans `emulators\cemu\portable`.

Le fichier `keys.txt` s'extrait de votre console Wii U : voir le [guide de Cemu](https://wiki.cemu.info/wiki/Obtaining_Keys_for_Keys.txt).

Les jeux au format `.wua` et les dossiers de jeu décryptés (`.rpx`) n'ont pas besoin de clés.

## Quel format de jeu ?

<table><thead><tr><th width="149">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.rpx</strong></td><td>Jeu décrypté au format « Loadiine » (ou « Bootloader ») : un dossier avec les sous-dossiers <code>code</code>, <code>content</code> et <code>meta</code>, tel qu'il sort de votre console avec l'outil Dumpling. Le fichier <code>.rpx</code> est dans <code>code</code>. Format conseillé (voir <a href="wiiu.md#ajouter-des-jeux"><strong>Ajouter des jeux</strong></a>).</td></tr><tr><td><strong>.wua</strong></td><td>Archive Cemu : jeu, mise à jour et DLC dans un seul fichier, non chiffrée.</td></tr><tr><td><strong>.wud</strong> / <strong>.wux</strong></td><td>Image du disque (<code>.wux</code> = compressée). Chiffrée : demande <code>keys.txt</code>.</td></tr><tr><td><strong>.iso</strong></td><td>Image de disque. Chiffrée : demande <code>keys.txt</code>.</td></tr><tr><td><strong>.m3u</strong></td><td>Fichier texte qui donne le chemin du <code>.rpx</code> à lancer (voir <a href="wiiu.md#ajouter-des-jeux"><strong>Ajouter des jeux</strong></a>).</td></tr><tr><td><strong>.decomp</strong></td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

## Contrôles

### Configuration automatique

{% hint style="info" %}
RetroBat configure automatiquement pour Cemu :

* les manettes XInput ;
* les DualShock et DualSense ;
* la Nintendo Switch Pro.
{% endhint %}

Le joueur 1 joue avec un **GamePad** Wii U émulé, les joueurs 2 à 4 avec une **Pro Controller**. **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** (à 4) change ce choix : MANETTE (GamePad), MANETTE PRO CONTROLLER ou WIIMOTE À L'HORIZONTALE. Certains jeux à plusieurs refusent le GamePad pour le joueur 1 : passez-le en Pro Controller.

Les boutons sont placés comme sur une manette Nintendo (position, pas lettre) :

<table><thead><tr><th width="271.5">Manette RetroBat</th><th>Wii U</th></tr></thead><tbody><tr><td>START</td><td>+</td></tr><tr><td>SELECT</td><td>−</td></tr><tr><td>Croix</td><td>Croix</td></tr><tr><td>Stick gauche / stick droit</td><td>Stick gauche / stick droit</td></tr><tr><td>SUD</td><td>B (ou A si inversé)</td></tr><tr><td>EST</td><td>A (ou B si inversé)</td></tr><tr><td>OUEST</td><td>Y (ou X si inversé)</td></tr><tr><td>NORD</td><td>X (ou Y si inversé)</td></tr><tr><td>L1 / R1</td><td>L / R</td></tr><tr><td>L2 / R2</td><td>ZL / ZR</td></tr><tr><td>L3 / R3</td><td>Clic du stick gauche / droit</td></tr></tbody></table>

L'option **CONTRÔLES > INVERSER LES BOUTONS A/B/X/Y** inverse les boutons (A sur SUD, selon les lettres imprimées) :

<div align="left"><figure><img src="../../../../.gitbook/assets/image (719).png" alt=""><figcaption></figcaption></figure></div>

### Jouer avec des Wiimotes

Cemu permet de jouer avec de vraies Wiimotes connectées au PC (DolphinBar ou Bluetooth).

Choisissez le nombre de Wiimotes dans **CONTRÔLES > UTILISER DES WIIMOTES** (options avancées du système ou du jeu). Les autres manettes ne sont alors plus utilisées.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (720).png" alt=""><figcaption></figcaption></figure></div>

**CONTRÔLES > TYPE DE WIIMOTE 1** (à 4) indique pour chaque joueur la Wiimote connectée : MOTION PLUS, MOTION PLUS + NUNCHUK, STANDARD ou STANDARD + NUNCHUK.

### Détection des mouvements (motion control)

Certains jeux demandent le gyroscope de la manette pour avancer (par exemple certains sanctuaires de Zelda: Breath of the Wild).

Activez **CONTRÔLES > DÉTECTION DES MOUVEMENTS** dans les options avancées du système ou du jeu. Manettes compatibles aujourd'hui : Switch Pro, 8BitDo (en mode Switch / Pro Controller) et DualSense.

Le [wiki de Cemu](https://wiki.cemu.info/wiki/Motion_controls) détaille les autres solutions.

### Microphone

Les jeux qui demandent de souffler dans le micro du GamePad :

* **CONTRÔLES > BOUTON POUR ÉMULER LE MICROPHONE** associe un bouton au micro (L3 ou R3) ;
* **AUDIO > ACTIVER LE MICROPHONE DE L'ORDINATEUR** utilise le micro du PC.

{% hint style="info" %}
Le bouton du microphone ne fonctionne qu'avec le Wii U GamePad comme manette émulée.
{% endhint %}

### Afficher l'écran du GamePad

Le GamePad a son propre écran. Deux façons de l'afficher :

* **CONTRÔLES > AFFICHER L'ÉCRAN DU GAMEPAD** choisit un bouton (L3, R3 ou SELECT) qui montre l'écran du GamePad à la place de l'écran principal, tant qu'il est maintenu. Avec **CONTRÔLES > BASCULER L'ÉCRAN GAMEPAD**, chaque appui passe d'un écran à l'autre.
* **INTERFACE UTILISATEUR > VUE GAMEPAD SÉPARÉE** ouvre l'écran du GamePad dans une seconde fenêtre (pratique avec deux écrans).

{% hint style="info" %}
Le bouton d'écran ne fonctionne qu'avec le Wii U GamePad comme manette émulée.
{% endhint %}

### Raccourcis

HOTKEY + START quitte le jeu. Cemu n'a pas de sauvegardes instantanées : sauvegardez dans le jeu. Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="317.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\wiiu</code></td></tr><tr><td>mlc01 (sauvegardes, jeux, mises à jour et DLC installés)</td><td><code>saves\wiiu\cemu\mlc01</code></td></tr><tr><td>Clés des jeux chiffrés</td><td><code>bios\cemu\keys.txt</code> (copié dans <code>emulators\cemu\portable</code>)</td></tr><tr><td>Fichier de configuration</td><td><code>emulators\cemu\portable\settings.xml</code></td></tr><tr><td>Configuration des manettes</td><td><code>emulators\cemu\portable\controllerProfiles</code> (un fichier <code>.xml</code> par manette)</td></tr><tr><td>Packs graphiques</td><td><code>emulators\cemu\portable\graphicPacks</code></td></tr></tbody></table>

## Ajouter des jeux

Le format conseillé est le format **Loadiine** (ou « Bootloader ») : c'est le format des jeux extraits (dumpés) de votre console Wii U avec Dumpling. Le jeu est un dossier qui contient 3 sous-dossiers, `code`, `content` et `meta`. Par exemple :

<div align="left"><figure><img src="../../../../.gitbook/assets/image (721).png" alt=""><figcaption><p>Example of dumped Zelda game</p></figcaption></figure></div>

Il y a deux façons d'ajouter ces jeux dans RetroBat.

### Méthode 1 : installer le jeu dans Cemu et utiliser un fichier .m3u

Cette méthode simule l'installation du jeu dans la mémoire de la Wii U, comme pour un jeu acheté en version numérique. Le dossier d'origine du jeu n'est plus nécessaire après l'installation.

1. Ouvrez Cemu depuis le menu des émulateurs de RetroBat (ou directement `emulators\cemu\Cemu.exe`), puis choisissez **Fichier > Installer un jeu, une mise à jour ou un DLC**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (722).png" alt=""><figcaption><p>File > Install</p></figcaption></figure></div>

2. Sélectionnez le fichier `meta.xml` du dossier `meta` du jeu et lancez l'installation.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (723).png" alt=""><figcaption></figcaption></figure></div>

3. Attendez la fin de l'installation : le jeu apparaît dans la liste de Cemu.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (725).png" alt=""><figcaption></figcaption></figure></div>

4. Faites un clic droit sur le jeu et choisissez **Dossier du jeu**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (726).png" alt=""><figcaption></figcaption></figure></div>

5. L'explorateur Windows ouvre le dossier du jeu, qui contient le fichier `.rpx` (dans `code`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (736).png" alt=""><figcaption></figcaption></figure></div>

6. Quittez Cemu. Dans `roms\wiiu`, créez un fichier texte `<nom du jeu>.m3u` qui contient le chemin du `.rpx` :

`\..\..\saves\wiiu\cemu\mlc01\usr\title\`<mark style="color:red;">`<chemin du jeu>`</mark>`\code\`<mark style="color:red;">`<nom du fichier>`</mark>`.rpx`

Par exemple pour Zelda: Breath of the Wild :

Le chemin peut aussi être absolu (`C:\...`), ou relatif au dossier du fichier `.m3u`. Le fichier `example-to-edit.m3u.txt` du dossier `roms\wiiu` sert de modèle.

7. Enregistrez le fichier `.m3u` : le jeu est disponible dans RetroBat, prêt à être scrapé et lancé.

### Méthode 2 : placer le dossier du jeu dans roms\wiiu

Cette méthode simule la présence du disque dans la console.

Copiez le dossier du jeu (format Loadiine) dans `roms\wiiu` :

RetroBat trouve le fichier **.rpx** du dossier `code` : le jeu est disponible dans RetroBat, prêt à être scrapé et lancé.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (727).png" alt=""><figcaption></figcaption></figure></div>

ScreenScraper reconnaît le nom du fichier : par exemple, `U-King` est Zelda: Breath of the Wild.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (728).png" alt=""><figcaption></figcaption></figure></div>

### Autres formats

Les fichiers `.wua`, `.wud`, `.wux` et `.iso` se placent directement dans `roms\wiiu`. Pour `.wud`, `.wux` et `.iso`, ajoutez les clés du jeu dans `bios\cemu\keys.txt` (voir [**BIOS**](wiiu.md#bios)).

## Mises à jour et DLC

Les mises à jour et les DLC s'installent dans Cemu avec l'option **Installer un jeu, une mise à jour ou un DLC**. Elles ont le même format que les jeux : des dossiers Loadiine. Avec le format `.wua`, elles sont déjà dans le fichier du jeu.

1. Ouvrez Cemu depuis le menu des émulateurs de RetroBat et choisissez **Installer un jeu, une mise à jour ou un DLC**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (729).png" alt=""><figcaption><p>Select the install option</p></figcaption></figure></div>

2. Allez dans le dossier `meta` de la mise à jour ou du DLC et sélectionnez le fichier `meta.xml`.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (730).png" alt=""><figcaption><p>search for the meta.xml file in the meta folder</p></figcaption></figure></div>

3. Attendez la fin de l'installation.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (731).png" alt=""><figcaption></figcaption></figure></div>

4. Cemu affiche la version et le niveau du DLC dans les colonnes **Version** et **DLC**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (732).png" alt=""><figcaption></figcaption></figure></div>

Tout est installé dans `saves\wiiu\cemu\mlc01`.

## Packs graphiques

Les packs graphiques de Cemu améliorent le rendu (résolution, 60 images par seconde) et corrigent aussi des bugs dans certains jeux.

RetroBat ne les gère pas : activez-les dans Cemu. Ils sont ensuite appliqués à chaque lancement du jeu depuis RetroBat.

1. Ouvrez Cemu et choisissez **Options > Packs graphiques** :

<div align="left"><figure><img src="../../../../.gitbook/assets/image (735).png" alt=""><figcaption></figcaption></figure></div>

2. Cliquez sur **Télécharger les derniers packs graphiques de la communauté** (en bas à droite) et attendez la fin du téléchargement.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (733).png" alt=""><figcaption></figcaption></figure></div>

3. Consultez la liste des packs disponibles pour votre jeu et activez ceux qu'il vous faut.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (734).png" alt=""><figcaption></figcaption></figure></div>

4. Quittez Cemu : la configuration des packs est enregistrée automatiquement.

{% hint style="info" %}
La page de compatibilité de Cemu indique, pour chaque jeu, les réglages et les packs utiles :

[https://compat.cemu.info/](https://compat.cemu.info/)
{% endhint %}

## Problèmes connus

| Problème                                               | Solution                                                                                                                            |
| ------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| « Could not decrypt title »                            | Le jeu est chiffré : ajoutez ses clés dans `bios\cemu\keys.txt`, ou utilisez le format Loadiine ou `.wua`.                          |
| Un jeu à plusieurs ne reconnaît pas le joueur 1        | Passez **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** sur MANETTE PRO CONTROLLER.                                                      |
| Les profils de jeu créés dans Cemu ne s'appliquent pas | Normal : RetroBat les désactive pendant la partie pour appliquer ses propres options. Réglez le jeu dans les options de RetroBat.   |
| Un jeu plante ou s'affiche mal                         | Consultez [compat.cemu.info](https://compat.cemu.info/) : beaucoup de jeux demandent un pack graphique (voir **Packs graphiques**). |
| Saccades à la première partie                          | Cemu compile ses shaders. Avec Vulkan, **RENDU VISUEL > COMPILATION DES TEXTURES ASYNCHRONE** les réduit.                           |
