# Configuration des systèmes et des jeux

Un des avantages majeurs de RetroBat par rapport aux autres front-end, est que le paramétrage des émulateurs se fait directement depuis les menus de RetroBat, sans avoir à passer par l'interface de chaque émulateur.

{% hint style="danger" %}
Si vous paramétrez un émulateur directement depuis l'interface de ce dernier, il y a de fortes chances que la configuration effectuée soit écrasée par RetroBat lors du lancement d'un jeu.
{% endhint %}



Les éléments de configuration disponibles dans RetroBat sont appelés "fonctionnalités" (features); elles ont l'avantage de pouvoir être paramétrées à 2 niveaux : <br>

* Globalement pour tout un système,
* Par jeu.



## Comment accéder au menu de configuration :

Le menu des fonctionnalités est disponible depuis le menu "[Options d'Affichage](view-options.md)" ou depuis le menu  "[Options du jeu](game-options.md)" :

#### En sélectionnant le sous-menu **CONFIGURATION AVANCÉE DU SYSTÈME** :

<div align="left"><figure><img src="https://i.imgur.com/sj9Pu6j.png" alt=""><figcaption><p>Accéder aux fonctionnalités depuis les OPTIONS D'AFFICHAGE</p></figcaption></figure></div>

\==> Les changements s'appliqueront à tous les jeux du système sélectionné.



#### En sélectionnant le sous-menu CONFIGURATION AVANCÉE DU JEU :

<div align="left"><figure><img src="https://i.imgur.com/zrzRAf4.png" alt=""><figcaption><p>Accéder aux fonctionnalités depuis les OPTIONS DU JEU</p></figcaption></figure></div>

\==> Les changements s'appliqueront uniquement à ce jeu.



Il est important de noter que les options configurées pour le jeu sont prioritaires à celles configurées pour le système. Cela signifie que si des réglages sont faits pour un système, et d'autres réglages pour un jeu de ce même système, au lancement de ce jeu ce sont les réglages par jeu qui seront pris en compte.

## Les options de configuration

Les fonctionnalités disponibles dépendent de l'émulateur sélectionné, car tous ne proposent pas les mêmes options.

Cela signifie que pour un même système, en changeant l'émulateur par défaut, les fonctionnalités disponibles ne sont pas les mêmes.



Dans la plupart des cas, les fonctionnalités sont catégorisées en 2 sous-groupes :

* General Settings (réglages généraux)
* Advanced Settings (réglages avancés)

<div align="left"><figure><img src="https://i.imgur.com/ITxbL6Q.png" alt=""><figcaption><p>Exemple de réglages pour NES avec le core FCEUMM (core par défaut)</p></figcaption></figure></div>

### Réglages généraux

Les **Réglages généraux** vous donneront accès aux options de configurations suivantes, disponibles pour une grande majorité d'émulateurs :

* les filtres vidéo à appliquer
* les bezels (décorations) à appliquer
* le ratio d'affichage du jeu et la résolution
* la synchronisation verticale
* l'affichage échelle entière "Pixel Perfect"
* la désactivation de la configuration automatique des manettes



### Réglages avancés

Ces réglages sont plus spécifiques, ils sont organisés en sous-menus, se décomposant de la façon suivante :

* EMULATION : contient des fonctionnalités telles que la langue, la machine émulée, la région mais aussi les options de performances quand elles sont disponibles pour l'émulateur
* VIDEO : Options vidéo générales comme l'index de moniteur, le signal de sortie, l'orientation de l'écran, ...
* SCREEN SYNC : contient habituellement des options permettant de règler la synchronisation verticale de l'écran ou le taux de rafraîchissement
* VISUAL RENDERING : contient des fonctionnalités liées au rendu visuel, comme la mise à l'échelle, l'anti crénelage...
* AUDIO : les réglages audios comme le taux d'échantillonnage, le filtre passe-bas...
* LATENCY REDUCTION : les options pour réduire le décalage d'entrée (input lag)
* USER INTERFACE : contient des fonctionnalités comme l'affichage des FPS, l'activation ou la désactivation des notifications des émulateurs...
* DRIVERS : les options permettant de changer les pilotes vidéos, audios, les pilotes des manettes utilisées par les émulateurs
* CONTROLS : les options liées aux contrôleurs : type de manettes, options des lightguns...

<div align="left"><figure><img src="https://i.imgur.com/xmWmV4E.png" alt=""><figcaption><p>Exemple des fonctionnalités du sous-menu EMULATION pour le core FCEUMM</p></figcaption></figure></div>



De plus, certains émulateurs possèdent des sous-menus spécifiques, c'est le cas par exemple pour pcsx2, qui est pourvu d'un sous-menu MANUAL HACKS et GAME FIXES :

<div align="left"><figure><img src="https://i.imgur.com/FHWmxWa.png" alt=""><figcaption></figcaption></figure></div>

ou pour les PORTS qui ont des réglages dédiés par jeu :

<div align="left"><figure><img src="https://i.imgur.com/nCX1t0V.png" alt=""><figcaption></figcaption></figure></div>



## Comment la magie opère ?

L'astuce qui permet de rendre cela possible est simple : avant de lancer un jeu, RetroBat récupère les options qui ont été définies par l'utilisateur depuis le menu, et applique ces réglages directement dans les fichiers de configuration de l'émulateur, avant de démarrer la partie.

Prenons par exemple le cas d'un utilisateur qui souhaite changer le pilote graphique de l'émulateur DuckStation pour choisir VULKAN.



Depuis le menu de configuration du système,

<div align="left"><figure><img src="https://i.imgur.com/HOticd8.png" alt=""><figcaption></figcaption></figure></div>

Sélectionner le sous-menu **DRIVERS** dans la catégorie **ADVANCED SETTINGS** :

<div align="left"><figure><img src="https://i.imgur.com/A45rj72.png" alt=""><figcaption></figcaption></figure></div>



Puis modifier l'option **VIDEO** en "VULKAN" :

<div align="left"><figure><img src="https://i.imgur.com/xaeKGGB.png" alt=""><figcaption></figcaption></figure></div>

Lors du lancementdu jeu, RetroBat va automatiquement définir la valeur suivante dans le fichier de configuration de Duckstation avant de démarrer le jeu :

<div align="left"><figure><img src="https://i.imgur.com/yYUfic3.png" alt=""><figcaption></figcaption></figure></div>

Et voilà !

## Super, mais alors à quoi correspond la valeur "AUTO" ?

La valeur "AUTO" peut avoir différentes significations, selon que le paramétrage de la fonctionnalité soit fait au niveau du système, ou au niveau du jeu.

Au niveau du système, la valeur "AUTO" est une valeur par défaut que l'équipe RetroBat a choisie comme étant la valeur qui permet de proposer la meilleure expérience utilisateur.

Au niveau du jeu, la valeur "AUTO" correspond à la valeur définie au niveau système/émulateur.

{% hint style="info" %}
Rappelez-vous que le réglage "par jeu" prendra toujours le dessus sur tous les autres réglages.
{% endhint %}

## Bien, mais je ne vois pas l'option dont j'ai besoin !

Pas de panique, s'il y a une option dans un émulateur que vous souhaiteriez ajouter (ou modifier), n'hésitez pas à contacter l'équipe RetroBat, qui fera le nécessaire pour ajouter l'option sur la version suivante, dans la mesure du possible !

En parallèle, sachez que les options qui ne sont pas disponibles depuis le menu RetroBat peuvent être modifiées directement dans l'émulateur, elles ne devraient pas être écrasés par RetroBat...
