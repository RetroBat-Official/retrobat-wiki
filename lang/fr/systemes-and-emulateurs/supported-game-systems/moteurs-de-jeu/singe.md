# Singe

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/fb69ee3e5daf0db1c90d85d4a743edf1cc8a1843/art/logos/singe.svg" alt="" width="375"><figcaption></figcaption></figure></div>

Moteur de jeu SINGE

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>hypseus</li><li>singe2</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> singe</td></tr><tr><td><strong>Extensions</strong></td><td>.hypseus .zip</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

| Retrobat                                           | Hypseus    |
| -------------------------------------------------- | ---------- |
| START                                              | START 1    |
| SELECT                                             | COIN 1     |
| D-PAD                                              | DIRECTIONS |
| Left analog stick                                  | DIRECTIONS |
| ![](<../../../.gitbook/assets/image (33).png>)     | SKILL 1    |
| ![](<../../../.gitbook/assets/image (20) (1).png>) | BUTTON 1   |
| ![](<../../../.gitbook/assets/image (7) (1).png>)  | BUTTON 2   |
| ![](<../../../.gitbook/assets/image (35).png>)     | SKILL 2    |
| L1                                                 | SKILL 3    |
| R1                                                 | BUTTON 3   |
| L3                                                 | SERVICE    |
| R3                                                 | TEST       |

## Information spécifique au système

### Ajout de jeux SINGE/SINGE2 (méthode zip)

Il s'agit de la méthode la plus simple pour l'ajout de jeux SINGE, tous les jeux ne sont pas encore disponibles dans ce format.

Télécharger la dernière version zip du jeu ici:\
[https://github.com/DirtBagXon/hypseus\_singe\_data/tree/master/00-zip-roms](https://github.com/DirtBagXon/hypseus_singe_data/tree/master/00-zip-roms)

Créer la structure de fichier suivante:

```
roms\
└─ singe\
   ├─ roms\
   │  └─ timegal.zip
   ├─ vldp\
      └─ timegal\
         ├─ timegal.dat
         ├─ timegal.m2v
         ├─ timegal.ogg
         └─ timegal.txt
```

Placerle fichier zip dans le dossier singe\roms.

Placer les fichiers framework et médias (non fournis) dans le sous-dossier du jeu dans le dossier vldp.

### Ajout de jeux SINGE/SINGE2 (Hypseus)

Placer le dossier du jeu dans le répertoire "**\roms\singe**" et ajouter l'extension .hypseus au dossier.

2 fichiers additionnels doivent être présents dans le dossier de jeu `<jeu>.hypseus`:

* `<jeu>.singe`
* `<jeu>.txt`

Un dossier de jeu SINGE doit avoir une structure similaire à celle-ci:

<div align="left"><figure><img src="https://i.imgur.com/55vdoKB.png" alt=""><figcaption></figcaption></figure></div>

### Structure de fichier pour Hypseus

Pour faciliter le mise en place du système SINGE, il est possible d'utiliser les ressources disponibles sur le Github d'Hypseus.

{% embed url="https://github.com/DirtBagXon/hypseus_singe_data/" %}

Pour commencer, télécharger le contenu du repo ci-dessous,

<figure><img src="https://i.imgur.com/dEGyFs9.gif" alt=""><figcaption></figcaption></figure>

&#x20;extraire le contenu de l'archive dans un répertoire temporaire.

<div align="left"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FexdzL60ZuqPLldz2AYta%2Fuploads%2FRUpdMz97dRcfxyZVG0qp%2Fimage.png?alt=media&#x26;token=3b1ac82f-38a1-4379-ab7e-9d94b7f84e5e" alt=""><figcaption></figcaption></figure></div>

Pour l'exemple, nous allons utiliser le jeu Asterix, qui se situe dans le sous-dossier 00-singe2 de l'archive précédente :

<div align="left"><figure><img src="https://i.imgur.com/cbDJNRN.png" alt=""><figcaption></figcaption></figure></div>

Dans ce dossier de jeu se trouve un fichier texte qui contient des précisions concernant les fichiers manquants pour que le jeu soit fonctionnel, et à quel endroit ils doivent être placés. Dans notre exemple, il faut ajouter le fichier`asterix.m2v` dans le dossier `Video`.

<div align="left"><figure><img src="https://i.imgur.com/iN4Evfi.png" alt=""><figcaption></figcaption></figure></div>

Après avoir ajouté les fichiers nécessaires (cela peut être des fichiers`.m2v`, ou bien des fichiers`.ogg` et`.m2v`), il est nécessaire de renommer le dossier de jeux avec .hypseus à la fin du nom du dossier (dans notre exemple : `Asterix.hypseus`) et déplacer ce dossier dans le répertoire `/roms/singe/` de l'installation RetroBat.

<div align="left"><figure><img src="https://i.imgur.com/f29wlp8.png" alt=""><figcaption></figcaption></figure></div>

### Utiliser des lignes de commandes personnalisées (Hypseus)

Il est possible d'utiliser un fichier de commandes personnalisées pour envoyer des configurations à l'émulateur Hypseus. Pour cela, créer un fichier texte dans le dossier du jeu, et renseigner toutes les commandes voulues à l’intérieur du fichier :

<div align="left"><figure><img src="https://i.imgur.com/AuIQeoE.png" alt=""><figcaption></figcaption></figure></div>

Renommer le fichier avec l'extension .commands, le nom du fichier doit être strictement identique au nom du dossier de jeu (sans l'extension .hypseus).

### Ajout de jeux SINGE2 (émulateur singe2)

L'émulateur singe2 ne fonctionne pas avec le même format de jeux que Hypseus.

Seuls les jeux fournis sur le site web de l'émulateur fonctionnent avec l'émulateur:

{% embed url="https://kangaroopunch.com/view/ShowSoftware?id=7" %}

Télécharger le jeu, ajouter les fichiers requis (vidéo/son), puis renomme le dossier de jeu avec l'extension .singe pour utiliser les jeux avec l'émulateur singe2 depuis RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/0iDxyWG.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/7dDJtAe.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Le nom du dossier doit être parfaitement identique au nom du dossier du jeu téléchargé sur le site de l'émulateur.
{% endhint %}
