# Ajouter des filtres vidéos Retroarch à Retrobat

Retrobat inclus dans sa configuration d'origine une liste de filtres vidéos (shaders) prédéfinis, mais tous les filtres disponibles depuis Retroarch n'apparaissent pas par défaut dans cette liste.

Vous pouvez ajouter manuellement de nouveaux filtres vidéos pour les cores libretro, voici comment procéder :

<div align="left">

<figure><img src="https://i.imgur.com/ZQ8UAUt.png" alt=""><figcaption></figcaption></figure>

</div>

## Emplacement des filtres vidéos

### Retrobat

Les filtres vidéos disponibles dans Retrobat se situent dans le répertoire  `\system\shaders\configs` de votre installation.

<div align="left">

<figure><img src="https://i.imgur.com/ChxJMdd.png" alt=""><figcaption></figcaption></figure>

</div>

### RetroArch

Les filtres vidéos disponibles dans Retroarch se situent dans le répertoire `\retroarch\shaders\` de votre installation Retrobat.

Ils sont d'abord classés par le type de filtres (glsl or slang) :

* GLSL : Filtres vidéos disponible pour OpenGL.
* Slang : Nouveaux formats de filtres vidéos, recommandés lorsqu'ils sont disponibles. Compatibles Vulkan, Direct3D 10/11/12, et core OpenGL.

{% hint style="info" %}
Retrobat reherche automatiquement les filtres dans le dossier correspondant au pilote vidéo sélectionné pour le jeu. Par défaut, pour Retroarch, le driver est réglé sur OpenGL.
{% endhint %}

Exemple de dossier contenant les filtres vidéos GLSL :

<div align="left">

<figure><img src="https://i.imgur.com/ijn2wYK.png" alt=""><figcaption></figcaption></figure>

</div>



## Ajout d'un nouveau filtre vidéo dans le menu Retrobat

Pour l'exemple, nous chercherons a ajouter le filtre vidéo "advcartoon" à la liste de filtre prédéfinis de Retrobat, ce filtre étant disponible aussi bien en GLSL qu'en SLANG :

| ![](https://2703045246-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FexdzL60ZuqPLldz2AYta%2Fuploads%2F34bRH58z1B2IkcYR7i1P%2Fimage.png?alt=media\&token=f843ec53-0d7b-46a1-884f-7a9f568572f7) | ![](https://2703045246-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FexdzL60ZuqPLldz2AYta%2Fuploads%2FKfi7h9NrJo7HCm7juqjn%2Fimage.png?alt=media\&token=6cdef858-a02f-46e5-9e2b-85e542eda744) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

Le filtre vidéo se situe dans le dossier `\retroarch\shaders\shaders_xxxx\cel` et se nomme "advcartoon.glslp".

Pour qu'il apparaisse dans le menu Retrobat, il faut se rendre dans le dossier `\system\shaders\configs` et créer un nouveau répertoire, que l'on nommera par exemple  "advcartoon" :

<div align="left">

<figure><img src="https://i.imgur.com/xkrY1en.png" alt=""><figcaption></figcaption></figure>

</div>

Dans ce répertoire, créer un fichier texte nommé "**rendering-defaults**" et renommer l'extension .txt en .yml :

<div align="left">

<figure><img src="https://i.imgur.com/oNGcd2L.png" alt=""><figcaption></figcaption></figure>

</div>

Ouvrir le fichier avec un éditeur de texte, et ajouter le texte suivant :&#x20;

```yaml
default:
  shader: <dossier du filtre retroarch>/<nom du fichier sans extension>
```

Pour notre exemple, cela correspond à :

```yaml
default:
  shader: cel/advcartoon
```

<div align="left">

<figure><img src="https://i.imgur.com/uKOVcK3.png" alt=""><figcaption></figcaption></figure>

</div>

Le nouveau filtre vidéo apparait désormais dans Retrobat :

<div align="left">

<figure><img src="https://i.imgur.com/2ZKdvDC.png" alt=""><figcaption></figcaption></figure>

</div>

Certains shaders peuvent être adaptés de façon spécifiques à certains systèmes, pour reproduire avec plus de fidélité le rendu visuel de ceux-ci. C'est pour cela qu'il est possible d'utiliser différents shaders par système, au sein du même fichier **rendering-defaults.yml**; il faut ajouter le nom du système pour lequel le shader doit être différent de celui par défaut (NB : il s'agit des noms présent dans le fichier **es\_systems.cfg** entre les balises \<name>).

<figure><img src="https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2Fi.imgur.com%2Fknv5MPm.png&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=5f17ffec1819c7a71815ffdb0284bb3a95fbf3a948337f7919faba860567b7b9" alt=""><figcaption></figcaption></figure>

Enfin, certains émulateurs standalone peuvent également utiliser les shaders retroarch. Il faut alors rajouter le nom de l'émulateur sur une seconde ligne, suivi par le shader a utiliser.

<figure><img src="https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2Fi.imgur.com%2FAC6PXNK.png&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=03948f3d221a0e075ba53bda6267f34f1c22158f4341db3aa1b837d479b94147" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Pour éviter tout risque de voir disparaitre ses fichiers de configuration lors d'une mise à jour de RetroBat, il est recommandé de sauvegarder les dossiers de config crées manuellement, de façon a pouvoir les remettre en place rapidement si nécessaire.
{% endhint %}
