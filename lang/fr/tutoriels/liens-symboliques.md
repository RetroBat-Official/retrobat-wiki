---
description: Stocker vos jeux dans un autre dossier
---

# Liens symboliques

Windows prend en charge les **liens symboliques** : un dossier qui pointe vers un autre dossier, ailleurs sur l'ordinateur ou sur le réseau.

**Quel intérêt pour RetroBat ?** Vous pouvez garder vos jeux en dehors du dossier `roms` de RetroBat (sur un disque dur plus grand, ou sur un NAS), tout en les laissant visibles pour RetroBat dans `roms`.

**Exemple :**

<div align="left"><figure><img src="../.gitbook/assets/image (458).png" alt=""><figcaption></figcaption></figure></div>

## Créer un lien symbolique

Il existe trois méthodes : l'outil **Link Shell Extension** (la plus simple), ou l'**invite de commandes** avec une jonction ou un lien symbolique.

{% hint style="warning" %}
Avant de créer un lien, déplacez vos jeux vers le nouvel emplacement et vérifiez que le dossier que vous remplacez dans `roms` ne contient rien à garder : il doit être supprimé, car un lien ne peut pas être créé à la place d'un dossier existant.
{% endhint %}

### Télécharger Link Shell Extension

Télécharger le programme sur le site web suivant: [https://schinagl.priv.at/nt/hardlinkshellext/linkshellextension\_fr.html#download](https://schinagl.priv.at/nt/hardlinkshellext/linkshellextension_fr.html#download)

### Utiliser Link Shell Extension

Après l'installation, redémarrez l'ordinateur (ou relancez le processus `explorer.exe`). De nouvelles options apparaissent avec le clic droit :

* **Prendre comme cible du lien**

<div align="left"><figure><img src="../.gitbook/assets/image (461).png" alt=""><figcaption></figcaption></figure></div>

* **Coller...** (un lien symbolique ou une jonction)

<div align="left"><figure><img src="../.gitbook/assets/image (462).png" alt=""><figcaption></figcaption></figure></div>

## Créer un lien symbolique avec Link Shell Extension

Dans cet exemple, les jeux 3DO sont dans `D:\Retrobat\3do`, et RetroBat est installé dans `C:\Retrobat`.

1. Copiez tous vos jeux dans `D:\Retrobat\3do`. Vérifiez que `C:\Retrobat\roms\3do` ne contient rien à garder.
2. Supprimez le dossier `C:\Retrobat\roms\3do`.
3. Faites un clic droit sur `D:\Retrobat\3do` et choisissez **Prendre comme cible du lien**.
4. Ouvrez `C:\Retrobat\roms`, faites un clic droit dans le dossier et choisissez **Coller... > un lien symbolique**.
5. Le dossier `3do` apparaît maintenant dans `C:\Retrobat\roms` avec une petite flèche sur son icône :&#x20;

![](<../.gitbook/assets/image (464).png>)

**FÉLICITATIONS** : vous venez de créer un lien symbolique ! Faites de même pour chaque dossier que vous voulez stocker ailleurs.

## Créer un lien avec l'invite de commandes

Même exemple que ci-dessus. Faites d'abord les étapes 1 et 2 ci-dessus, puis utilisez l'une de ces commandes.

### Disque local : jonction (sans droits administrateur)

Ouvrez une **invite de commandes** (`cmd`) et tapez :

```
mklink /J "C:\Retrobat\roms\3do" "D:\Retrobat\3do"
```

### Partage réseau (NAS) : lien symbolique

Ouvrez une **invite de commandes en administrateur** (clic droit sur **Invite de commandes** > **Exécuter en tant qu'administrateur**) et tapez :

```
mklink /D "C:\Retrobat\roms\3do" "\\NAS\Jeux\3do"
```

{% hint style="info" %}
* Utilisez le chemin réseau (`\\NAS\...`), et non une lettre de lecteur réseau (`Z:\`) : les lecteurs réseau ne sont pas visibles depuis une invite de commandes en administrateur.
* `mklink /D` fonctionne aussi pour un disque local, mais demande les droits administrateur (ou le **mode développeur** de Windows).
{% endhint %}

Le dossier `3do` apparaît maintenant dans `C:\Retrobat\roms` avec une petite flèche sur son icône :

&#x20;![](<../.gitbook/assets/image (32).png>)&#x20;

## Lier tout le dossier roms

Pour stocker tous vos jeux ailleurs en une seule fois, liez tout le dossier `roms` au lieu de chaque système :

1. Déplacez le contenu de `C:\Retrobat\roms` vers `D:\Retrobat\roms`.
2. Supprimez le dossier vide `C:\Retrobat\roms`.
3. Créez le lien : `mklink /J "C:\Retrobat\roms" "D:\Retrobat\roms"` (ou `/D` pour un partage réseau).

## Bon à savoir

* **Données des jeux :** les listes de jeux (`gamelist.xml`) et les images et vidéos scrapées sont enregistrées dans les dossiers des jeux : elles sont donc aussi sur le disque cible.
* **Supprimer un lien :** supprimez le dossier du lien dans `roms` (celui avec la flèche), ou tapez `rmdir "C:\Retrobat\roms\3do"`. Seul le lien est supprimé : vos jeux restent dans `D:\Retrobat\3do`.

{% hint style="danger" %}
Ne supprimez pas le **contenu** du dossier du lien : les fichiers que vous y voyez sont vos vrais jeux, et ils seraient supprimés du disque cible.
{% endhint %}

* **Partage réseau :** le chargement des listes de jeux est plus lent par le réseau. Si le NAS n'est pas disponible au démarrage de RetroBat, les systèmes liés apparaissent vides.
