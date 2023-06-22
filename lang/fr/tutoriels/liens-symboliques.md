---
description: Stockez vos ROMs dans un dossier différent
---

# Liens symboliques

Les Liens Symboliques permettent de créer un un accès transparent à un dossier ou à un fichier.

Contrairement à un simple raccourci (.lnk) (qui est un processus en 2 étapes pour lequel quelque chose doit lire et interpréter le contenu du fichier de raccourci puis ouvrir le fichier qu'il référence), quand une application utilise un lien symbolique, elle accède directement à l'objet donnée référencé par le lien symbolique (c'est donc un processus en une seule étape).

L'avantage de cette fonctionnalité dans le cadre de Retrobat, est qu'elle vous permettra de stocker vos jeux ou tout autre dossiers (bios...) sur un disque différent de celui sur lequel Retrobat est installé.

**Exemple:**

<div align="left">

<figure><img src="https://i.imgur.com/v7XAUFu.png" alt=""><figcaption></figcaption></figure>

</div>

## Comment créer un Lien Symbolique ?

Il existe 2 façons pour gérer les liens symboliques:

* L'utilisation de lignes de commandes dans la console Windows (par la commande mklink)
* L'utilisation d'un logiciel tiers nommé "Link Shell Extension"

C'est cette deuxième méthode que nous allons détailler dans ce guide.

### Télécharger Link Shell Extension

Télécharger le programme sur le site web suivant: [https://schinagl.priv.at/nt/hardlinkshellext/linkshellextension\_fr.html#download](https://schinagl.priv.at/nt/hardlinkshellext/linkshellextension\_fr.html#download)

### Utilisation de Link Shell Extension

Une fois le programme installé, il est nécessaire de redémarrer l'ordinateur ou de redémarrer le processus "explorer.exe" depuis le Gestionnaire de Tâches.

Ensuite, 2 nouvelles options seront disponibles dans le menu contextuel affiché lorsque vous effectuez un clic droit:

* Prendre comme cible du lien

<div align="left">

<figure><img src="https://i.imgur.com/DJ3yi2r.png" alt=""><figcaption></figcaption></figure>

</div>

* Coller...

<div align="left">

<figure><img src="https://i.imgur.com/j2TnYfg.png" alt=""><figcaption></figcaption></figure>

</div>

### Créer un Lien Symbolique avec Link Shell Extension

Dans l'exemple ci-dessous, nous assumons que les jeux 3do sont stockés dans le dossier `D:\Retrobat\3do` et que le dossier d'installation de Retrobat est `C:\Retrobat`.

1. Assurez-vous que tous les jeux et fichiers annexes (gamelist, images, vidéos...) ont bien été copiés dans `D:\Retrobat\3do` et que le dossier `C:\Retrobat\roms\3do` ne contient plus aucun fichier que vous souhaitez conserver
2. Supprimez le dossier `C:\Retrobat\roms\3do`
3. Effectuez un clic droit sur le dossier `D:\Retrobat\3do` et sélectionnez "**Prendre comme cible du lien**"
4. Allez dans le dossier `C:\Retrobat\roms` , effectuez un clic droit à l'intérieur du dossier et sélectionnez "**Coller... > un lien symbolique**"
5. Le dossier `C:\Retrobat\roms` contient désormais un dossier 3do contenant une petite icône de raccourci: ![](<../.gitbook/assets/image (31).png>)&#x20;

**FÉLICITATIONS**: vous venez de créer votre premier lien symbolique !

Vous pouvez désormais répéter cette opération pour tout dossier que vous souhaiteriez stocké à un emplacement différent de l'emplacement prévu par défaut.

### Créer un lien symbolique avec l'invitation de commande Windows

Reprenons l'exemple ci-dessus.

1. Assurez-vous que tous les jeux et fichiers annexes (gamelist, images, vidéos...) ont bien été copiés dans `D:\Retrobat\3do` et que le dossier `C:\Retrobat\roms\3do` ne contient plus aucun fichier que vous souhaitez conserver
2. Supprimez le dossier `C:\Retrobat\roms\3do`
3. Ouvrir l'invitation de commande Windows et taper: `mklink /D "C:\Retrobat\roms\3do" "D:\Retrobat\3do`
4. Le dossier `C:\Retrobat\roms` contient désormais un dossier 3do contenant une petite icône de raccourci: ![](<../.gitbook/assets/image (31).png>)&#x20;

<div align="left">

<figure><img src="https://i.imgur.com/wgrK31v.png" alt=""><figcaption></figcaption></figure>

</div>
