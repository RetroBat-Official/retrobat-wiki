# Configuration des touches RetroArch

Le mappage des contrôleurs sous RetroArch est très spécifique, avant de rentrer dans le détail il est important de comprendre le principe de mappage générale de RetroArch.

### Principe du mappage dans RetroArch <a href="#retroarch-mapping-principle" id="retroarch-mapping-principle"></a>

Les Informations sur la façon dont RetroArch gère les contrôles se trouve ici :&#x20;

{% embed url="https://docs.libretro.com/guides/input-and-controls/" %}

RetroArch à une approche en 2 phases concernant le mappage des contrôleurs :&#x20;

* Étape 1 : Configuration de votre manette physique avec « RetroPad » de RetroArch
* Étape 2 : Configuration du Retropad avec la manette d'origine de la console ou de l'ordinateur

<div align="left"><figure><img src="../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure></div>

Le guide présenté sur cette page porte principalement sur la deuxième étape, car il part du principe que RetroBat transmet toutes les commandes de votre manette physique à RetroArch (ce qui devrait toujours être le cas si vous avez correctement configuré votre manette dans RetroBat).

**Configuration générale**

La configuration effectuée à l'étape 1 se trouve dans la section suivante de la configuration de RetroArch :

<div align="left"><figure><img src="../../.gitbook/assets/image (132).png" alt="" width="375"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (133).png" alt="" width="375"><figcaption></figcaption></figure></div>

{% hint style="info" %}
Le réglage général est stocké dans le fichier "**retroarch.cfg**" situé dans le dossier `/emulators/retroarch`
{% endhint %}

**Remap**

Les informations de reconfiguration (étape 2) sont accessibles dans le menu « Paramètres rapides » de RetroArch, pendant qu'un cœur est en cours d'exécution :

<div align="left"><figure><img src="../../.gitbook/assets/image (134).png" alt="" width="294"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (135).png" alt="" width="342"><figcaption></figcaption></figure></div>

{% hint style="info" %}
Les fichiers de remappage sont enregistrés au format .rmp dans le dossier `/emulators/retroarch/config/remaps`.
{% endhint %}

### Comment modifier le remappage dans RetroArch lorsque l'on utilise RetroBat ?

RetroBat propose plusieurs façons de modifier le remappage de votre manette dans RetroArch ; le wiki vous guidera à travers les méthodes suivantes :

* ​[Enregistrer manuellement un fichier de remappage pour un jeu](configuration-des-touches-retroarch.md#manually-create-a-remap-file-for-a-game) (remap)
* ​[Utiliser un fichier d'override YAML pour le core](configuration-des-touches-retroarch.md#utilisation-dun-fichier-de-remappage-pour-un-coeur) (remap)
* ​[Forcer une configuration pour un type particulier de manette](configuration-des-touches-retroarch.md#imposer-une-configuration-de-touche) (changer le mapping de la manette)
* Forcer un contrôleur de type "clavier" (tel que IPAC2 ou TankStick)​
* [Activer un type de manette spécial](configuration-des-touches-retroarch.md#activer-un-type-de-controleur-specifique) (pour certains systèmes/cœurs uniquement)
* ​[Utiliser un layout différent fourni en option dans RetroBat](configuration-des-touches-retroarch.md#utilisation-dune-disposition-de-touches-predefini)

### Création manuelle d'un fichier de remappage pour un jeu <a href="#manually-create-a-remap-file-for-a-game" id="manually-create-a-remap-file-for-a-game"></a>

Ouvrir RetroBat et démarrer un jeu pour lequel il est nécessaire de créer un paramétrage spécifique des touches.\
\
Une fois dans le jeu, appuyer sur les touches SELECT + ![](<../../.gitbook/assets/image (20) (1).png>) simultanément pour ouvrir le menu  RetroArch, et choisir **Menu rapide**&#x20;

<div align="left"><figure><img src="https://i.imgur.com/w1hW2nI.png" alt=""><figcaption></figcaption></figure></div>

Dans le MENU RAPIDE, aller dans la section " **Touches** "

<div align="left"><figure><img src="https://i.imgur.com/thwZ08G.png" alt=""><figcaption></figcaption></figure></div>

Puis, sélectionner le port souhaité et paramétrer comme désiré :

<div align="left"><figure><img src="https://i.imgur.com/NBbomL3.png" alt=""><figcaption></figcaption></figure></div>

\
Dans cet exemple, la touche Analogique gauche haut du Retropad a été mappé sur la touche défini comme A dans RetroBat (qui correspond à la touche W sur le clavier) :

<div align="left"><figure><img src="https://i.imgur.com/4aS0EX9.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Vous ne pouvez reparamétrer que les touches qui ont été paramétrées dans les paramètres généraux Retroarch pour le contrôleur utilisé.
{% endhint %}

Une fois le paramétrage fait, sortir et retourner sur le menu **TOUCHES**, puis sélectionner "_Gérer les fichiers de remappage_" :

<div align="left"><figure><img src="https://i.imgur.com/7gkrHwE.png" alt=""><figcaption></figcaption></figure></div>

Dans le sous-menu suivant, sauvegarder la configuration des touches pour le jeu (et il ne s'appliquera que pour celui-ci)

<div align="left"><figure><img src="../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure></div>

Une fois sauvegardé, le nouveau fichier de configuration sera utilisé au prochain lancement du jeu.

{% hint style="info" %}
Il n'est pas possible d'utiliser l'option "Sauvegarder le remappage pour le coeur", celui-ci étant utilisé par RetroBat, il sera automatiquement supprimé au démarrage suivant.
{% endhint %}

### Utilisation d'un fichier de remappage pour un cœur

Lisez [ce chapitre](../controller-configuration.md#utiliser-les-fichiers-de-remplacement-retrobat) pour des informations générales.

Les fichiers de reconfiguration par cœur fournis par RetroBat se trouvent dans le dossier `\system\resources\inputmapping` de votre installation RetroBat, ils commencent avec le préfixe "**libretro\_**".

La logique utilisée par RetroBat pour accéder à ce fichier est la suivante :&#x20;

1. Chercher dans `\user\inputmapping` un fichier nommé **libretro\_\<core>\_\<system>.yml**
2. Chercher dans `\user\inputmapping` un fichier nommé **libretro\_\<core>.yml**
3. Chercher dans `\user\inputmapping` un fichier nommé **libretro.yml**
4. Chercher dans `\system\resources\inputmapping`  un fichier nommé **libretro\_\<core>\_\<system>.yml**
5. Chercher dans `\system\resources\inputmapping` un fichier nommé **libretro\_\<core>.yml**
6. Chercher dans `\system\resources\inputmapping` un fichier nommé **libretro.yml**

Si un fichier yaml est trouvé, RetroBat le lira et cherchera un conteneur nommé à l'identique du nom du jeu :

<div align="left"><figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure></div>

Si aucun conteneur n'existe pour le jeu, RetroBat essaiera d'utiliser le conteneur "default":

<div align="left"><figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Pour les systèmes Arcade, un même jeu peut avoir plusieurs configurations, selon les options définies dans l'interface de RetroBat, sous PARAMÈTRES AVANCÉS > CONTRÔLES :

![](<../../.gitbook/assets/image (78).png>)

RetroBat cherchera alors le conteneur correspondant à la disposition des boutons sélectionnée dans le menu RetroBat, puis il cherchera sur le conteneur spécifique au jeu :

![](<../../.gitbook/assets/image (73).png>)
{% endhint %}

Lorsqu'un conteneur spécifique est détecté, RetroBat génère et modifie automatiquement le fichier de remappage du cœur au moment du lancement d'un jeu, ce qui applique automatiquement le remappage sélectionné :

<div align="left"><figure><img src="../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure></div>

### Imposer un mapping pour un contrôleur

Il est possible de forcer l'utilisation d'une manette avec une configuration spécifique. Cela s'avère utile lorsqu'une manette donnée n'est pas correctement configurée par RetroBat ou lorsqu'elle n'est pas reconnue par RetroArch, mais fonctionne correctement après avoir effectué un mappage manuel dans les options de configuration de RetroArch.

RetroBat est fourni avec un fichier spécifique nommé "**retroarch\_controller.json**" situé dans le répertoire `\system\resources\inputmapping` de votre installation RetroBat.

Ce fichier est au format JSON ; il contient le mappage exact requis dans le fichier `retroarch.cfg`, basé sur le GUID SDL de la manette :

<div align="left"><figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure></div>

L'exemple ci-dessus concerne la manette NSO N64 ; les différentes valeurs à indiquer dans le fichier sont les suivantes :

* **Name** : Seulement à titre d'information
* **Guid** : permet à RetroBat d'activer la configuration spécifique en fonction de la manette connectée (le GUID SDL de la manette se trouve dans le fichier es\_input.cfg ou dans le fichier emulatorlauncher.log après le lancement d'un jeu). Il est possible de saisir plusieurs GUID si une manette comporte plusieurs versions).
* **Driver** : peut être utilisé si la configuration de RetroArch varie en fonction du pilote Joypad sélectionné dans RetroArch ; les valeurs possibles sont : sdl2 (par défaut dans RetroBat), xinput, dinput
* **Mapping** : Le mappage à définir dans le fichier  `retroarch.cfg`, pour chaque bouton. Pour connaître le mappage de la manette, effectuez la configuration manuellement en lançant retroarch.exe, quittez RetroArch, puis ouvrez le fichier retroarch.cfg et recherchez les lignes commençant par input\_player1\_ et se terminant par btn ou axis.
* **HotkeyMapping** : la configuration des raccourcis clavier pour la manette
* **ControllerInfo** : peut servir à régler la sensibilité analogique ou à d'autres fins spécifiques (n'hésitez pas à contacter l'équipe RetroBat si vous avez besoin d'une fonctionnalité particulière)

{% hint style="info" %}
N'hésitez pas à partager avec l'équipe RetroBat toute configuration de manette que vous auriez créée.
{% endhint %}

### Forcer un contrôleur de type clavier

Certains contrôleurs sont reconnus par Windows comme des claviers ; c'est le cas, par exemple, du X-Arcade Tankstick ou de l'IPAC2.\
\
RetroBat propose une configuration automatique pour ces contrôleurs, qui est forcée à partir d'un fichier YAML situé dans le dossier `\system\resources\inputmapping\kbpads` de votre installation RetroBat :\
\
Ce fichier contient le mappage à appliquer dans RetroArch pour un périphérique :

<div align="left"><figure><img src="../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure></div>

Si vous possédez l'un de ces appareils, vous pouvez activer le mappage automatique depuis le menu RetroBat général **MENU GÉNÉRAL > PARAMÈTRES DES JEUX > OPTIONS RETROARCH >  CONTRÔLES :**

<div align="left"><figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Si vous possédez une autre manette reconnue comme un clavier, vous pouvez partager la configuration avec l'équipe RetroBat ; elle sera alors ajoutée de la même façon dans RetroBat.
{% endhint %}

### Activer un type de contrôleur spécifique

Accédez [à cette page du wiki](../supported-controllers/gamepads/controleurs-speciaux.md) pour plus d'informations.

### Utilisation d'une disposition de touches prédéfinie

RetroBat offre, pour de nombreux systèmes, la possibilité de changer la dispositions des touches.

L'option se trouve généralement dans le menu **Réglages avancés > contrôles** :

<div align="left"><figure><img src="../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure></div>

Plus d'informations sur les différentes dispositions de touches se trouvent sur [la page du système](../../systemes-and-emulateurs/supported-game-systems/).
