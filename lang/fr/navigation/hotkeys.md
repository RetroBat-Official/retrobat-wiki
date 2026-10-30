# Raccourcis

Les raccourcis (« hotkeys ») sont des combinaisons de touches à la manette ou au clavier qui permettent de réaliser des actions en jeu : sauvegarder ou charger votre progression (sauvegardes instantanées), mettre en pause, rembobiner, faire une capture d'écran… Le plus utilisé est **HOTKEY + START**, qui quitte le jeu et revient à RetroBat.

{% hint style="info" %}
**Utiliser un raccourci à la manette :** maintenez le bouton **HOTKEY** appuyé (le bouton défini lors de la configuration de votre manette, **SELECT** par défaut), puis appuyez sur le second bouton du raccourci.

Au clavier, les raccourcis sont des touches simples (pas besoin de touche HOTKEY).
{% endhint %}

## Raccourcis par défaut

L'équipe RetroBat a défini un jeu de raccourcis commun, pour que les mêmes raccourcis fonctionnent dans un maximum d'émulateurs.

Les boutons de manette sont désignés par leur position : **Sud** = B (Nintendo) / ✕ (PlayStation) / A (Xbox), **Est** = A / ◯ / B, **Ouest** = Y / ▢ / X, **Nord** = X / △ / Y.

| Action                                                        | Manette               | Clavier                         |
| ------------------------------------------------------------- | --------------------- | ------------------------------- |
| Quitter le jeu                                                | HOTKEY + START        | `Échap`                         |
| [Game Control Center](game-control-center.md)                 | HOTKEY + Est          | `Ctrl` + `F12`                  |
| Menu de l'émulateur (ou pause si l'émulateur n'a pas de menu) | HOTKEY + Sud          | `F1`                            |
| Sauvegarde instantanée                                        | HOTKEY + Ouest        | `F2`                            |
| Chargement instantané                                         | HOTKEY + Nord         | `F4`                            |
| Emplacement de sauvegarde précédent                           | HOTKEY + Croix bas    | `F6`                            |
| Emplacement de sauvegarde suivant                             | HOTKEY + Croix haut   | `F7`                            |
| Rembobiner                                                    | HOTKEY + Croix gauche | `Retour arrière`                |
| Avance rapide (maintenir)                                     | HOTKEY + Croix droite | `L`                             |
| Avance rapide (activer / désactiver)                          | (\*)                  | `Espace`                        |
| Capture d'écran                                               | HOTKEY + R3           | `F8`                            |
| Éjecter / insérer le disque                                   | HOTKEY + L1           |                                 |
| Disque précédent                                              | HOTKEY + L2           | `F9`                            |
| Disque suivant                                                | HOTKEY + R2           | `F10`                           |
| Service de traduction IA                                      | HOTKEY + R1           |                                 |
| Pause ou plein écran (selon l'émulateur)                      | HOTKEY + L3           | `P` (pause) / `F` (plein écran) |
| Plein écran                                                   |                       | `F`                             |
| Avance image par image                                        |                       | `K`                             |
| Shader suivant / précédent                                    |                       | `M` / `N`                       |
| Couper le son                                                 |                       | `O`                             |
| Capturer / libérer la souris                                  |                       | `F11`                           |
| Game Focus (RetroArch, voir plus bas)                         |                       | `Arrêt défil`                   |

(\*) L'avance rapide de **HOTKEY + Croix droite** peut passer du mode « maintenir » au mode « activer / désactiver » avec l'option d'avance rapide des paramètres avancés du système ou du jeu.

{% hint style="info" %}
Tous les émulateurs ne gèrent pas toutes ces actions : chaque émulateur reçoit uniquement les actions qu'il sait réaliser.
{% endhint %}

### Émulateurs utilisant les raccourcis par défaut

<details>

<summary>Émulateurs avec raccourcis alignés</summary>

Les émulateurs marqués ✏️ sont personnalisables (voir Personnaliser les raccourcis).

* RetroArch (tous les cores libretro) ✏️
* ArcadeDuck ✏️
* ares ✏️ (utilise PadToKey)
* Azahar (plein écran sur `F1`)
* BigPEmu ✏️ (uniquement menu, avance rapide, rembobinage, sauvegarde/chargement, capture)
* BizHawk ✏️ (utilise PadToKey)
* BlastEm ✏️ (utilise PadToKey)
* CGenius ✏️ (uniquement sauvegarde/chargement, utilise PadToKey)
* Citron
* Demul
* DeSmuME ✏️ (utilise PadToKey)
* Dhewm3
* Dolphin ✏️
* DuckStation ✏️
* Eden
* Flycast ✏️
* Hatari
* Jgenesis ✏️ (utilise PadToKey)
* MAME
* Mednafen ✏️
* melonDS ✏️ (utilise PadToKey)
* Mesen ✏️
* Model3-Vulkan ✏️ (utilise PadToKey)
* Mupen64 (RMG)
* OpenMSX
* PCSX2 / PCSX2x6 ✏️
* PPSSPP ✏️
* Project64 ✏️ (utilise PadToKey)
* Raine ✏️ (utilise PadToKey)
* SM2-emu ✏️ (utilise PadToKey)
* Snes9x ✏️ (utilise PadToKey)
* Sudachi
* Suyu
* Ymir (quitter avec `Ctrl` + `Q`)
* Yuzu

</details>

{% hint style="info" %}
« Utilise PadToKey » signifie que l'émulateur n'a pas de raccourcis manette propres : RetroBat convertit vos raccourcis manette en touches clavier correspondantes.
{% endhint %}

{% hint style="warning" %}
**Un émulateur propose des raccourcis mais ne suit pas ce modèle ?** Merci de le signaler à l'équipe RetroBat sur [Discord](https://discord.gg/GVcPNxwzuT) ou sur le [forum](https://retrobat.forumgaming.fr/), pour qu'il soit aligné dans une prochaine version.
{% endhint %}

## Systèmes « ordinateurs » et raccourcis clavier

Sur les systèmes ordinateurs (Amiga, Amstrad CPC, Atari ST, Commodore 64, MSX, ZX Spectrum, DOS, PC-98, X68000…), l'ordinateur émulé a souvent besoin de tout le clavier, y compris des touches de fonction. Les raccourcis clavier peuvent alors entrer en conflit avec le jeu, ou être désactivés par l'émulateur.

* **Utilisez de préférence les raccourcis manette** (HOTKEY + bouton) : ils n'utilisent pas le clavier.
* Dans **RetroArch**, appuyez sur `Arrêt défil` pour activer le **Game Focus** : toutes les touches du clavier sont envoyées à l'ordinateur émulé, et les raccourcis clavier sont désactivés. Appuyez à nouveau sur `Arrêt défil` pour les retrouver.
* Certains émulateurs autonomes utilisent des raccourcis modifiés pour ces systèmes (par exemple `Alt` + touche dans OpenMSX).

## Personnaliser les raccourcis

RetroBat permet de modifier les raccourcis par défaut de plusieurs émulateurs, au clavier et à la manette, grâce à deux fichiers fournis dans le dossier `system\resources\inputmapping` de RetroBat :

* **kb\_hotkeys.yml** : raccourcis clavier
* **controller\_hotkeys.yml** : raccourcis manette

<details>

<summary>Émulateurs avec raccourcis personnalisables</summary>

ArcadeDuck, ares, BigPEmu, BizHawk, BlastEm, CGenius, DeSmuME, Dolphin, DuckStation, Flycast, Jgenesis, Mednafen, melonDS, Mesen, Model3-Vulkan, PCSX2, PPSSPP, Project64, Raine, RetroArch, SM2-emu, Snes9x.

</details>

{% hint style="warning" %}
**Ne modifiez jamais les fichiers de `system\resources\inputmapping`** : ils sont remplacés à chaque mise à jour. Copiez-les dans le dossier `user\inputmapping` de RetroBat et modifiez la copie.
{% endhint %}

### Quel fichier est utilisé ?

Vous pouvez créer un fichier pour tous les émulateurs, ou un fichier pour un seul émulateur en ajoutant son nom au début du nom de fichier (par exemple `pcsx2_controller_hotkeys.yml` ou `retroarch_kb_hotkeys.yml`).

RetroBat utilise le premier fichier trouvé, dans cet ordre :

1. `user\inputmapping\<émulateur>_kb_hotkeys.yml` (ou `_controller_hotkeys.yml`)
2. `system\resources\inputmapping\<émulateur>_kb_hotkeys.yml`
3. `user\inputmapping\kb_hotkeys.yml`
4. `system\resources\inputmapping\kb_hotkeys.yml`

<details>

<summary>Noms d'émulateurs à utiliser dans les noms de fichiers</summary>

`arcadeduck`, `ares`, `bigpemu`, `bizhawk`, `blastem`, `cgenius`, `desmume`, `dolphin`, `duckstation`, `flycast`, `jgenesis`, `mednafen`, `melonds`, `mesen`, `model3-vulkan`, `pcsx2`, `ppsspp`, `project64`, `raine`, `retroarch`, `sm2-emu`, `snes9x`

</details>

### Structure des fichiers

Ce sont des fichiers texte au format YAML : ouvrez-les avec n'importe quel éditeur de texte (Bloc-notes, Notepad++…). Dans les fichiers fournis, **toutes les lignes sont commentées** (elles commencent par `#`) : elles montrent seulement les valeurs par défaut.

Les lignes sont regroupées dans des **conteneurs** :

* Le conteneur `default:` s'applique à tous les jeux.
* Un conteneur portant le nom d'un **core** (par exemple `fceumm:` ou `flycast:`) s'applique uniquement à ce core. C'est utile pour les émulateurs qui ont plusieurs cores ou systèmes : RetroArch, ares, BizHawk, BlastEm, Jgenesis, Mednafen, Mesen.
* Pour les raccourcis manette de RetroArch, un conteneur peut aussi porter le nom d'un **système** (par exemple `nes:`).

Si aucun conteneur ne correspond au core ou au système, le conteneur `default` est utilisé.

{% hint style="warning" %}
* L'indentation est importante : les lignes d'un conteneur doivent commencer par **deux espaces**, jamais par une tabulation.
* Les noms d'actions sont toujours ceux de **RetroArch**, même pour les autres émulateurs : RetroBat les convertit automatiquement.
{% endhint %}

### Modifier les raccourcis manette

Dans `controller_hotkeys.yml`, chaque ligne s'écrit `bouton: action`.

| Nom du bouton                    | Bouton                    |
| -------------------------------- | ------------------------- |
| `a`                              | Sud                       |
| `x`                              | Nord                      |
| `y`                              | Ouest                     |
| `start`                          | START                     |
| `pageup` / `pagedown`            | L1 / R1                   |
| `l2` / `r2`                      | L2 / R2                   |
| `l3` / `r3`                      | Clic stick gauche / droit |
| `up` / `down` / `left` / `right` | Croix directionnelle      |

{% hint style="info" %}
Le bouton `b` (Est) ne peut pas être utilisé : HOTKEY + Est est réservé au Game Control Center.
{% endhint %}

| Nom de l'action                               | Action                                         |
| --------------------------------------------- | ---------------------------------------------- |
| `exit_emulator`                               | Quitter le jeu                                 |
| `menu_toggle`                                 | Menu de l'émulateur                            |
| `pause_toggle`                                | Pause                                          |
| `save_state` / `load_state`                   | Sauvegarde / chargement instantané             |
| `state_slot_increase` / `state_slot_decrease` | Emplacement suivant / précédent                |
| `rewind`                                      | Rembobiner                                     |
| `hold_fast_forward` / `toggle_fast_forward`   | Avance rapide (maintenir / activer-désactiver) |
| `screenshot`                                  | Capture d'écran                                |
| `disk_eject_toggle`                           | Éjecter / insérer le disque                    |
| `disk_prev` / `disk_next`                     | Disque précédent / suivant                     |
| `ai_service`                                  | Service de traduction IA                       |

**Exemple :** placer le **rembobinage** et l'**avance rapide** sur L1 et R1, et déplacer l'**éjection du disque** et le **service IA** sur la croix directionnelle.

1. Copiez `controller_hotkeys.yml` de `system\resources\inputmapping` vers `user\inputmapping`.
2. Ouvrez la copie, supprimez le `#` au début de la ligne `#default:` et de toutes les lignes du conteneur par défaut en dessous.
3. Modifiez les lignes souhaitées :

```yaml
default:
  start: exit_emulator
  a: menu_toggle
  x: load_state
  y: save_state
  pageup: rewind
  pagedown: hold_fast_forward
  l2: disk_prev
  r2: disk_next
  r3: screenshot
  up: state_slot_increase
  down: state_slot_decrease
  left: disk_eject_toggle
  right: ai_service
```

4. Enregistrez le fichier.

{% hint style="warning" %}
Gardez toujours **tous** les raccourcis que vous voulez utiliser dans le conteneur, pas seulement ceux que vous modifiez : pour RetroArch, le conteneur remplace toute la liste par défaut. Par exemple, `start: exit_emulator` doit rester dans la liste, sinon HOTKEY + START ne quittera plus le jeu.
{% endhint %}

**Exemple pour un seul core :** avance rapide en mode « activer / désactiver » au lieu de « maintenir » avec le core Flycast, et conteneur par défaut pour tous les autres cores :

```yaml
default:
  start: exit_emulator
  a: menu_toggle
  x: load_state
  y: save_state
  pageup: disk_eject_toggle
  pagedown: ai_service
  l2: disk_prev
  r2: disk_next
  r3: screenshot
  up: state_slot_increase
  down: state_slot_decrease
  left: rewind
  right: hold_fast_forward

flycast:
  start: exit_emulator
  a: menu_toggle
  x: load_state
  y: save_state
  left: rewind
  right: toggle_fast_forward
```

{% hint style="info" %}
**RetroArch uniquement — raccourcis à un seul bouton :** ajouter la ligne `noHotkey: true` dans un conteneur désactive le bouton HOTKEY pour les cores concernés : chaque raccourci se déclenche alors avec **son bouton seul** (par exemple START seul quitte le jeu). À réserver aux systèmes dont les jeux n'utilisent pas ces boutons.
{% endhint %}

### Modifier les raccourcis clavier

Dans `kb_hotkeys.yml`, chaque ligne s'écrit dans l'autre sens : `action: touche`, et les noms d'actions commencent par `input_`.

**Exemple :** sauvegarde instantanée sur `F5` et chargement sur `F9`.

1. Copiez `kb_hotkeys.yml` de `system\resources\inputmapping` vers `user\inputmapping`.
2. Ouvrez la copie, supprimez le `#` au début de la ligne `#default:` et de toutes les lignes en dessous.
3. Modifiez les lignes souhaitées :

```yaml
default:
  input_menu_toggle: f1
  input_toggle_fullscreen: f
  input_hold_fast_forward: l
  input_rewind: backspace
  input_toggle_fast_forward: space
  input_frame_advance: k
  input_screenshot: f8
  input_save_state: f5
  input_load_state: f9
  input_state_slot_decrease: f6
  input_state_slot_increase: f7
  input_pause_toggle: p
  input_exit_emulator: escape
  input_shader_next: m
  input_shader_prev: n
  input_disk_prev: f3
  input_disk_next: f10
  input_game_focus_toggle: scroll_lock
  input_grab_mouse_toggle: f11
  input_audio_mute: o
```

4. Enregistrez le fichier.

{% hint style="info" %}
* Les noms de touches suivent le nommage RetroArch : `a` à `z`, `f1` à `f12`, `escape`, `enter`, `space`, `backspace`, `tab`, `insert`, `del`, `home`, `end`, `pageup`, `pagedown`, `up`, `down`, `left`, `right`, `scroll_lock`…
* Si une touche n'est pas prise en charge par un émulateur, sa touche par défaut est utilisée à la place.
* Pour les émulateurs qui **utilisent PadToKey**, les raccourcis manette envoient la touche clavier : si vous modifiez une touche dans `kb_hotkeys.yml`, le raccourci manette correspondant suit automatiquement.
{% endhint %}
