# Game Control Center

Le Game Control Center est un menu affiché par-dessus le jeu. Il donne un accès rapide aux informations du jeu en cours : jaquette, description, contrôles (tatouage), carte et manuel. Il permet aussi de quitter le jeu.

## Ouvrir le Game Control Center

Pendant une partie, appuyez sur :

* **HOTKEY + Est** ![](<../.gitbook/assets/image (324).png>) à la manette,
* ou **Ctrl + F12** au clavier.

<div align="left"><figure><img src="../.gitbook/assets/image (325).png" alt=""><figcaption></figcaption></figure></div>

Quand le Game Control Center est ouvert :

<table><thead><tr><th width="191.5">Bouton</th><th>Action</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Se déplacer entre les boutons</td></tr><tr><td>Sud</td><td>Valider</td></tr><tr><td>Est ou Nord</td><td>Fermer le Game Control Center et revenir au jeu</td></tr><tr><td>L1 / R1</td><td>Page précédente / suivante</td></tr></tbody></table>

## Boutons

<table><thead><tr><th width="221.5">Bouton</th><th>Action</th></tr></thead><tbody><tr><td><strong>Tatouage</strong> / <strong>Jaquette</strong></td><td>Afficher les contrôles du système ou du jeu à la place de la jaquette. Le bouton devient alors <strong>Jaquette</strong> : appuyez dessus pour réafficher la jaquette</td></tr><tr><td><strong>Carte</strong></td><td>Ouvrir la carte du jeu</td></tr><tr><td><strong>Manuel d'utilisation</strong></td><td>Ouvrir le manuel du jeu (PDF)</td></tr><tr><td><strong>Retourner au jeu</strong></td><td>Fermer le Game Control Center</td></tr><tr><td><strong>Terminer l'émulation</strong></td><td>Quitter l'émulateur et revenir à RetroBat</td></tr></tbody></table>

<div align="left"><figure><img src="../.gitbook/assets/image (326).png" alt="" width="563"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (327).png" alt="" width="563"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (328).png" alt="" width="563"><figcaption></figcaption></figure></div>

{% hint style="info" %}
* **Carte** et **Manuel d'utilisation** ne s'affichent que si le jeu possède ces médias (téléchargés par le [scrapeur](scraping-and-metadata.md) ou ajoutés avec **ÉDITER LES MÉTADONNÉES DU JEU**).
* **Tatouage** ne s'affiche que s'il existe un tatouage pour le système ou le jeu. Vous pouvez ajouter vos propres tatouages dans `user\tattoos\games\<système>\` (un jeu) ou `user\tattoos\default\` (tout le système) : voir [Structure du répertoire RetroBat](../premiers-pas/structure-du-repertoire-retrobat.md).
* **Terminer l'émulation** ferme l'émulateur sans sauvegarder : sauvegardez votre partie avant, ou utilisez **HOTKEY + START** pour quitter normalement.
{% endhint %}

{% hint style="warning" %}
La plupart des émulateurs se mettent en pause automatiquement quand le Game Control Center s'affiche (MAME, Model 2 et Hypseus sont suspendus par RetroBat). Si **NE PAS METTRE EN PAUSE LORS DE LA PERTE DE FOCUS** est activé dans les **PARAMÈTRES DES JEUX**, le jeu peut continuer à tourner derrière le Game Control Center.
{% endhint %}

## Désactiver le Game Control Center

Le Game Control Center utilise la combinaison **HOTKEY + Est** : tant qu'il est activé, cette combinaison ne peut pas être utilisée pour un autre raccourci, dans aucun émulateur (voir [Raccourcis](hotkeys.md)).

Si vous ne l'utilisez pas, vous pouvez le désactiver dans **MENU PRINCIPAL** > **PARAMÈTRES DES JEUX** > **DÉSACTIVER LE GAME CONTROL CENTER**. **HOTKEY + Est** est alors libre, et vous pouvez l'attribuer à un autre raccourci dans les fichiers de raccourcis (voir [Personnaliser les raccourcis](hotkeys.md#personnaliser-les-raccourcis)).

<div align="left"><figure><img src="../.gitbook/assets/image (329).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Le Game Control Center n'est pas disponible pour Pinball FX et pour les jeux Windows.
{% endhint %}
