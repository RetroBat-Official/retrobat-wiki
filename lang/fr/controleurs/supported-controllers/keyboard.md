# ⌨️ Clavier

Un clavier standard est reconnu d'office, pour naviguer dans RetroBat et pour jouer.

## Naviguer dans RetroBat

Les touches par défaut sont listées sur la page [Navigation](https://app.gitbook.com/s/Cgoewyw8Sagl6SNUMrCG/navigation). Pour les modifier, allez dans **MENU PRINCIPAL > PARAMÈTRES DES MANETTES > CONFIGURER UNE MANETTE** et appuyez sur une touche du clavier pour le configurer comme une manette.

## Jouer avec le clavier

La configuration clavier de RetroBat est aussi utilisée en jeu : RetroArch et la plupart des émulateurs la récupèrent automatiquement.

{% hint style="info" %}
Pour certains émulateurs standalone, le clavier n'est pas configuré automatiquement : configurez les touches directement dans l'émulateur.
{% endhint %}

## Ordinateurs : le focus clavier

Pour les systèmes ordinateurs (Amiga, Commodore 64, Amstrad CPC, MSX, Atari ST, ZX Spectrum, DOS…), le clavier est celui de l'ordinateur émulé : les jeux ont souvent besoin de nombreuses touches.

Dans RetroArch, certaines touches sont aussi des raccourcis RetroArch (F1 pour le menu, Échap pour quitter, F2 / F4 pour les sauvegardes d'état…, voir [Raccourcis](../../navigation/hotkeys.md)). Pour donner **tout le clavier** à l'ordinateur émulé, activez **FOCUS CLAVIER** dans la configuration avancée du système (ou du jeu) > **CONTRÔLES** :

* toutes les touches du clavier sont envoyées au jeu, et les raccourcis clavier de RetroArch sont désactivés ;
* appuyez sur **Arrêt défil** (Scroll Lock) pour désactiver le focus (et retrouver les raccourcis) puis le réactiver, en cours de jeu ;
* les raccourcis manette fonctionnent toujours (par exemple **HOTKEY + START** pour quitter).

Cette option est disponible pour les cores RetroArch des ordinateurs, ainsi que pour ScummVM et les portages de Quake / Doom.

## Jouer aux jeux d'ordinateur avec une manette (PadToKey)

Beaucoup de jeux d'ordinateur se jouent uniquement au clavier. Avec [**PadToKey**](../pad2key.md), les boutons de votre manette envoient des touches du clavier : vous pouvez alors jouer à ces jeux à la manette.

* RetroBat fournit des profils prêts à l'emploi pour certains systèmes (Amiga, Apple II, Atari ST, FM Towns…).
* Vous pouvez créer ou modifier un profil depuis EmulationStation :
  * pour tout un système : dans la configuration avancée du système, **CRÉER UN PROFIL PADTOKEY** (ou **ÉDITER UN PROFIL PADTOKEY** s'il existe déjà) ;
  * pour un seul jeu : dans les [Options du jeu](../../navigation/game-options.md), **CRÉER UN PROFIL PADTOKEY** / **ÉDITER UN PROFIL PADTOKEY**. Le profil d'un jeu est enregistré à côté du jeu, dans un fichier `<jeu>.keys` (`padto.keys` dans le dossier pour un jeu qui est un dossier).

Dans l'écran **CONFIGURATION MANETTE À CLAVIER**, choisissez un bouton de la manette, puis la touche du clavier (ou l'action de la souris) qu'il doit envoyer.

{% hint style="info" %}
Les options PadToKey n'apparaissent que pour les systèmes et émulateurs qui le prennent en charge.
{% endhint %}
