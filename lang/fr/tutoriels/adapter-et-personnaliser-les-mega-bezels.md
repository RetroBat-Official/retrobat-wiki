# Adapter et personnaliser les Mega-Bezels

Retrobat vous permet de télécharger les Mega-Bezels, un ensemble de décorations et de filtres vidéos. Vous pouvez retrouver d'avantages d'informations dans la section [Décorations & Bezels](../utilisation-avancee/decorations-and-bezels.md#les-mega-bezels) du wiki.&#x20;

<div align="left">

<figure><img src="https://i.imgur.com/G9GEGwh.png" alt=""><figcaption></figcaption></figure>

</div>

## Emplacement des éléments

### Retrobat

Les éléments permettant de faire apparaitre les Mega-Bezels dans les menus jeux de Retrobat se trouvent dans le dossier`system\shaders\configs` de votre installation.

<div align="left">

<figure><img src="https://i.imgur.com/7SEscUi.png" alt=""><figcaption></figcaption></figure>

</div>

Chacun des dossiers contient un fichier `rendering-defaults.yml` qui indique : \
\- en premier le système concerné, \
\- en dessous le "preset" (fichier de préselection) qui sera appelé pour ce système

<figure><img src="https://i.imgur.com/tLGT8CN.png" alt=""><figcaption></figcaption></figure>

### RetroArch

Les éléments nécessaires au fonctionnement des Mega-Bezels dans Retroarch se situent dans le répertoire `emulators\retroarch\shaders\shaders_slang\Duimon-Mega-Bezel\` de votre installation Retrobat.

<div align="left">

<figure><img src="https://i.imgur.com/fgpBn8a.png" alt=""><figcaption></figcaption></figure>

</div>

## Ajout d'une nouvelle entrée de présélection dans le menu Retrobat

### Modification du preset

Pour l'exemple, nous allons ajouter une option dans le preset qui permet de "retourner" l'image.\
En effet, pour certains cores, le rendu hardware peut inverser le tampon d'image, ce qui fait que certains utilisateurs se retrouvent avec une décoration inversée

<div align="left">

<figure><img src="https://i.imgur.com/c0QPInK.png" alt=""><figcaption><p>Décoration inversée pour SEGA Saturn</p></figcaption></figure>

</div>

Nous allons commencer par créer l'instruction permettant d'inverser l'image dans le fichier preset.\
Pour cela, il faut commencer par copier des presets existants, qui se situent dans le répertoire `emulators\retroarch\shaders\shaders_slang\Duimon-Mega-Bezel\`. \


Dans notre exemple, nous copierons les plus couramment utilisés, a savoir \[Bezel] et \[Bezel]-\[Night], dans le système Sega Saturn en mode "Advanced" :&#x20;

<figure><img src="https://i.imgur.com/INWfURU.png" alt=""><figcaption></figcaption></figure>

Puis, nous allons renommer ces presets afin de pouvoir les identifier plus facilement.\
Ajoutons la balise \[VFlip] (pour Vertical Flip) et veillons a ne pas laisser d'espaces dans le nom du fichier:&#x20;

<figure><img src="https://i.imgur.com/VJea3ZI.png" alt=""><figcaption></figcaption></figure>

Ensuite, nous allons ouvrir ces deux fichiers l'un après l'autre avec un éditeur de texte, et ajouter l'instruction permettant de retourner l'image.\
il s'agit de la ligne `HSM_FLIP_VIEWPORT_VERTICAL = "1.000000"`

<figure><img src="https://i.imgur.com/HiXJkq0.png" alt=""><figcaption><p>Toutes les différentes lignes composent le presets, et donne a Retroarch les instructions d'affichage, de filtres vidéos, de taille...</p></figcaption></figure>

### Appel du nouveau preset depuis le menu Retrobat

Il faut désormais utiliser le fichier que nous avons modifié.\
Pour cela, depuis le dossier `system\shaders\configs`, dupliquer l'un des dossier existant (dans notre exemple le "mega-bezel-advanced-night") et renommer-le pour pouvoir le différencier facilement dans le menu Retrobat (dans notre exemple "mega-bezel-advanced-night-VFlip") :

<figure><img src="https://i.imgur.com/AxSDahs.jpg" alt=""><figcaption></figcaption></figure>

A l'intérieur de ce dossier, se trouve un fichier "rendering-defaults.yml".\
C'est lui qui indique à Retroarch quel preset utiliser, pour quel système.\
La première ligne correspond au système, tel qu'il est connu dans Retrobat et EmulationStation (en cas de doute, vous pouvez retrouver l'information dans `\emulationstation.emulationstation\es_systems.cfg`).\
La seconde correspond au preset qui sera utilisé pour ce système, en pointant vers le fichier .slangp correspondant (le chemin est relatif) :&#x20;

<figure><img src="https://i.imgur.com/SvVwEBZ.png" alt=""><figcaption></figcaption></figure>

Dans notre cas, nous allons choisir le preset que nous venons tout juste de modifier. Il n'est pas nécessaire d'ajouter l'extension .slangp :&#x20;

<figure><img src="https://i.imgur.com/nOO5d9c.png" alt=""><figcaption></figcaption></figure>

Enregistrer, et fermer les fichiers.

\
En lançant Retrobat, vous trouverez maintenant dans les filtres vidéos l'entrée "mega-bezel-advanced-night-vflip".\
Vous pouvez faire une sélection "par-système", de façon a ce que ce preset ne soit utilisé que dans le cas du système Saturn :&#x20;

<figure><img src="https://i.imgur.com/r6R365E.png" alt=""><figcaption></figcaption></figure>

Le Mega-Bezel apparaitra alors inversé par rapport a son positionnement initial.

<figure><img src="https://i.imgur.com/EkippyM.png" alt=""><figcaption></figcaption></figure>

{% embed url="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCgoewyw8Sagl6SNUMrCG%2Fuploads%2F6i5dHhfTffjYicfwkM7C%2FVerticalFlip-Shaders3.mp4?alt=media&token=ecd83899-152f-452d-b5c6-fefd52fd3f94" %}

D'autres réglages sont également possibles, chaque système possédant plusieurs presets selon ses caractéristiques (vertical, cabinet...).\
N'hésitez pas à consulter le GitHub de Duimon pour plus d'infos : [https://github.com/Duimon/Duimon-Mega-Bezel](https://github.com/Duimon/Duimon-Mega-Bezel)\


{% embed url="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCgoewyw8Sagl6SNUMrCG%2Fuploads%2F4GBUEMCfoEYBAeER58HG%2FEdit%20Shaders%20Presets.mp4?alt=media&token=ae36a62c-76b7-4e24-a0b3-86581f79cba9" %}
