# Mises à jour et téléchargements

## Mises à jour

RetroBat se met à jour depuis le menu **MISES À JOUR & TÉLÉCHARGEMENTS**.

### Réglages des mises à jour

Dans **MENU PRINCIPAL > MISES À JOUR & TÉLÉCHARGEMENTS**, groupe **MISES À JOUR LOGICIEL** :

<table><thead><tr><th width="236.5">Option</th><th>Description</th></tr></thead><tbody><tr><td><strong>VÉRIFIER LES MISES À JOUR</strong></td><td>Vérifie au démarrage de RetroBat si une nouvelle version existe, et affiche un message si c'est le cas</td></tr><tr><td><strong>TYPE DE MISE À JOUR</strong></td><td><strong>stable</strong> (par défaut) ou <strong>beta</strong> (versions de test, qui peuvent contenir des bugs)</td></tr></tbody></table>

<div align="left"><figure><img src="../.gitbook/assets/image (407).png" alt=""><figcaption></figcaption></figure></div>

Quand une nouvelle version est disponible, un message s'affiche en haut de l'écran :

<figure><img src="../.gitbook/assets/image (406).png" alt=""><figcaption></figcaption></figure>

### Mettre à jour RetroBat

1. Ouvrez **MENU PRINCIPAL > MISES À JOUR & TÉLÉCHARGEMENTS** et sélectionnez **LANCER LA MISE À JOUR**.
2. RetroBat affiche votre version et la nouvelle : confirmez avec **OUI**.

<div align="left"><figure><img src="../.gitbook/assets/image (408).png" alt=""><figcaption></figcaption></figure></div>

3. La progression du téléchargement et de l'installation s'affiche en haut à droite. Attendez le message **LA MISE À JOUR EST PRÊTE**.

<div align="left"><figure><img src="../.gitbook/assets/image (409).png" alt=""><figcaption></figcaption></figure></div>

4. Sélectionnez **APPLIQUER LA MISE À JOUR** (même menu) ou quittez et relancez RetroBat. RetroBat termine la mise à jour au démarrage.

Votre version actuelle est indiquée dans **MENU PRINCIPAL > PARAMÈTRES SYSTÈME > INFORMATIONS**.

<div align="left"><figure><img src="../.gitbook/assets/image (410).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Une mise à jour remplace les fichiers fournis avec RetroBat. Vos propres fichiers sont conservés : placez vos personnalisations dans le dossier `user` (padtokey, inputmapping, tattoos…) et dans `decorations`.
{% endhint %}

### Mise à jour manuelle (es-update)

Si la mise à jour échoue depuis le menu (connexion lente ou bloquée, ordinateur hors ligne…), vous pouvez installer vous-même une archive de mise à jour.

1. Vérifiez votre version actuelle dans `system\version.info` (ou dans **PARAMÈTRES SYSTÈME > INFORMATIONS**).
2. Téléchargez la ou les archives nécessaires sur [retrobat.org/repo/win64/stable/archives](https://www.retrobat.org/repo/win64/stable/archives/). Prenez uniquement les fichiers `.zip` (ex. `retrobat-v8.3.0-stable-win64.zip`), sans les renommer.

<div align="left"><figure><img src="../.gitbook/assets/image (411).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Seules les archives d'une nouvelle version **majeure** (le deuxième numéro change : 8.2.0, 8.3.0, 8.4.0…) sont complètes, et elles s'installent par-dessus la version majeure précédente (n'importe quelle 8.2.x pour 8.3.0). Les autres archives (8.3.1, 8.3.1.1…) ne contiennent que les changements depuis la version précédente.

Installez donc les archives **dans l'ordre**, une version majeure après l'autre, puis les mises à jour de la dernière version majeure. Par exemple, pour passer de 8.1.2 à 8.3.1.1 : installez 8.2.0, puis 8.3.0, puis 8.3.1.1.
{% endhint %}

{% hint style="info" %}
La mise à jour est faite par le `es-update.exe` de votre version actuelle. Avant RetroBat 8.4.0, une connexion Internet reste nécessaire, l'archive doit être celle de la version proposée par **LANCER LA MISE À JOUR**, et elle est supprimée après l'installation.
{% endhint %}

3. **Quittez RetroBat.**
4. Ouvrez une invite de commandes (**Windows + R**, tapez `cmd`, **Entrée**) et placez-vous dans le dossier `emulationstation` de RetroBat :

```bat
cd /d C:\RetroBat\emulationstation
```

5. Lancez la mise à jour avec l'archive (chemin entre guillemets) :

```bat
es-update.exe -uselocalzip "C:\Users\<nom>\Downloads\retrobat-v8.3.0-stable-win64.zip"
```

6. Attendez le message **UPDATE DONE**. Si vous avez plusieurs archives à installer, recommencez l'étape 5 avec l'archive suivante.
7. Lancez RetroBat.

{% hint style="info" %}
Le détail de la mise à jour est écrit dans `emulationstation\es-update.log`. Joignez ce fichier si vous demandez de l'aide sur Discord ou GitHub.
{% endhint %}

## Téléchargements

Le groupe **TÉLÉCHARGEMENTS** de **MENU PRINCIPAL > MISES À JOUR & TÉLÉCHARGEMENTS** donne accès à du contenu gratuit.

### Téléchargement de contenu

Sélectionnez **TÉLÉCHARGEMENT DE CONTENU**. Le contenu est classé par onglets :

| Onglet                     | Contenu                                                                                                                                            |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Bezels**                 | [Décorations](decorations-and-bezels.md)                                                                                                           |
| **Games**                  | Jeux gratuits (homebrews, freewares…)                                                                                                              |
| **Intro Videos**           | Vidéos lues au démarrage de RetroBat                                                                                                               |
| **Medias and Tools**       | Médias et outils                                                                                                                                   |
| **Shaders and Megabezels** | Packs de shaders et Mega Bezels pour RetroArch (voir [Décorations](https://wiki.retrobat.org/francais/utilisation-avancee/decorations-and-bezels)) |

<div align="left"><figure><img src="../.gitbook/assets/image (412).png" alt=""><figcaption></figcaption></figure></div>

* **GAUCHE** / **DROITE** : changer d'onglet. **HAUT** / **BAS** : se déplacer dans la liste.
* Appuyez sur **SUD** pour installer le contenu sélectionné. Le contenu installé est marqué d'un ✔.
* Appuyez sur **SUD** sur un contenu installé pour le supprimer.

Le contenu est téléchargé et installé automatiquement dans le bon dossier.

### Thèmes

1. Sélectionnez **THÈMES** pour ouvrir le **TÉLÉCHARGEMENT DE THÈMES**.
2. Sélectionnez un thème et appuyez sur **SUD** pour l'installer. La progression s'affiche en haut à droite.

<div align="left"><figure><img src="../.gitbook/assets/image (413).png" alt=""><figcaption></figcaption></figure></div>

3. Une fois installé, sélectionnez le thème dans **MENU PRINCIPAL > PARAMÈTRES D'AFFICHAGE > PACK DE THÈMES**.

<div align="left"><figure><img src="../.gitbook/assets/image (414).png" alt=""><figcaption></figcaption></figure></div>

### The Bezel Project

**LE BEZEL PROJECT** télécharge des bezels pour chaque jeu d'un système. Voir [Décorations (bezels)](decorations-and-bezels.md).
