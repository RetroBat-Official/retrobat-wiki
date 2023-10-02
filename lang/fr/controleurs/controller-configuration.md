# Configuration des Contrôleurs

RetroBat configure automatiquement les contrôleurs en utilisant une base de données fournies par la librairie SDL, cela signifie que, dans la plupart des cas, aucune intervention utilisateur n'est nécessaire.

Dans certains cas cependant, la configuration automatique ne fonctionne pas ou effectue une assignation incorrecte de certaines touches (par exemple, pour les manettes Nintendo, les boutons A,B et X,Y sont inversés), il est alors nécessaire de faire une configuration manuelle du contrôleur. Pour cela, procéder ainsi:

## Configuration des contrôleurs

Depuis le menu RetroBat, appuyer sur "START" (ENTREE sur le clavier), puis dans le menu sélectionner "PARAMETRES DES MANETTES"

<div align="left">

<figure><img src="https://i.imgur.com/B6nd01B.png" alt=""><figcaption></figcaption></figure>

</div>

Dans le menu suivant, sélectionner "CONFIGURER UNE MANETTE"

<div align="left">

<figure><img src="https://i.imgur.com/pFxyTXF.png" alt=""><figcaption></figcaption></figure>

</div>

Confirmer pour passer à l'écran de détection de la manette

<figure><img src="https://i.imgur.com/eNTHkgt.png" alt=""><figcaption></figcaption></figure>

Presser et maintenir appuyé un bouton pour passer à l'écran **CONFIGURATION**

<div align="left">

<figure><img src="https://i.imgur.com/yGkfqEt.png" alt=""><figcaption></figcaption></figure>

</div>

Configurer la correspondance entre le système et la manette connectée pour chaque bouton.&#x20;

{% hint style="info" %}
Si la manette de jeu contient moins de bouton que ceux disponibles dans Retrobat, rester appuyer sur un bouton pour ignorer la ligne en cours et passer à la ligne suivante.

Il est toutefois nécessaire d'assigner les boutons A, B, D-PAD, START, SELECT et HOTKEY pour pouvoir utiliser Retrobat correctement.
{% endhint %}

Les correpondances de boutons "standard" pour les manettes XBOX, PlayStation et Nintendo sont listées dans la table ci-dessous:

<table><thead><tr><th width="184">Retrobat</th><th>Microsoft</th><th>PlayStation</th><th>Nintendo</th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (19).png" alt="A"></td><td>A</td><td><img src="../.gitbook/assets/image (12).png" alt=""></td><td>B</td></tr><tr><td><img src="../.gitbook/assets/image (6).png" alt=""></td><td>B</td><td><img src="../.gitbook/assets/image (22).png" alt=""></td><td>A</td></tr><tr><td><img src="../.gitbook/assets/image (34).png" alt=""></td><td>Y</td><td><img src="../.gitbook/assets/image (20).png" alt=""></td><td>X</td></tr><tr><td><img src="../.gitbook/assets/image (32).png" alt="" data-size="line"></td><td>X</td><td><img src="../.gitbook/assets/image (5).png" alt=""></td><td>Y</td></tr><tr><td>START</td><td><img src="../.gitbook/assets/image (24).png" alt=""></td><td>START / OPTIONS</td><td>+</td></tr><tr><td>SELECT</td><td><img src="../.gitbook/assets/image (23).png" alt=""></td><td>SELECT / SHARE</td><td>-</td></tr><tr><td>D-PAD HAUT</td><td>D-PAD HAUT</td><td>D-PAD HAUT</td><td>D-PAD HAUT</td></tr><tr><td>D-PAD BAS</td><td>D-PAD BAS</td><td>D-PAD BAS</td><td>D-PAD BAS</td></tr><tr><td>D-PAD GAUCHE</td><td>D-PAD GAUCHE</td><td>D-PAD GAUCHE</td><td>D-PAD GAUCHE</td></tr><tr><td>D-PAD DROITE</td><td>D-PAD DROITE</td><td>D-PAD DROITE</td><td>D-PAD DROITE</td></tr><tr><td>L1</td><td>L1</td><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R1</td><td>R1</td><td>R</td></tr><tr><td>Stick gauche haut</td><td>Stick gauche haut</td><td>Stick gauche haut</td><td>Stick gauche haut</td></tr><tr><td>Stick gauche gauche</td><td>Stick gauche gauche</td><td>Stick gauche gauche</td><td>Stick gauche gauche</td></tr><tr><td>Stick droit haut</td><td>Stick droit haut</td><td>Stick droit haut</td><td>Stick droit haut</td></tr><tr><td>Stick droit gauche</td><td>Stick droit gauche</td><td>Stick droit gauche</td><td>Stick droit gauche</td></tr><tr><td>L2</td><td>L2</td><td>L2</td><td>ZL</td></tr><tr><td>R2</td><td>R3</td><td>R2</td><td>ZR</td></tr><tr><td>L3</td><td>L3 (stick)</td><td>L3 (stick)</td><td>L3 (stick)</td></tr><tr><td>R3</td><td>R3 (stick)</td><td>R3 (stick)</td><td>R3 (stick)</td></tr></tbody></table>

## Activer une configuration spécifique par jeu

Il est possible de désactiver la configuration automatique des contrôleurs dans Retrobat et de gérer la configuration des manettes directement dans les émulateurs.

La configuration automatique des manettes peut être désactivées pour tous les systèmes, par système ou uniquement pour un jeu.

### **Désactivation pour tous les systèmes**

Ouvrir le [MENU PRINCIPAL](../navigation/main-menu.md#parametres-des-jeux) et aller dans les **PARAMETRES DES JEUX.**

<div align="left">

<figure><img src="https://i.imgur.com/EZGqHO6.png" alt=""><figcaption></figcaption></figure>

</div>

Désactiver **AUTOCONFIGURER LES MANETTES.**

<div align="left">

<figure><img src="https://i.imgur.com/ExUlbH4.png" alt=""><figcaption></figcaption></figure>

</div>

### **Désactivation pour un système**

Ouvrir le menu [**OPTIONS D'AFFICHAGE**](../navigation/view-options.md#configuration-avancees-du-systeme) et aller dans **CONFIGURATION AVANCÉE DU SYSTÈME.**

<div align="left">

<figure><img src="https://i.imgur.com/yluNDLe.png" alt=""><figcaption></figcaption></figure>

</div>

Puis régler l'option **AUTOCONFIGURER LES MANETTES**  sur **NON.**

<div align="left">

<figure><img src="https://i.imgur.com/I45PNhI.png" alt=""><figcaption></figcaption></figure>

</div>

### **Désactivation pour un jeu**

Ouvrir le menu [**OPTIONS DU JEU**](../navigation/game-options.md#configuration-avancee-du-jeu) et sélectionner **CONFIGURATION AVANCEE DU JEU.**

<div align="left">

<figure><img src="https://i.imgur.com/nedAp7Z.png" alt=""><figcaption></figcaption></figure>

</div>

Puis régler l'option **AUTOCONFIGURER LES MANETTES**  sur **NON.**

<div align="left">

<figure><img src="https://i.imgur.com/Z96x4mm.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="warning" %}
Lorsque l'option AUTOCONFIGURER LES MANETTES est réglée sur NON, il est nécessaire de configurer les contrôleurs directement dans l'émulateur.

Pour accéder aux menus des émulateurs, naviguer dans la **Vue Système** et sélectionner le système "RETROBAT". (Il est également possible de lancer chaque émulateur depuis le dossier `\emulators` dans le répertoire d'installation de Retrobat)

Pour RetroArch, il est possible de créer une configuration spécifique à chaque jeu en pressant F1 (hotkey + ![A](<../.gitbook/assets/image (19).png>)) en cours de jeu et en naviguant dans le menu RetroArch pour accéder à la configuration du contrôleur.
{% endhint %}

## Résolution de soucis liés aux contrôleurs

En cas de problème avec vos contrôleurs, vous pouvez tenter avant toute chose de réinitialiser la configuration des touches à l'aide de [BatGui](https://wiki.retrobat.org/v/francais/utilisation-avancee/batgui#gerer-la-bibliotheque-sdl-et-reinitialiser-la-configuration-des-manettes).\
Si le problème persiste, n'hesitez pas à contacter la team Retrobat sur le forum ou le discord.
