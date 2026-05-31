# Raccourcis

Les "hotkeys" sont des raccourcis à la manette ou au clavier, qui sont utilisés pour réaliser certaines actions en jeu, comme par exemple la sauvegarde de progression d'un jeu (savestate), la mise en pause ou bien le rembobinage. L'utilisation la plus fréquente consiste à quitter une partie en cours en appuyant simultanément sur les boutons **HOTKEY** + **START.**

L'équipe RetroBat a défini des hotkeys par défaut à la manette et au clavier pour de nombreux émulateurs, ces hotkeys sont les suivantes :&#x20;

{% hint style="info" %}
Pour réaliser une action liée à une hotkey, il est nécessaire de presser la touche d'activation hotkey, puis de presser le second bouton simultanément.
{% endhint %}

<table><thead><tr><th width="234.699951171875">Hotkeys (manette)</th><th>touche clavier</th><th>Action</th></tr></thead><tbody><tr><td>Hotkey + <img src="../.gitbook/assets/image (7) (1).png" alt=""></td><td>CTRL+F12</td><td><a href="game-control-center.md">Game control center</a></td></tr><tr><td>Hotkey + <img src="../.gitbook/assets/image (20) (1).png" alt=""></td><td>F1</td><td>Menu de l'émulateur (ou Pause si l'émulateur n'a pas de menu)</td></tr><tr><td>Hotkey + <img src="../.gitbook/assets/image (35).png" alt=""></td><td>F4</td><td>Charger Save State</td></tr><tr><td>Hotkey + <img src="../.gitbook/assets/image (33).png" alt=""></td><td>F2</td><td>Enregistrer Save State</td></tr><tr><td>Hotkey + START</td><td>ECHAP</td><td>Quitter l'émulateur / le jeu</td></tr><tr><td>Hotkey + L1</td><td>F11</td><td>Éjecter Disque</td></tr><tr><td>Hotkey + R1</td><td></td><td>Service de traduction IA</td></tr><tr><td>Hotkey + L2</td><td>F9</td><td>Disque Index -</td></tr><tr><td>Hotkey + R2</td><td>F10</td><td>Disque Index +</td></tr><tr><td>Hotkey + D-PAD HAUT</td><td>F7</td><td>Choisir Slot de sauvegarde Index +</td></tr><tr><td>Hotkey + D-PAD BAS</td><td>F6</td><td>Choisir Slot de sauvegarde Index -</td></tr><tr><td>Hotkey + D-PAD GAUCHE</td><td>Retour arrière</td><td>Rembobiner</td></tr><tr><td>Hotkey + D-PAD DROITE</td><td>Constant : F<br>Bref : Espace</td><td>Avance rapide (Choix possible entre maintenir et basculer)</td></tr><tr><td>Hotkey + R3 (stick droit)</td><td>F8</td><td>Capture d'écran</td></tr><tr><td></td><td>F</td><td>Basculer plein écran</td></tr><tr><td></td><td>K</td><td>Avance de frame</td></tr><tr><td>Hotkey + L3</td><td>P</td><td>Pause (si un émulateur à un menu et que la Hotkey + <img src="../.gitbook/assets/image (95).png" alt=""> est utilisée)</td></tr></tbody></table>

Pour la liste des émulateurs ci-dessous, les hotkeys ont été alignés, avec quelques variations liés aux possibilités des émulateurs :

<details>

<summary>Émulateurs avec des hotkeys alignés</summary>

* RetroArch
* Ares (utilise PadToKey)
* BigPEmu
* Bizhawk (utilise PadToKey)
* Cgenius (Seulement sauvegarde / chargement savestate) (utilise PadToKey)
* Citron
* Demul
* DesMume (utilise PadToKey)
* Dhewm3
* Dolphin
* Duckstation
* Eden
* Flycast
* Hatari
* Jgenesis (utilise PadToKey)
* MAME
* Mednafen
* MelonDS (utilise PadToKey)
* Mesen
* Mupen64(RMG)
* OpenMSX
* PCSX2
* PPSSPP
* Project64 (utilise PadToKey)
* Raine (utilise PadToKey)
* Snes9X (utilise PadToKey)
* Sudachi
* Suyu
* Yuzu

</details>

## Personnalisation des hotkeys

RetroBat permet de modifier l'assignation des hotkeys par défaut pour de nombreux émulateurs, aussi bien pour le clavier que pour la manette.

Les modifications doivent être faites dans un fichier situé dans le dossier `\system\resources\inputmapping` de votre installation RetroBat :

* **kb\_hotkeys.yml** : permet de modifier l'assignation standard pour clavier
* **controller\_hotkeys.yml** : permet de modifier l'assignation standard pour manette

{% hint style="info" %}
Il est également possible de modifier les hotkeys seulement pour un seul émulateur. Pour cela, il faudra ajouter, au début du nom du fichier, le nom de l'émulateur, par exemple "`pcsx2_controller_hotkeys.yml`".
{% endhint %}

Ci-après la liste des émulateurs permettant la modification des hotkeys :

<details>

<summary>Émulateurs avec hotkeys personnalisables :</summary>

* RetroArch
* Ares
* BigPEmu
* Bizhawk
* DesMUME
* Dolphin
* Duckstation
* Flycast
* JGenesis
* Mednafen
* MelonDS
* Mesen
* PCSX2
* PPSSPP
* Project64
* Raine
* Snes9X

</details>

{% hint style="warning" %}
Les fichiers utilisent le nommage RetroArch pour les hotkeys, même pour les autres émulateurs.
{% endhint %}

### Remappage des hotkeys pour manette <a href="#remap-controller-hotkeys" id="remap-controller-hotkeys"></a>

Copier le fichier **controller\_hotkeys.yml** dans le dossier `\user\inputmapping\` de votre installation RetroBat.

Ouvrir le fichier avec votre éditeur de texte préféré :

<div align="left"><figure><img src="../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure></div>

Le fichier est formaté en yml, **par défaut toutes les valeurs sont commentées**.

La première chose à faire est de dé-commenter la section actuelle ou les boutons sont définis, ainsi que la section container. Pour cela, il faut supprimer le caractère # de toutes les lignes situées a partir de la ligne `#default:` incluant cette dernière :

<div align="left"><figure><img src="../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure></div>

Dans cet exemple, nous allons replacer les hotkeys d'**avance rapide** et de **rembobinage** sur les boutons R1 et L1, et déplacer les actions d'**éjection de disque** et de **service AI** vers le d-pad :

Pour cela, il faut assigner la fonction de **rembobinage** sur pageup (L1) et la fonction d'**avance rapide maintenu** sur pagedown (R1), puis assigner la fonction d’**éjection de disque** et de **service AI** sur les boutons d-pad correspondant (gauche et droite) :

<div align="left"><figure><img src="../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure></div>

Puis, sauvegarder le fichier dans le dossier `\user\inputmapping` de votre installation RetroBat :

<div align="left"><figure><img src="../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure></div>

Vous pouvez également spécifier des mappages spécifiques pour un cœur en particulier (dans le cas ou l’émulateur utilise des cœurs différents : Ares, Bizhawk, RetroArch...). Dans l'exemple ci-dessous, le mappage est différent avec le cœur flycast, pour lequel l'avance rapide s'active par pression unique du bouton, au lieu d'une activation en restant appuyé sur le bouton par défaut :

<div align="left"><figure><img src="../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure></div>

### Remappage des hotkeys pour clavier <a href="#remap-controller-hotkeys" id="remap-controller-hotkeys"></a>

Copier le fichier **kb\_hotkeys.yml** dans le dossier `\user\inputmapping\` de votre installation RetroBat.

Ouvrir le fichier avec votre éditeur de texte préféré :

<div align="left"><figure><img src="../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure></div>

Le fichier est formaté en yml, **par défaut toutes les valeurs sont commentées**.

La première chose à faire est de dé-commenter la section actuelle ou les boutons sont définis, ainsi que la section container. Pour cela, il faut supprimer le caractère # de toutes les lignes situées a partir de la ligne `#default:` incluant celle-ci :

<div align="left"><figure><img src="../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure></div>

Puis sauvegarder le fichier :

<div align="left"><figure><img src="../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure></div>

Vous pouvez également spécifier des mappages spécifiques pour un cœur en particulier (dans le cas ou l’émulateur utilise des cœurs différents : Ares, Bizhawk, RetroArch...). Dans l'exemple ci-dessous, le mappage est différent avec le cœur flycast, pour lequel l'avance rapide s'active par pression unique du bouton, au lieu d'une activation en restant appuyé sur le bouton par défaut :

<div align="left"><figure><img src="../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure></div>
