# Configuration des touches MAME

La configuration des commandes de l'émulateur MAME est très complexe, car chaque machine qu'il émule dispose d'une disposition des commandes différente.

RetroBat propose plusieurs façons de modifier la configuration des manettes pour MAME, ainsi que pour libretro-mame. Chaque méthode est décrite sur cette page.

## MAME (standalone)

Il existe différentes façons de paramétrer les configurations de touches pour MAME, que ce soit manuellement ou automatiquement :

* Avec l'autoconfiguration par défaut de RetroBat
* Avec la surcharge RetroBat des fichiers xml (par jeu)
* Par une configuration adaptée a des types de contrôleur spécifiques
* Par une configuration manuelle spécifique à un jeu
* Par une configuration manuelle personnalisée

### Autoconfiguration RetroBat&#x20;

Par défaut, RetroBat tentera de configurer automatiquement les commandes dans MAME, soit en utilisant les paramètres fournis par RetroBat pour chaque jeu, soit en appliquant une configuration par défaut.

L'autoconfiguration peut être modifié selon la disposition des boutons, a spécifier dans le menu **CONFIGURATION AVANCÉE DU SYSTÈME > CONTRÔLES :**

<div align="left"><figure><img src="../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure></div>

**Les boutons par défaut pour chacun de ces profiles sont les suivants :**&#x20;

**Controller** : Ce profile est adapté pour les manettes, ou ![](<../../.gitbook/assets/image (118).png>) est assigné au bouton 1, ![](<../../.gitbook/assets/image (121).png>) est assigné au bouton 2, ![](<../../.gitbook/assets/image (124).png>) est assigné au bouton 3, ![](<../../.gitbook/assets/image (127).png>) est assigné au bouton 4, L1 au bouton 5, R1 au bouton 6, L2 au bouton 7 et R2 au bouton 8

**Modern 8 buttons** : Ce profile est celui le plus communément utilisé pour les sticks d'arcade modernes, les 4 boutons supérieurs sont les boutons 1 (![](<../../.gitbook/assets/image (125).png>)), 2(![](<../../.gitbook/assets/image (128).png>)), 3(R1) et 7(L1), les 4 boutons inférieurs sont les boutons 4(![](<../../.gitbook/assets/image (119).png>)), 5(![](<../../.gitbook/assets/image (122).png>)), 6(R2) et 8(L2)

**Classic 8 buttons** : Les 4 boutons supérieurs sont les boutons 1 (![](<../../.gitbook/assets/image (126).png>)), 2(![](<../../.gitbook/assets/image (129).png>)), 3(L1) et 7(L2), les 4 boutons inférieurs sont les boutons 4(![](<../../.gitbook/assets/image (120).png>)), 5(![](<../../.gitbook/assets/image (123).png>)), 6(R1) et 8(R2)

**6 buttons** : similaire au profile classic 8 buttons mais sans les boutons 7 et 8

**8 buttons alternative** : La valeur par défaut correspond au mappage du contrôleur

### Surcharge RetroBat des fichiers xml par jeu

RetroBat est fourni avec des configurations adaptées par jeu, pour chacune des dispositions décrites ci-dessus, pour environ 130 jeux. Les fichiers de configuration fournis avec RetroBat se trouvent dans le répertoire `\system\resources\inputmapping\mame` :

<div align="left"><figure><img src="../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Vous pouvez créer votre propre fichier et le partager avec l'équipe RetroBat, ou le sauvegarder dans le dossier `\user\inputmapping\mame` de votre installation RetroBat si vous souhaitez apporter des variations personnelles à la configuration fournie par RetroBat.
{% endhint %}

Le fichier de remplacement est un fichier XML, très similaire au format MAME utilisé pour ses propres fichiers de configuration, mais contenant des noms de boutons génériques, qui seront convertis par RetroBat en fonction de la manette connectée et du profil sélectionné :

<div align="left"><figure><img src="../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure></div>

Chaque fichier contient plusieurs sections « _layout_ », qui correspondent aux dispositions disponibles dans RetroBat. En fonction de la valeur sélectionnée dans les paramètres de contrôle de RetroBat, la disposition correspondante sera choisie dans le fichier.

Chaque configuration contient les raccourcis clavier spécifiques à utiliser pour le jeu ; par exemple, la ligne suivante signifie que le **bouton 3** de la machine arcade "_altbeast_", pour le joueur 1, sera défini sur le **bouton EST** du contrôleur, lors de l'utilisation du layout "default" :

<div align="left"><figure><img src="../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure></div>

In the same file you can see that this button is mapped to the **R1 button** when using the modern8 layout (which corresponds to the 3rd button of the upper range of the arcade stick) :

Dans ce même fichier, vous pouvez voir que ce bouton est associé à la **touche R1** lorsque vous utilisez la configuration « modern8 » (ce qui correspond au troisième bouton de la rangée supérieure de la manette d'arcade) :

<div align="left"><figure><img src="../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure></div>

Vous pouvez utiliser [la même méthode que décrite ci-dessous](configuration-des-touches-mame64.md#creation-dun-fichier-de-configuration-de-manette-specifique-pour-mame) pour créer votre propre configuration de fichier, vous devrez toutefois remplacer les valeurs des boutons par celles fournies par RetroBat :

<details>

<summary>Liste des valeurs génériques des boutons RetroBat</summary>

* JOY\_west
* JOY\_north
* JOY\_east
* JOY\_south
* JOY\_down (dpad down)
* JOY\_lsdown (left stick down)
* JOY\_up / JOY\_lsup
* JOY\_left / JOY\_lsleft
* JOY\_right / JOY\_lsright
* JOY\_r1
* JOY\_l1
* JOY\_r2trigger
* JOY\_l2trigger
* JOY\_r3
* JOY\_l3
* JOY\_leftstickx (stick gauche axe horizontal) / JOY\_rightstickx
* JOY\_leftsticky (stick gauche axe vertical) / JOY\_leftstickx
* JOY\_lsup / JOY\_lsdown / JOY\_lsleft / JOY\_lsright (directions stick gauche)

Il est également possible d'ajouter « reverse » après un axe afin de définir \_REVERSE dans le fichier de configuration de MAME.

</details>

### Utilisation d'une configuration spécifique manuelle

Utilisez les réglages suivants dans le menu **CONFIGURATION AVANCÉE DU SYSTÈME > CONTRÔLES** de RetroBat pour activer une configuration spécifique :

<div align="left"><figure><img src="../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure></div>

Tous les paramètres autres que « RetroBat Auto » permettent de configurer MAME pour qu'il utilise un fichier de configuration de manette situé dans le dossier `\saves\mame\ctrlr\` de votre installation RetroBat.\
RetroBat est fourni avec deux fichiers : l'un pour la manette IPAC2 et l'autre pour la manette X-Arcade TankStick. Si vous possédez l'une de ces manettes, vous pouvez utiliser ces options pour les configurer automatiquement.\
Les autres profils peuvent être utilisés pour pointer vers des fichiers que vous devez créer, qu'il s'agisse de fichiers personnalisés ou de fichiers spécifiques à chaque jeu (nommés d'après la ROM du jeu). Ces fichiers ne sont pas fournis avec RetroBat et doivent être créés. Voici la procédure à suivre :

## Création d'un fichier de configuration de manette spécifique pour MAME

### ÉTAPE 1 : Préambule

Au lancement, MAME parcourt plusieurs dossiers pour définir la configuration à utiliser, l'ordre de priorité utilisé est le suivant (du moins prioritaire au plus prioritaire - cela signifie que le dernier fichier trouvé aura la priorité sur les autres):

1. Configuration native de l'émulateur
2. Fichier default.cfg dans le dossier `\bios\mame\cfg` (si existant)
3. Fichier spécifique au jeu dans le dossier `\bios\mame\cfg` (si existant - doit porter exactement le nom de la rom de jeu)
4. Fichier de configuration contrôleur situé dans `\saves\mame\ctrlr` selon la sélection faite par l'utilisateur depuis l'interface RetroBat

### ÉTAPE 2 : Création du fichier de configuration des touches dans MAME

Démarrer _mame.exe_, l’exécutable se trouve dans le répertoire `emulators\mame` de votre installation RetroBat.

Cliquer sur "General Settings":

<div align="left"><figure><img src="https://i.imgur.com/7FfrAyr.png" alt=""><figcaption></figcaption></figure></div>

Sélectionner "Input Assignments"

<div align="left"><figure><img src="https://i.imgur.com/P23EUU1.png" alt=""><figcaption></figcaption></figure></div>

Sélectionner les touches à assigner :

* La section "User Interface" vous permet de choisir les touches servant à la navigation dans les menus MAME
* Les sections Player X permettent d'assigner les touches qui seront utilisées dans les jeux pour les différents joueurs

<div align="left"><figure><img src="https://i.imgur.com/pgXcIQM.png" alt=""><figcaption></figcaption></figure></div>

Attribuer les touches comme désiré :

<div align="left"><figure><img src="https://i.imgur.com/kxVLMtw.png" alt=""><figcaption></figcaption></figure></div>

En utilisant les touches gauche et droite (ou les boutons), il est possible de rajouter une touche pour effectuer la même action, ou de réinitialiser le paramétrage de la touche.

<div align="left"><figure><img src="https://i.imgur.com/ubjsXry.png" alt=""><figcaption><p>Vous pouvez compléter...</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/6pGoFrF.png" alt=""><figcaption><p>Ou bien supprimer et réinitialiser</p></figcaption></figure></div>

Une fois le paramétrage effectué, revenir en arrière et cliquer sur "Save Settings" :

<div align="left"><figure><img src="https://i.imgur.com/pDLsvFJ.png" alt=""><figcaption></figcaption></figure></div>

Un fichier nommé "default.cfg" sera sauvegardé dans le répertoire`\emulators\mame\cfg`.

<div align="left"><figure><img src="https://i.imgur.com/PmZJO4I.png" alt=""><figcaption></figcaption></figure></div>

### ÉTAPE 3 : Utiliser le fichier cfg

Ouvrir le fichier default.cfg et vérifier le contenu :

<div align="left"><figure><img src="https://i.imgur.com/tYgSbfM.png" alt=""><figcaption></figcaption></figure></div>

Le fichier est au format xml, le paramétrage précédemment renseigné se situe dans la section \<input> du fichier.\
\
&#xNAN;_&#x44;ans l'exemple, la touche "Q" du clavier a été attribué à l'action "UI\_MENU" qui ouvre le menu MAME._

Enfin, déplacer le fichier default.cfg vers le dossier `\bios\mame\cfg` de votre installation : ce profil devient alors le profil par défaut.

### ÉTAPE 4 : Créer un profil contrôleur dédié

Procéder comme expliqué à l'étape 1, puis renommer le fichier selon l'une des valeurs ci-dessous :&#x20;

* custom1.cfg
* custom2.cfg
* ...
* custom8.cfg

Déplacer le fichier dans le répertoire `\saves\mame\ctrlr` de votre installation RetroBat :

<div align="left"><figure><img src="https://i.imgur.com/15wt2XH.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Il est également possible de réaliser le paramétrage des touches directement dans le fichier .cfg si vous vous sentez à l'aise avec la structure xml du document.\
\
D'autres informations concernant la structure du fichier se trouvent ici : \
[http://mirrors.arcadecontrols.com/easyemu/mameguidenew/mameguide-controlini.htm](http://mirrors.arcadecontrols.com/easyemu/mameguidenew/mameguide-controlini.htm)\
[https://docs.mamedev.org/advanced/ctrlr\_config.html](https://docs.mamedev.org/advanced/ctrlr_config.html)
{% endhint %}

### ÉTAPE 5 : Sélectionner le profil de touche depuis RetroBat

Depuis le [menu jeu](../../navigation/system-view-and-game-view.md#vue-jeux) MAME, appuyer sur SELECT pour ouvrir le menu [Options d'affichage](../../navigation/view-options.md) et sélectionner "CONFIGURATION AVANCÉE DU SYSTÈME"

<div align="left"><figure><img src="https://i.imgur.com/6LP55Wp.png" alt=""><figcaption></figcaption></figure></div>

S'assurer que MAME64 soit défini comme émulateur par défaut et naviguer jusqu'au sous-menu CONTROLS :

<div align="left"><figure><img src="https://i.imgur.com/gC4dECi.png" alt=""><figcaption></figcaption></figure></div>

Sélectionner l'option "CONTROLLER PROFILE" et choisir dans la liste le profil correspondant au fichier que vous avez créé :

{% hint style="info" %}
RetroBat propose 8 profils personnalisés ainsi que la possibilité d'utiliser un fichier de profil par jeu.

Pour utiliser le profil par jeu, le nom du fichier doit correspondre au nom du jeu (sans l'extension), par exemple il faut appeler le fichier de configuration "wjammers.cfg" pour le jeu "wjammers.zip" (WindJammers).
{% endhint %}

<div align="left"><figure><img src="https://i.imgur.com/SzXa5UY.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
N’hésitez pas à partager les fichiers que vous avez créé avec l'équipe RetroBat si vous avez un profil général pouvant être partagé avec d'autres utilisateurs.
{% endhint %}

## Libretro-mame

RetroBat propose une configuration automatique pour MAME dans le cadre de la configuration automatique de RetroArch. Cependant, comme les bornes d'arcade MAME disposent d'une grande variété de types de commandes, il est possible de générer une configuration spécifique à chaque jeu. Les méthodes de configuration suivantes sont disponibles pour libretro-mame au sein de RetroBat :

* Autoconfiguration standard RetroBat
* Avec la surcharge RetroBat des fichiers xml (par jeu)

### Autoconfiguration RetroBat&#x20;

Par défaut, RetroBat tentera de configurer automatiquement les commandes dans libretro-mame, soit en utilisant les paramètres fournis par RetroBat pour chaque jeu, soit en utilisant le mappage RetroPad par défaut de RetroArch.\
\
La configuration automatique peut varier en fonction de la disposition de la manette que vous spécifiez dans **CONFIGURATION AVANCÉE DU SYSTÈME > CONTRÔLES :**

<div align="left"><figure><img src="../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure></div>

### Surcharge RetroBat des fichiers xml par jeu

Lisez [ce chapitre](configuration-des-touches-retroarch.md#utilisation-dun-fichier-de-remappage-pour-un-coeur) pour plus d'informations.

RetroBat peut utiliser un fichier YAML de remappage pour la bibliothèque libretro-mame ; ce fichier se trouve dans le dossier `system/resources/inputmapping` de votre installation RetroBat et s'appelle **libretro\_mame.yml**.

{% hint style="info" %}
Si vous souhaitez modifier ce fichier, copiez-le d'abord dans le dossier `user\inputmapping` de votre installation RetroBat, sinon il risque d'être effacé lors d'une future mise à jour de RetroBat.
{% endhint %}

Le fichier de remappage est un fichier YAML ; chaque conteneur contient le remappage RetroArch correspondant à un jeu ou à une configuration :

<div align="left"><figure><img src="../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure></div>
