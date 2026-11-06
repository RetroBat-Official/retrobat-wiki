# Configuration des manettes

RetroBat configure vos manettes en deux étapes :

1. **Dans RetroBat (EmulationStation)** : votre manette est reconnue et ses boutons sont connus. Cette étape n'est faite qu'une fois par modèle de manette.
2. **À chaque lancement de jeu (autoconfiguration)** : RetroBat écrit la configuration de vos manettes dans l'émulateur, pour que vous puissiez jouer sans configurer chaque émulateur.

Pour la plupart des manettes de marque (Xbox, PlayStation, Switch Pro, 8BitDo…), il n'y a rien à faire : les deux étapes sont automatiques.

## Configurer une manette dans RetroBat

Les manettes connues sont configurées automatiquement. Pour configurer une manette non reconnue, ou modifier sa configuration, allez dans **MENU PRINCIPAL > PARAMÈTRES DES MANETTES > CONFIGURER UNE MANETTE**, puis **maintenez un bouton** de la manette à configurer :

<div align="left"><figure><img src="../.gitbook/assets/image (373).png" alt=""><figcaption></figcaption></figure></div>

L'écran de configuration demande chaque entrée l'une après l'autre :

<div align="left"><figure><img src="../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure></div>

* **Configurez les boutons selon leur position**, pas selon leur inscription : SUD est le bouton du bas, EST celui de droite, etc. (voir le tableau ci-dessous).
* **Passez** une entrée que votre manette n'a pas en **maintenant un bouton** pendant une seconde.
* Entrées obligatoires : **SUD**, **EST**, la **croix directionnelle** (si votre manette en a une) et **RACCOURCI** (HOTKEY). Si votre manette n'a pas de bouton dédié pour RACCOURCI, utilisez **SÉLECTIONNER** (SELECT).
* À la fin, appuyez sur **SUD** pour valider.

| Entrée RetroBat                                 | Xbox                                                       | PlayStation                        | Nintendo               |
| ----------------------------------------------- | ---------------------------------------------------------- | ---------------------------------- | ---------------------- |
| SUD ![](<../.gitbook/assets/image (367).png>)   | A                                                          | ✕ (Croix)                          | B                      |
| EST ![](<../.gitbook/assets/image (368).png>)   | B                                                          | ○ (Rond)                           | A                      |
| NORD ![](<../.gitbook/assets/image (369).png>)  | Y                                                          | △ (Triangle)                       | X                      |
| OUEST ![](<../.gitbook/assets/image (370).png>) | X                                                          | □ (Carré)                          | Y                      |
| DÉMARRER (START)                                | Menu ![](<../.gitbook/assets/image (371).png>) / Start     | Options                            | +                      |
| SÉLECTIONNER (SELECT)                           | Affichage ![](<../.gitbook/assets/image (372).png>) / Back | Share / Create                     | −                      |
| PAD DIRECTIONNEL                                | Croix                                                      | Croix                              | Croix                  |
| L1 / R1                                         | LB / RB                                                    | L1 / R1                            | L / R                  |
| L2 / R2                                         | LT / RT                                                    | L2 / R2                            | ZL / ZR                |
| STICK GAUCHE / STICK DROIT                      | Sticks gauche / droit                                      | Sticks gauche / droit              | Sticks gauche / droit  |
| CLIC STICK GAUCHE / CLIC STICK DROIT            | Clic des sticks (L3 / R3)                                  | L3 / R3                            | Clic des sticks        |
| RACCOURCI (HOTKEY)                              | SELECT (Affichage), ou un bouton dédié                     | SELECT (Share), ou un bouton dédié | − , ou un bouton dédié |

La configuration est enregistrée pour ce modèle de manette dans `emulationstation\.emulationstation\es_input.cfg`.

### Ordre des joueurs

L'ordre des manettes (joueur 1, joueur 2…) se règle dans **MENU PRINCIPAL > PARAMÈTRES DES MANETTES > ORDRE DES MANETTES**, avec **MANETTE J1**, **MANETTE J2**…

<div align="left"><figure><img src="../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure></div>

## Autoconfiguration dans les émulateurs

À chaque lancement de jeu, RetroBat écrit la configuration des manettes branchées dans l'émulateur (RetroArch et la plupart des émulateurs standalone) : boutons, raccourcis, ordre des joueurs.

{% hint style="warning" %}
Tant que l'autoconfiguration est active, la configuration des manettes de l'émulateur est **réécrite à chaque lancement** : un mappage fait à la main dans l'émulateur est perdu au lancement suivant. Pour garder votre propre configuration, désactivez l'autoconfiguration (voir ci-dessous).
{% endhint %}

### Désactiver l'autoconfiguration

L'autoconfiguration peut être désactivée globalement, pour un système ou pour un jeu, avec l'option **AUTOCONFIGURER LES MANETTES** :

* **Globalement** : **MENU PRINCIPAL > PARAMÈTRES DES JEUX > AUTOCONFIGURER LES MANETTES** : **NON**.

<div align="left"><figure><img src="../.gitbook/assets/image (376).png" alt=""><figcaption></figcaption></figure></div>

* **Pour un système** : ouvrez les [Options d'affichage](../navigation/view-options.md) du système, **CONFIGURATION AVANCÉE DU SYSTÈME > AUTOCONFIGURER LES MANETTES** : **NON**.

<div align="left"><figure><img src="../.gitbook/assets/image (377).png" alt=""><figcaption></figcaption></figure></div>

* **Pour un jeu** : ouvrez les [Options du jeu](../navigation/game-options.md), **CONFIGURATION AVANCÉE DU JEU > AUTOCONFIGURER LES MANETTES** : **NON**.

<div align="left"><figure><img src="../.gitbook/assets/image (378).png" alt=""><figcaption></figcaption></figure></div>

Puis régler l'option **AUTOCONFIGURER LES MANETTES**  sur **NON.**

<div align="left"><figure><img src="../.gitbook/assets/image (379).png" alt=""><figcaption></figcaption></figure></div>

Configurez ensuite vos manettes **directement dans l'émulateur** :

* les émulateurs standalone peuvent être ouverts depuis le système **RETROBAT** de la Vue Systèmes ;
* dans RetroArch, ouvrez le menu pendant le jeu (**RACCOURCI + SUD** ou **F1**) puis **Commandes**.

{% hint style="warning" %}
**Pistolets** : désactiver **AUTOCONFIGURER LES MANETTES** n'empêche pas RetroBat de configurer les pistolets. Pour garder votre propre configuration des pistolets, réglez aussi **ACTIVER LES PISTOLETS** (configuration avancée > **PISTOLETS**) sur **NON** pour le même système ou jeu.
{% endhint %}

## Adapter les contrôles sans désactiver l'autoconfiguration

RetroBat propose plusieurs façons d'adapter les contrôles tout en gardant l'autoconfiguration :

<table><thead><tr><th width="235.75">Besoin</th><th width="279.25">Solution</th><th>Page</th></tr></thead><tbody><tr><td>Changer un raccourci</td><td>Fichiers de raccourcis <code>kb_hotkeys.yml</code> / <code>controller_hotkeys.yml</code></td><td><a href="../navigation/hotkeys.md">Raccourcis</a></td></tr><tr><td>Jouer aux jeux d'arcade avec un stick arcade</td><td>Option <strong>DISPOSITION DES BOUTONS</strong></td><td><a href="supported-controllers/arcade-sticks.md">Sticks Arcade</a></td></tr><tr><td>Choisir une autre disposition de boutons pour une console</td><td>Options de disposition du système (ex. Saturn <strong>BUTTON LAYOUT</strong>)</td><td>Page du système dans <a href="../systemes-and-emulateurs/supported-game-systems/">Systèmes compatibles</a></td></tr><tr><td>Changer le mappage d'un jeu ou d'un core</td><td>Fichiers de mappage dans <code>user\inputmapping</code></td><td><a href="configuration-des-touches-specifique-par-emulateur/">Configuration des touches par émulateur</a>, <a href="../systemes-and-emulateurs/arcade-guide.md">Guide Arcade</a></td></tr><tr><td>Utiliser une manette ou un adaptateur N64, Megadrive, Saturn, GameCube</td><td>Contrôleurs spéciaux</td><td><a href="supported-controllers/gamepads/controleurs-speciaux.md">Contrôleurs spéciaux</a></td></tr><tr><td>Jouer aux jeux d'ordinateur avec une manette</td><td>PadToKey</td><td><a href="supported-controllers/keyboard.md">Clavier</a></td></tr></tbody></table>

### Comment fonctionne un fichier de mappage : deux exemples

#### Flycast (standalone)

Le fichier `flycast_Arcade.yml` contient le mappage de nombreux jeux Naomi, Naomi 2 et Atomiswave. Chaque bloc correspond à un jeu (les jeux d'arcade ont toujours le même nom de rom, le mappage est donc toujours appliqué) :

<div align="left"><figure><img src="../.gitbook/assets/image (380).png" alt=""><figcaption></figcaption></figure></div>

Par exemple, `l2: btn_trigger_left` signifie que la gâchette gauche de votre manette est affectée à l'entrée `btn_trigger_left` de Flycast. RetroBat convertit L2 en ce que votre manette utilise réellement (axe ou bouton) :

<div align="left"><figure><img src="../.gitbook/assets/image (381).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (382).png" alt=""><figcaption></figcaption></figure></div>

#### RetroArch (core Flycast)

Le fichier `libretro_flycast_naomi.yml` contient, pour chaque jeu Naomi, le remappage des boutons du RetroPad de RetroArch vers les entrées du core :

<div align="left"><figure><img src="../.gitbook/assets/image (383).png" alt=""><figcaption></figcaption></figure></div>

Par exemple, `btn_b: 4` signifie que le bouton SUD du RetroPad envoie l'entrée n° 4 du core (ici, DRIVE GEAR) :

<div align="left"><figure><img src="../.gitbook/assets/image (384).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (385).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Pour RetroArch, ces fichiers ne modifient pas le mappage entre votre manette et le RetroPad : RetroBat crée un **fichier de remap du core** dans `emulators\retroarch\config\remaps\<nom du core>`.
{% endhint %}

## Résoudre un problème de manette

1. **Reconfigurez votre manette** dans **PARAMÈTRES DES MANETTES > CONFIGURER UNE MANETTE**, selon la position des boutons.
2. **Vérifiez l'ordre des joueurs** dans **ORDRE DES MANETTES**.
3. **Vérifiez qu'AUTOCONFIGURER LES MANETTES n'est pas sur NON** (globalement, pour le système ou pour le jeu).
4. Lancez le jeu et ouvrez `emulationstation\emulatorLauncher.log` : il indique les manettes détectées et la configuration écrite.
5. Si le problème persiste, désactivez l'autoconfiguration, configurez la manette directement dans l'émulateur et gardez le fichier de configuration qu'il crée.
6. Contactez l'équipe RetroBat (Discord ou GitHub) avec `es_input.cfg`, `emulatorLauncher.log` et les fichiers de configuration de l'émulateur des étapes 4 et 5.
