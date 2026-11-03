# Contrôleurs spéciaux

Pour certains systèmes, RetroBat reconnaît les manettes qui reproduisent la manette d'origine de la console (manettes N64, manettes de type Megadrive/Saturn, adaptateurs GameCube…) et les configure **bouton pour bouton**, afin que chaque bouton fasse exactement ce qu'il faisait sur la console d'origine.

Ces mappages sont stockés dans des fichiers `.json`. RetroBat fournit déjà les mappages des manettes listées sur cette page, et vous pouvez ajouter les vôtres.

{% hint style="info" %}
Quand un contrôleur spécial est détecté, le mappage configuré dans RetroBat (PARAMÈTRES DES MANETTES) est ignoré pour cette manette : c'est le mappage du fichier `.json` qui est utilisé.
{% endhint %}

## Fonctionnement

RetroBat identifie la manette grâce à son **GUID** (et, pour RetroArch, grâce au pilote d'entrée utilisé). Deux cas existent :

<table><thead><tr><th width="169">Cas</th><th>Comportement</th></tr></thead><tbody><tr><td><strong>Automatique</strong></td><td>Manettes avec un identifiant unique (adaptateurs, manettes 8BitDo en mode D-input, manette N64 Nintendo Switch Online…). Le mappage spécial est appliqué dès que la manette est branchée.</td></tr><tr><td><strong>Activation requise</strong></td><td>Manettes qui partagent leur identifiant avec des manettes standard (par exemple une 8BitDo M30 en mode X-input est vue comme une manette Xbox 360). Le mappage spécial n'est appliqué que si vous activez l'option correspondante dans la configuration avancée du système, sous-menu <strong>CONTRÔLES</strong>.</td></tr></tbody></table>

{% hint style="warning" %}
N'activez les options **UTILISER UNE MANETTE DE TYPE xxx** que si vous jouez réellement avec une des manettes listées ci-dessous. Sinon, une manette Xbox ou Switch classique risque de recevoir le mappage spécial et ses boutons seront faux.
{% endhint %}

Pour vérifier qu'un mappage spécial a bien été appliqué, ouvrez `emulationstation\emulatorLauncher.log` après avoir lancé un jeu et cherchez une ligne du type `Performing specific … mapping for <nom de la manette>`.

## Fichiers de mappage

Les fichiers se trouvent dans `system\resources\inputmapping` :

<table><thead><tr><th width="230.25">Fichier</th><th>Systèmes</th></tr></thead><tbody><tr><td><code>n64Controllers.json</code></td><td>Nintendo 64</td></tr><tr><td><code>mdControllers.json</code></td><td>Megadrive / Genesis, Mega-CD / Sega CD, 32X</td></tr><tr><td><code>saturnControllers.json</code></td><td>Saturn</td></tr><tr><td><code>GCControllers.json</code></td><td>GameCube</td></tr><tr><td><code>3doControllers.json</code></td><td>3DO</td></tr><tr><td><code>arcade_sticks.json</code></td><td>Mappage personnalisé des sticks arcade (RetroArch)</td></tr><tr><td><code>kbpads\*.yml</code></td><td>Sticks arcade reconnus comme un clavier (I-PAC2, X-Arcade Tankstick)</td></tr></tbody></table>

{% hint style="info" %}
Si vous modifiez un fichier, copiez-le dans `user\inputmapping` (`user\inputmapping\kbpads` pour les fichiers `.yml`) et modifiez la copie. RetroBat lit ce dossier en priorité, et il n'est pas écrasé lors des mises à jour.
{% endhint %}

## Nintendo 64

<table><thead><tr><th>Manette</th><th width="90.5" align="center">RetroArch</th><th width="76.75" align="center">Ares</th><th width="83" align="center">BizHawk</th><th width="76.75" align="center">RMG</th><th width="90.5" align="center">Simple64</th><th width="99.25" align="center">Ports Ship</th></tr></thead><tbody><tr><td>Manette N64 Nintendo Switch Online</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td></tr><tr><td>Manette 8BitDo N64</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">–</td></tr><tr><td>Adaptateur N64 Mayflash</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td></tr><tr><td>Adaptateur N64 Raphnet</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td><td align="center">Auto</td></tr><tr><td>SWITCH CO.LTD. USB Controller (D-input/SDL)</td><td align="center">Auto</td><td align="center">–</td><td align="center">Auto</td><td align="center">–</td><td align="center">–</td><td align="center">–</td></tr><tr><td>SWITCH CO.LTD. USB Controller (X-input)</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">Option</td><td align="center">–</td></tr></tbody></table>

* **RetroArch** : cores Mupen64Plus-Next et ParaLLEl N64.
* **BizHawk** : cores Ares64 et Mupen64Plus.
* **RMG** : Rosalie's Mupen GUI (Mupen64Plus).
* **Ports Ship** : Ship of Harkinian, 2 Ship 2 Harkinian, Ghostship.
* **Option** : **UTILISER UNE MANETTE DE TYPE N64** (configuration avancée du système > CONTRÔLES).

### INVERSER LA GÂCHETTE Z (N64)

Sur les manettes avec deux gâchettes (manette N64 Nintendo Switch Online, manette 8BitDo N64), le bouton **Z** est placé par défaut sur la gâchette gauche. Activez **INVERSER LA GÂCHETTE Z (N64)** pour utiliser la gâchette droite à la place.

C'est une option globale : **PARAMÈTRES DES JEUX > CONTRÔLES > CONTRÔLEURS SPÉCIAUX > INVERSER LA GÂCHETTE Z (N64)**. Elle fonctionne avec RetroArch, Ares, BizHawk, RMG et Simple64.

<div align="left"><figure><img src="../../../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure></div>

## Megadrive / Genesis (et Mega-CD, 32X)

Manette prise en charge : **8BitDo M30** (le mode dépend de la façon dont elle est connectée et allumée ; voir la page [Manettes](./)).

<table><thead><tr><th width="250.25">Mode de la M30</th><th>Activation</th></tr></thead><tbody><tr><td>X-input</td><td>Option</td></tr><tr><td>Switch</td><td>Option</td></tr><tr><td>D-input</td><td>Auto</td></tr><tr><td>Récepteur 2.4G</td><td>Auto</td></tr></tbody></table>

* **Émulateurs** : RetroArch (cores Genesis Plus GX, Genesis Plus GX Wide, Genesis Plus GX Expanded et PicoDrive), Ares, BizHawk (Genplus-gx, PicoDrive), BlastEm, Jgenesis, Kega Fusion, Mednafen.
* **Option** : **UTILISER UNE MANETTE DE TYPE MEGADRIVE** (configuration avancée du système > CONTRÔLES). Dans Kega Fusion, l'option permet de choisir **OUI(MODE DPAD)** ou **OUI(MODE STICK ANALOGIQUE)**.

## Saturn

Manette prise en charge : **8BitDo M30**.

| Mode de la M30 | RetroArch | BizHawk | Mednafen | Kronos |         SSF        | YabaSanshiro |        Ymir        |
| -------------- | :-------: | :-----: | :------: | :----: | :----------------: | :----------: | :----------------: |
| X-input        |   Option  |  Option |  Option  | Option |       Option       |    Option    |       Option       |
| Switch         |   Option  |  Option |     –    | Option |       Option       |    Option    |       Option       |
| D-input        |    Auto   |   Auto  |   Auto   | Option |        Auto        |    Option    |       Option       |
| Récepteur 2.4G |    Auto   |   Auto  |   Auto   |  Auto  | Non pris en charge |     Auto     | Non pris en charge |

* **RetroArch** : cores Beetle Saturn, Kronos, YabaSanshiro, Yabause et Ymir.
* **BizHawk** : core Saturnus.
* **Option** : **UTILISER UNE MANETTE DE TYPE SATURN** (configuration avancée du système > CONTRÔLES). Dans Kronos, SSF et YabaSanshiro, choisissez **OUI(MODE DPAD)** ou **OUI(MODE STICK ANALOGIQUE)**.

## GameCube

Les mappages spéciaux pour les manettes GameCube sont disponibles uniquement avec **Dolphin** (standalone), pour les systèmes GameCube et Triforce.

| Adaptateur                                     | Activation |
| ---------------------------------------------- | ---------- |
| Mayflash GameCube Controller Adapter (mode PC) | Auto       |
| Adaptateur raphnet Dual GameCube to USB        | Auto       |

L'option **UTILISER UNE MANETTE DE TYPE GAMECUBE** sert aux entrées qui nécessitent une activation (aucune dans le fichier fourni pour l'instant).

### Adaptateur GameCube Wii U (officiel ou Mayflash en mode Wii U)

Dolphin peut utiliser cet adaptateur directement (vibrations prises en charge, 4 ports) :

1. Installez le pilote WinUSB de l'adaptateur avec [Zadig](https://zadig.akeo.ie/), comme expliqué dans le [guide Dolphin](https://dolphin-emu.org/docs/guides/how-use-official-gc-controller-adapter-wii-u/).
2. Dans la configuration avancée du système GameCube > CONTRÔLES, réglez **TYPE DE CONTRÔLEUR JOUEUR 1** (et joueurs 2 à 4 si besoin) sur **ADAPTATEUR GAMECUBE**.

## 3DO

Manette prise en charge : **8BitDo M30**, avec le core **RetroArch Opera**.

<table><thead><tr><th width="226.5">Mode de la M30</th><th>Activation</th></tr></thead><tbody><tr><td>X-input</td><td>Option</td></tr><tr><td>Switch</td><td>Option</td></tr><tr><td>D-input</td><td>Auto</td></tr><tr><td>Récepteur 2.4G</td><td>Auto</td></tr></tbody></table>

**Option** : **UTILISER UNE MANETTE DE TYPE 3DO** (configuration avancée du système > CONTRÔLES).

## Wiimotes (Wii)

Avec **Dolphin** (standalone), l'option **TYPE DE WIIMOTE** (configuration avancée du système Wii > CONTRÔLES) définit la gestion des manettes Wii :

<table><thead><tr><th width="250.25">Valeur</th><th>Comportement</th></tr></thead><tbody><tr><td><strong>RÉELLE</strong> (par défaut)</td><td>Vraies Wiimotes, connectées en Bluetooth ou avec une DolphinBar Mayflash en <strong>mode 4</strong>.</td></tr><tr><td><strong>ÉMULÉE</strong></td><td>Vos manettes servent de Wiimotes. Choisissez le périphérique émulé (Wiimote, Wiimote horizontale, Nunchuk, Classic Controller…) avec <strong>TYPE DE WIIMOTE ÉMULÉE</strong>.</td></tr><tr><td><strong>RÉELLE COMME ÉMULÉE</strong> / <strong>(NUNCHUK)</strong> / <strong>(CC)</strong></td><td>Une vraie Wiimote est utilisée à travers la Wiimote émulée de Dolphin, sans extension, avec un Nunchuk ou avec un Classic Controller.</td></tr></tbody></table>

Autres options utiles :

* **NOMBRE DE WIIMOTES** : force le nombre de Wiimotes détectées par le jeu (réglez-le sur 1 pour les jeux qui passent en multijoueur dès que plusieurs manettes sont connectées).
* **UTILISER DES MANETTES GAMECUBE** : configure aussi vos manettes comme manettes GameCube, pour les jeux Wii qui les prennent en charge.
* **DÉSACTIVER LA RECHERCHE CONTINUE DES WIIMOTES** : RetroBat désactive automatiquement la recherche continue quand une DolphinBar est détectée, quand les Wiimotes sont émulées et pour les jeux GameCube. Cette option permet de forcer le comportement.

Pour utiliser une Wiimote comme pistolet, voir la page [Wiimote et DolphinBar](../lightguns/wiimotedolphinbar.md).

### Sticks arcade reconnus comme un clavier (I-PAC2, X-Arcade Tankstick)

Certains sticks et encodeurs arcade sont vus par Windows comme un **clavier** (Ultimarc I-PAC2, X-Arcade Tankstick…). Leurs touches suivent les touches par défaut de MAME (joueur 1 : flèches, Ctrl gauche, Alt gauche, Espace…, Start `1`, Coin `5` ; joueur 2 : `R`/`F`/`D`/`G`, `A`, `S`…, Start `2`, Coin `6`).

<table><thead><tr><th width="205.25">Émulateur</th><th>Configuration</th></tr></thead><tbody><tr><td><strong>RetroArch</strong></td><td><strong>PARAMÈTRES DES JEUX > OPTIONS RETROARCH > CONTRÔLES > CONFIGURER LES STICKS ARCADE DE TYPE CLAVIER</strong> : choisissez <strong>IPAC2</strong> ou <strong>X-ARCADE TANKSTICK</strong>. S'applique à tous les jeux RetroArch.</td></tr><tr><td><strong>MAME</strong> (standalone, GroovyMAME)</td><td>Configuration avancée du système > CONTRÔLES > <strong>PROFIL DE CONFIGURATION DES MANETTES</strong> : choisissez <strong>IPAC2</strong> ou <strong>X-ARCADE</strong>. Les profils se trouvent dans <code>saves\mame\ctrlr</code> ; vous pouvez aussi créer vos propres profils (<strong>PERSONNALISÉ 1</strong> à <strong>6</strong>) ou un profil par jeu (<strong>PAR JEU</strong>, fichier portant le nom de la rom).</td></tr><tr><td><strong>PCSX2x6</strong> (Namco System 246/256)</td><td>Configuration avancée du système > CONTRÔLES > <strong>CONFIGURER LES STICKS ARCADE DE TYPE CLAVIER</strong>.</td></tr></tbody></table>

Les mappages RetroArch et PCSX2x6 proviennent des fichiers `kbpads\libretro_<type>.yml` et `kbpads\pcsx2x6_<type>.yml`. Chaque fichier contient un bloc `default`, et vous pouvez ajouter des blocs portant le nom d'un **système**, d'un **core** (RetroArch uniquement) ou d'une **rom** (nom du fichier sans extension). Ils sont appliqués dans cet ordre : `default` → système → core → jeu, et il suffit d'indiquer ce qui change.

Exemple (`user\inputmapping\kbpads\libretro_ipac2.yml`) :

```yaml
default:
  input_player1_a: ctrl
  input_player1_b: alt
  # ...
snes:
  input_player1_a: alt
  input_player1_b: ctrl
```

## Mappage personnalisé des sticks arcade (RetroArch)

Pour un stick arcade reconnu comme une **manette**, vous pouvez définir un mappage RetroArch dédié :

1. Copiez `system\resources\inputmapping\arcade_sticks.json` dans `user\inputmapping`.
2. Remplacez l'entrée d'exemple (`Arcade Stick Test`) par le GUID de votre stick et votre mappage.
3. Activez **PARAMÈTRES DES JEUX > OPTIONS RETROARCH > CONTRÔLES > UTILISER UN MAPPING PERSO POUR LES STICKS ARCADE**.

## Ajouter votre propre manette

1. Copiez le fichier `.json` du système dans `user\inputmapping`.
2. Trouvez le GUID de votre manette : c'est la valeur `deviceGUID` dans `emulationstation\.emulationstation\es_input.cfg`.
3. Dupliquez une entrée existante **du même émulateur** (le format du mappage est propre à chaque émulateur) et modifiez `Name`, `Guid` et `Mapping`. Champs principaux :

<table><thead><tr><th width="164">Champ</th><th>Description</th></tr></thead><tbody><tr><td><code>Emulator</code></td><td>Émulateur concerné (<code>libretro</code>, <code>ares</code>, <code>bizhawk</code>, <code>mupen64</code>, <code>dolphin</code>…).</td></tr><tr><td><code>Guid</code></td><td>GUID de la manette ; plusieurs GUID peuvent être séparés par des virgules.</td></tr><tr><td><code>Driver</code></td><td>RetroArch uniquement : pilote d'entrée (<code>xinput</code>, <code>dinput</code>, <code>sdl2</code>). Laisser vide si inutile.</td></tr><tr><td><code>Mapping</code></td><td>Mappage des boutons, au format de l'émulateur.</td></tr><tr><td><code>HotKeyMapping</code></td><td>RetroArch uniquement : raccourcis du joueur 1 avec cette manette.</td></tr><tr><td><code>ControllerInfo</code></td><td>Réglages supplémentaires : <code>needActivationSwitch: "true"</code> rend le mappage dépendant de l'option UTILISER UNE MANETTE DE TYPE xxx ; <code>switch_trigger</code> est le bouton utilisé par INVERSER LA GÂCHETTE Z (N64).</td></tr></tbody></table>

4. Lancez un jeu et vérifiez `emulationstation\emulatorLauncher.log`.

{% hint style="success" %}
Votre mappage fonctionne ? Partagez-le sur le Discord RetroBat ou sur GitHub pour qu'il soit ajouté à RetroBat !
{% endhint %}
