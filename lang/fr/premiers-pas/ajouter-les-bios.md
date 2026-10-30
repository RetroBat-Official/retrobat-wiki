# Ajouter les BIOS

Certains émulateurs ont besoin de fichiers BIOS pour fonctionner correctement.

{% hint style="warning" %}
Les BIOS sont des fichiers protégés par le droit d'auteur : RetroBat ne les fournit pas, et l'équipe ne peut pas légalement les distribuer. Vous devez les extraire de votre propre matériel d'origine.
{% endhint %}

## Emplacement

Pour la plupart des systèmes, les fichiers BIOS doivent être placés dans le dossier `bios` de RetroBat, par exemple `C:\RetroBat\bios\`.

<div align="left"><figure><img src="../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
* Le nom des fichiers doit correspondre **exactement** au nom attendu par RetroBat (par exemple `scph5501.bin`). Ne les renommez pas.
* Pour certains systèmes, les BIOS doivent être placés dans un sous-dossier ou dans un autre emplacement. C'est précisé dans la page de chaque système, dans la section [Systèmes compatibles](../systemes-and-emulateurs/supported-game-systems/), avec la liste des BIOS nécessaires.
{% endhint %}

## Vérification des BIOS manquants

RetroBat peut vérifier vos fichiers BIOS : ouvrez le [MENU PRINCIPAL](../navigation/main-menu.md), allez dans [PARAMÈTRES DES JEUX](../navigation/main-menu.md#parametres-des-jeux), puis sélectionnez **VÉRIFIER LES BIOS MANQUANTS** dans le groupe **PARAMÈTRES BIOS**.

<div align="left"><figure><img src="../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure></div>

Le résultat liste, pour chaque système, les BIOS qui posent problème :

* **Manquant** ![](<../.gitbook/assets/image (253).png>) : le fichier n'a pas été trouvé.
* **Invalide** ![](<../.gitbook/assets/image (255).png>) **:** le fichier est présent, mais sa somme de contrôle (MD5) ne correspond à aucune version connue. Il peut tout de même fonctionner : testez le système pour vous en assurer.

<div align="left"><figure><img src="../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Par défaut, RetroBat vérifie aussi les BIOS au lancement d'un jeu. S'il manque un BIOS pour le système, un avertissement s'affiche et vous pouvez choisir de lancer le jeu quand même.

Cette vérification peut être désactivée avec l'option **VÉRIFIER LES BIOS AVANT DE LANCER UN JEU**, dans le même groupe **PARAMÈTRES BIOS**.
{% endhint %}
