---
description: Microsoft
---

# DOS

<div align="left"><figure><img src="../../../.gitbook/assets/image (757).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**MS-DOS** est le système d'exploitation des PC compatibles IBM de 1981 au milieu des années 1990, avant Windows 95. Des milliers de jeux sont sortis sous DOS : **Doom**, **Prince of Persia**, **Lemmings**, **Monkey Island**, **Day of the Tentacle**, **X-COM**, **Commander Keen**, **Duke Nukem 3D**, **Dune II**, **Alone in the Dark**…

Chaque PC était différent : processeur, carte graphique (CGA, EGA, VGA, SVGA), carte son (Sound Blaster, AdLib, Gravis Ultrasound, Roland MT-32). Les émulateurs DOSBox reproduisent ce matériel. La plupart des jeux se jouent au clavier et à la souris ; certains acceptent un joystick.

RetroBat propose quatre émulateurs, tous basés sur DOSBox : le core libretro **dosbox\_pure** (par défaut), **DOSBox Pure** en version autonome, **DOSBox Staging** et **DOSBox**.

{% embed url="https://fr.wikipedia.org/wiki/MS-DOS" %}

## En bref

<table><thead><tr><th width="287.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\dos</code></td></tr><tr><td><strong>Extensions</strong></td><td>.dosbox .pc .dos .dosz .zip .m3u8 .bat</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: dosbox_pure</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (ROM MT-32 optionnelles)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Mappage automatique de DOSBox Pure (core et autonome) ; joystick DOS ou pad2key avec DOSBox Staging et DOSBox</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core dosbox_pure ; DOSBox Pure par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="199.5">Émulateur</th><th width="291.5">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: dosbox_pure</strong> (défaut)</td><td>Lit les jeux en <code>.zip</code> sans les décompresser, menu de démarrage à la manette, mappage automatique de la manette pour beaucoup de jeux, clavier virtuel, sauvegardes instantanées, shaders et décorations de RetroArch.</td><td>—</td></tr><tr><td><strong>dosbox-pure</strong></td><td>Le même moteur en programme autonome, avec son propre menu.</td><td>Sauvegardes instantanées par raccourcis, non gérées par RetroBat.</td></tr><tr><td><strong>dosbox-staging</strong></td><td>DOSBox moderne et très fidèle : shaders CRT, 3dfx Voodoo, nombreuses cartes son, réglages fins du processeur.</td><td>Pas de sauvegardes instantanées. Pas de mappage automatique de la manette. Ne lit pas les <code>.dosz</code>.</td></tr><tr><td><strong>dosbox</strong></td><td>DOSBox 0.74 d'origine.</td><td>Ne lance que les dossiers de jeu (voir <a href="ms-dos.md#quel-format-de-jeu"><strong>Quel format de jeu ?</strong></a>). Peu de réglages.</td></tr></tbody></table>

**En cas de doute, gardez libretro: dosbox\_pure.**

## BIOS

Aucun BIOS n'est nécessaire.

Pour la musique MIDI, RetroBat fournit la banque de sons `Roland_SC-55.sf2` dans `bios\scummvm\extra`. Vous pouvez ajouter dans ce même dossier :

| Fichier                            | Utilisé pour                              | Vérifié par RetroBat |
| ---------------------------------- | ----------------------------------------- | -------------------- |
| `MT32_CONTROL.ROM`, `MT32_PCM.ROM` | Roland MT-32 (Sierra, LucasArts, Origin…) | Oui (optionnel)      |
| `Roland_SC-88.sf2`                 | Roland SC-88                              | Non                  |

Ces fichiers sont partagés avec ScummVM. Choisissez le périphérique avec **AUDIO > SORTIE MIDI**.

## Quel format de jeu ?

| Format                               | dosbox\_pure (core, autonome) | dosbox-staging                              | dosbox |
| ------------------------------------ | ----------------------------- | ------------------------------------------- | ------ |
| **.zip**, **.dosz**                  | Oui, sans décompression       | `.zip` seulement (décompressé par RetroBat) | Non    |
| **Dossier** `.pc`, `.dos`, `.dosbox` | Oui                           | Oui                                         | Oui    |
| **.bat**                             | Oui                           | Oui                                         | Non    |
| **.m3u8** (plusieurs disques)        | Oui                           | Non                                         | Non    |

* **Archive** : placez le jeu dans un `.zip` (ou `.dosz`, même format), sous le nom du jeu (`Lemmings.zip`).
* **Dossier** : créez un dossier qui porte l'extension `.pc`, `.dos` ou `.dosbox` (`Lemmings.pc`) et mettez-y les fichiers du jeu. Un fichier `dosbox.bat` dans le dossier lance le jeu (pour DOSBox Staging : `dosbox.bat`, `run.bat` ou `autoexec.bat`). Un `dosbox.conf` dans le dossier donne les réglages du jeu (DOSBox Staging ; core dosbox\_pure avec **ÉMULATION > CHARGER DOSBOX.CONF**).
* **.bat** : un fichier de commandes qui lance le jeu.

```
roms\
└─ dos\
   ├─ Lemmings.zip
   └─ Prince of Persia.pc\
      ├─ dosbox.bat
      └─ (fichiers du jeu)
```

### Jeux au format zip

DOSBox Pure peut charger des fichiers directement depuis une archive **ZIP** sans extraction préalable. Les modifications (parties sauvegardées, installation) sont enregistrées dans un fichier séparé (voir [**Dossiers**](ms-dos.md#dossiers)) : l'archive d'origine n'est pas modifiée.

### Monter un jeu sur les lecteurs A ou D (DOSBox Pure) <a href="#mount-zip-as-a-or-d-drive" id="mount-zip-as-a-or-d-drive"></a>

Certains jeux nécessitent d'être montés sur un lecteur de disquette (A:) ou un lecteur cd-rom (D), pour cela renommer le fichier `.ZIP` en `.D.ZIP` ou .`A.ZIP` (pour utiliser respectivement les lecteurs D ou A).

### Multi-disque

Utiliser un fichier `.m3u8` (DOSBox Pure). Tous les fichiers qu'il liste sont ajoutés au changement de disque. La première image est montée en A: (disquette) ou D: (CD-ROM) selon son type.

## Contrôles

Les jeux DOS se jouent surtout au clavier et à la souris. Le clavier et la souris du PC fonctionnent avec tous les émulateurs.

### Core dosbox\_pure et DOSBox Pure

DOSBox Pure reconnaît beaucoup de jeux et place les touches sur la manette tout seul (**CONTRÔLES > MAPPING AUTOMATIQUE DE LA MANETTE**, activé par défaut).

* **L3** ouvre le clavier virtuel (core, réglable avec **INTERFACE UTILISATEUR > UTILISATION DU BOUTON L3** : CLAVIER VIRTUEL, CLAVIER VIRTUEL SEUL (EN JEU), MENU DU CORE ou désactivé). Avec DOSBox Pure autonome, L3 ouvre le menu.
* **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** (core) choisit ce que la manette émule : touches du clavier, souris, joystick DOS, manette Gravis, flight stick…
* **CONTRÔLES > DISPOSITION CLAVIER** adapte le clavier DOS à votre clavier (FRANCE pour un clavier AZERTY).
* **CONTRÔLES > FOCUS CLAVIER** (core) donne tout le clavier au jeu : les raccourcis de RetroArch sont désactivés. La touche **Arrêt défil** bascule.

Certains jeux affichent les boutons de la manette officielle Gravis par couleur. Correspondance : Bleu = NORD, Rouge = OUEST, Jaune = SUD, Vert = EST.

### DOSBox Staging et DOSBox

La manette est vue par le jeu comme un joystick DOS (**CONTRÔLES > TYPE DE JOYSTICK** avec DOSBox Staging). Pour jouer à la manette à un jeu qui ne gère que le clavier, utilisez la fonctionnalité pad2key , ou le mappeur de DOSBox (**Ctrl + F1**).

### Raccourcis

Le core dosbox\_pure utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../navigation/hotkeys.md)).

**DOSBox Pure (autonome)**

<table><thead><tr><th width="219.5">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td></td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarde instantanée</td><td>Ctrl + F5</td></tr><tr><td>HOTKEY + NORD</td><td>Chargement instantané</td><td>Ctrl + F9</td></tr><tr><td>L3</td><td>Menu de DOSBox Pure</td><td>Ctrl + F12</td></tr><tr><td>—</td><td>Pause</td><td>Ctrl + F1</td></tr><tr><td>—</td><td>Avance rapide (maintenir)</td><td>Ctrl + F3</td></tr><tr><td>—</td><td>Plein écran / fenêtre</td><td>Ctrl + F7</td></tr><tr><td>—</td><td>Verrouiller la souris dans la fenêtre</td><td>Ctrl + F11</td></tr></tbody></table>

L'emplacement de sauvegarde se choisit dans le menu de DOSBox Pure (**Saving & Loading**). Ces sauvegardes n'apparaissent pas dans le gestionnaire de sauvegardes.

**DOSBox Staging et DOSBox**

| Raccourci          | Action                               | Clavier      |
| ------------------ | ------------------------------------ | ------------ |
| **HOTKEY + START** | Quitter                              |              |
| —                  | Mappeur des touches et de la manette | Ctrl + F1    |
| —                  | Plein écran / fenêtre                | Alt + Entrée |

## Dossiers

<table><thead><tr><th width="331.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\dos</code></td></tr><tr><td>Banques de sons et ROM MT-32</td><td><code>bios\scummvm\extra</code> (copiées dans le dossier de DOSBox Pure et de DOSBox Staging)</td></tr><tr><td>Core dosbox_pure : modifications des jeux en <code>.zip</code></td><td><code>saves\dos</code></td></tr><tr><td>Core dosbox_pure : sauvegardes instantanées</td><td><code>saves\dos\libretro.dosbox_pure</code></td></tr><tr><td>DOSBox Pure autonome : sauvegardes et sauvegardes instantanées</td><td><code>saves\dos\dosbox-pure</code></td></tr><tr><td>DOSBox Pure autonome : configuration</td><td><code>emulators\dosbox-pure\DOSBoxPure.cfg</code></td></tr><tr><td>DOSBox Staging : configuration</td><td><code>emulators\dosbox-staging\dosbox-staging.conf</code> (ou <code>dosbox.conf</code> dans le dossier du jeu)</td></tr><tr><td>DOSBox Staging, DOSBox : sauvegardes des jeux</td><td>Dossier du jeu</td></tr></tbody></table>

## Guides

### Démarrer un jeu

Le premier écran affiché lors du lancement d'un jeu avec DOSBox Pure permet de sélectionner l'exécutable à utiliser pour lancer le jeu. Cet écran est navigable avec une manette. Il est possible de définir un exécutable par défaut en appuyant sur la croix directionnel DROITE, permettant ainsi d'éviter cet écran lors de la prochaine exécution du jeu.

<div align="left"><figure><img src="../../../.gitbook/assets/image (758).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Si le jeu ne contient qu'un seul exécutable cet écran n'apparaîtra pas.
{% endhint %}

**INTERFACE UTILISATEUR > MENU DE DÉMARRAGE DOSBOX** (core) règle ce qui se passe quand le jeu se termine : fermeture immédiate, après 3 ou 5 secondes, ou retour au menu.

### Installer un jeu (DOSBox Staging)

Avec DOSBox Staging, **ÉMULATION > ESSAYER DE LANCER LE SETUP DU JEU** lance le programme d'installation du jeu (`SETUP.EXE`, ou celui choisi avec **ÉMULATION > EXÉCUTABLE DE SETUP**) pour régler la carte son. **ÉMULATION > FORCER LE LANCEMENT DE L'EXE** lance un exécutable précis.

### Un jeu trop rapide ou trop lent

* Core dosbox\_pure, DOSBox Pure : **ÉMULATION > FRÉQUENCE CPU (CYCLES)**.
* DOSBox Staging : **ÉMULATION > FRÉQUENCE CPU (CYCLES)** pour les jeux en mode réel, **ÉMULATION > CYCLES CPU (MODE PROTÉGÉ)** pour les jeux plus récents (Doom, Duke Nukem 3D…).

### Son et musique

* **AUDIO > MODÈLE DE SOUNDBLASTER** et **AUDIO > SORTIE MIDI** règlent la carte son et la musique. La carte son choisie dans le programme d'installation du jeu doit correspondre.
* **AUDIO > GRAVIS ULTRASOUND** active la carte Gravis pour les jeux qui la gèrent.

### Autres options utiles

<table><thead><tr><th width="225.75">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>dosbox_pure (core, autonome)</td><td><strong>VIDÉO > ACCÉLÉRATEUR 3DFX VOODOO</strong></td><td>Carte 3D pour les jeux compatibles (Tomb Raider, Carmageddon…).</td></tr><tr><td>dosbox_pure (core, autonome)</td><td><strong>VIDÉO > CORRECTION DU RAPPORT D'ASPECT</strong></td><td>Corrige les pixels non carrés des jeux DOS.</td></tr><tr><td>dosbox_pure (autonome)</td><td><strong>RENDU VISUEL > FILTRE CRT</strong></td><td>Effet d'écran cathodique.</td></tr><tr><td>dosbox-staging</td><td><strong>SHADERS</strong></td><td>Rendu CRT (CRT AUTO par défaut), lissage ou pixels nets.</td></tr><tr><td>dosbox-staging</td><td><strong>VOODOO > ACTIVER L'ÉMULATION 3DFX VOODOO</strong></td><td>Carte 3D pour les jeux compatibles.</td></tr></tbody></table>

## Problèmes connus

| Problème                                                        | Solution                                                                                                                                                              |
| --------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Le jeu ne démarre pas avec DOSBox                               | DOSBox 0.74 ne lance que les dossiers de jeu avec un `dosbox.bat`. Utilisez le core dosbox\_pure.                                                                     |
| Un `.dosz` ne démarre pas avec DOSBox Staging                   | Renommez-le en `.zip`, ou utilisez DOSBox Pure.                                                                                                                       |
| L'écran de choix de l'exécutable revient à chaque lancement     | Choisissez l'exécutable avec la croix DROITE (voir [**Guides**](ms-dos.md#demarrer-un-jeu)).                                                                          |
| Pas de son ou pas de musique                                    | Réglez la carte son dans le programme d'installation du jeu, comme dans **AUDIO > MODÈLE DE SOUNDBLASTER**. Pour le MT-32, ajoutez les ROM dans `bios\scummvm\extra`. |
| Les touches ne correspondent pas à mon clavier                  | Réglez **CONTRÔLES > DISPOSITION CLAVIER**.                                                                                                                           |
| Les raccourcis de RetroArch se déclenchent en tapant au clavier | Activez **CONTRÔLES > FOCUS CLAVIER** (core).                                                                                                                         |
