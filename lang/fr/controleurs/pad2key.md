# PadToKey

Avec **PadToKey**, les boutons de votre manette envoient des **touches du clavier** (ou des actions de la souris) au jeu. Utilisez-le pour les jeux qui ne se jouent pas à la manette : anciens jeux d'ordinateur, jeux Windows, certains émulateurs standalone ou portages.

Un profil PadToKey peut être créé pour **tout un système** ou pour **un seul jeu**, jusqu'à 4 joueurs. Pendant le jeu, RetroBat envoie les touches à la fenêtre de l'émulateur.

{% hint style="info" %}
Les options PadToKey n'apparaissent que pour les systèmes et émulateurs qui le gèrent (ordinateurs, DOS, jeux Windows, flippers, portages, certains émulateurs standalone…). Elles ne sont modifiables que lorsque l'interface est en mode **COMPLET**.
{% endhint %}

## Créer ou modifier un profil

### Pour un système

1. Dans la liste des jeux du système, appuyez sur **SELECT** pour ouvrir les [Options d'affichage](../navigation/view-options.md).
2. Sélectionnez **CONFIGURATION AVANCÉE DU SYSTÈME**.
3. Sélectionnez **CRÉER UN PROFIL PADTOKEY** (ou **ÉDITER UN PROFIL PADTOKEY** si le système en a déjà un).

### Pour un jeu

1. Dans la liste des jeux, maintenez **SUD** sur le jeu pour ouvrir les [Options du jeu](../navigation/game-options.md).
2. Sélectionnez **CRÉER UN PROFIL PADTOKEY** (ou **ÉDITER UN PROFIL PADTOKEY**).

Un nouveau profil de jeu part du profil du système, s'il existe : vous ne changez que les touches dont ce jeu a besoin.

### L'éditeur

La fenêtre **CONFIGURATION MANETTE À CLAVIER** liste les boutons de la manette, avec un onglet par joueur (**JOUEUR 1** à **JOUEUR 4**).

<div align="left"><figure><img src="../.gitbook/assets/image (386).png" alt=""><figcaption></figcaption></figure></div>

* Sélectionnez un bouton et appuyez sur **SUD** ![](<../.gitbook/assets/image (387).png>) : un clavier virtuel s'ouvre.
  * Placez-vous sur une touche et appuyez sur **SUD** ![](<../.gitbook/assets/image (388).png>) pour l'affecter.
  * Pour envoyer plusieurs touches en même temps (ex. **Maj + F1**), appuyez sur **NORD** (**AJOUTER UNE COMBINAISON DE TOUCHES**) sur chaque touche supplémentaire, puis sur **SUD** sur la dernière.
  * Appuyez sur **OUEST** (**RÉINITIALISER**) pour retirer la touche du bouton.
  * Les boutons de la souris sont à droite du clavier virtuel.
* **COMBINAISONS** : affectez des touches à **HOTKEY + START**, **HOTKEY + SUD**, **HOTKEY + EST**, **HOTKEY + NORD** ou **HOTKEY + OUEST**.
* **POINTEUR DE SOURIS** > **ÉMULER LE POINTEUR DE SOURIS** : déplace le pointeur de la souris avec le **STICK ANALOGIQUE GAUCHE** ou le **STICK ANALOGIQUE DROIT**.
* Sur un bouton : **NORD** supprime son affectation, **OUEST** modifie sa description (un rappel de l'action dans le jeu, ex. « Tir »).
* **SAUVEGARDER** (ou **START**) enregistre le profil, **SUPPRIMER** supprime tout le profil.

<div align="left"><figure><img src="../.gitbook/assets/image (389).png" alt=""><figcaption></figcaption></figure></div>

## Où sont enregistrés les profils

<table><thead><tr><th width="141.5">Profil</th><th>Fichier</th></tr></thead><tbody><tr><td>Jeu</td><td>À côté du jeu : <code>roms\&#x3C;système>\&#x3C;jeu>.keys</code> (ex. <code>roms\amiga500\Turrican.keys</code>). Pour un jeu qui est un dossier : <code>padto.keys</code> dans le dossier</td></tr><tr><td>Système</td><td><code>system\padtokey\&#x3C;système>.keys</code></td></tr></tbody></table>

{% hint style="warning" %}
Le dossier `system\padtokey` est écrasé par les mises à jour de RetroBat. Pour garder un profil système, copiez-le dans `user\padtokey` : ce dossier est lu en priorité et n'est jamais écrasé.
{% endhint %}

### Quel profil est utilisé

Au lancement, RetroBat utilise le **premier profil trouvé**, dans cet ordre :

1. Le profil du jeu (`<jeu>.keys` ou `padto.keys`).
2. `user\padtokey\<système>.<core>.keys`, puis `user\padtokey\<système>.keys`.
3. `emulationstation\.emulationstation\padtokey` (mêmes noms).
4. `system\padtokey` (mêmes noms).

Un profil `<système>.<core>.keys` ne s'applique que quand le jeu est lancé avec ce core ou cet émulateur (ex. `amiga500.puae.keys` pour le core puae uniquement). Il ne peut pas être créé depuis EmulationStation : copiez un fichier `<système>.keys` et renommez-le.

RetroBat fournit des profils prêts à l'emploi dans `system\padtokey` pour certains systèmes (Amiga, Apple II, Atari ST, FM Towns, X68000, Sam Coupé…).

## Profils ScreenScraper

ScreenScraper fournit des profils PadToKey pour certains jeux. Pour les récupérer, activez **MENU PRINCIPAL > SCRAPEUR > PARAMÈTRES PADTOKEY** avant de scraper.

Le profil est enregistré à côté du jeu sous le nom `<jeu>.p2k.cfg` (ou `.p2k.cfg` dans le dossier d'un jeu qui est un dossier) et il est utilisé automatiquement. Si vous le modifiez dans EmulationStation, vos changements sont enregistrés dans un fichier `.keys`, qui est alors utilisé à la place du profil ScreenScraper.

## Le fichier .keys

Un fichier `.keys` est un fichier texte (JSON). Vous pouvez le modifier avec un éditeur de texte, par exemple pour créer un profil `<système>.<core>.keys`.

```json
{
    "actions_player1": [
        { "trigger": "a", "type": "key", "target": "KEY_SPACE", "description": "Saut" },
        { "trigger": "b", "type": "key", "target": "KEY_LEFTCTRL", "description": "Tir" },
        { "trigger": "start", "type": "key", "target": "KEY_ENTER" },
        { "trigger": ["hotkey", "a"], "type": "key", "target": ["KEY_LEFTSHIFT", "KEY_F1"] },
        { "trigger": "joystick2", "type": "mouse" },
        { "trigger": "r3", "type": "key", "target": "BTN_LEFT" }
    ],
    "actions_player2": [
        { "trigger": "a", "type": "key", "target": "KEY_RIGHTCTRL" }
    ]
}
```

* `actions_player1` à `actions_player4` : les actions de la manette de chaque joueur.
* `trigger` : le bouton de la manette, ou une liste de boutons appuyés ensemble (ex. `["hotkey", "a"]`).
* `type` : `key` pour envoyer des touches, `mouse` pour déplacer le pointeur de la souris avec un stick.
* `target` : la touche, ou une liste de touches envoyées ensemble.
* `description` (facultatif) : texte affiché dans l'éditeur.

<table><thead><tr><th width="392.75">Trigger</th><th>Bouton de la manette</th></tr></thead><tbody><tr><td><code>up</code>, <code>down</code>, <code>left</code>, <code>right</code></td><td>Croix directionnelle</td></tr><tr><td><code>a</code>, <code>b</code>, <code>x</code>, <code>y</code></td><td>SUD, EST, NORD, OUEST</td></tr><tr><td><code>start</code>, <code>select</code>, <code>hotkey</code></td><td>START, SELECT, HOTKEY</td></tr><tr><td><code>pageup</code>, <code>pagedown</code></td><td>L1, R1</td></tr><tr><td><code>l2</code>, <code>r2</code></td><td>L2, R2</td></tr><tr><td><code>l3</code>, <code>r3</code></td><td>CLIC STICK GAUCHE, CLIC STICK DROIT</td></tr><tr><td><code>joystick1up</code>, <code>joystick1down</code>, <code>joystick1left</code>, <code>joystick1right</code></td><td>Stick analogique gauche</td></tr><tr><td><code>joystick2up</code>, <code>joystick2down</code>, <code>joystick2left</code>, <code>joystick2right</code></td><td>Stick analogique droit</td></tr><tr><td><code>joystick1</code>, <code>joystick2</code> (avec <code>"type": "mouse"</code>)</td><td>Stick qui déplace le pointeur de la souris</td></tr></tbody></table>

**Targets** :

* Touches : `KEY_A` à `KEY_Z`, `KEY_0` à `KEY_9`, `KEY_F1` à `KEY_F12`, `KEY_ENTER`, `KEY_ESC`, `KEY_SPACE`, `KEY_TAB`, `KEY_BACKSPACE`, `KEY_UP`, `KEY_DOWN`, `KEY_LEFT`, `KEY_RIGHT`, `KEY_LEFTSHIFT`, `KEY_LEFTCTRL`, `KEY_LEFTALT`, `KEY_KP0` à `KEY_KP9` (pavé numérique)…
* Boutons de la souris : `BTN_LEFT`, `BTN_RIGHT`, `BTN_MIDDLE`.
* Actions spéciales (jeux Windows, portages) : `(%{CLOSE})` ferme la fenêtre du jeu, `(%{KILL})` tue le processus du jeu, `(%{F4})` envoie Alt + F4.

{% hint style="warning" %}
- Les noms des touches sont ceux d'un clavier **QWERTY**, par position : sur un clavier AZERTY, `KEY_Q` est la touche **A** et `KEY_A` est la touche **Q**.
- Les actions spéciales ne peuvent être écrites qu'à la main : si vous ouvrez et sauvegardez le profil dans EmulationStation, elles sont supprimées.
{% endhint %}

## Dépannage

* Les touches ne sont envoyées qu'à la fenêtre de l'émulateur ou du jeu lancé par RetroBat, quand elle est au premier plan.
* Si **JoyToKey** est lancé, PadToKey est désactivé.
* RetroBat utilise déjà PadToKey pour les raccourcis de certains émulateurs standalone (ex. **HOTKEY + START** pour quitter). Un bouton de votre profil remplace le raccourci RetroBat sur le même bouton.
* `emulationstation\emulatorLauncher.log` indique le profil utilisé (ligne `[PadToKey] Using mapping file`) et chaque touche envoyée (lignes `[SendKey]`).
