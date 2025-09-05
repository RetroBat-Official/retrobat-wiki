# Duke Nukem 3D

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/0ab5d8cd36c673c827b022c2ae53042a38df33da/art/logos/eduke32.svg" alt=""><figcaption></figcaption></figure></div>

Moteur de jeu permettant de jouer à Duke Nukem 3D.

{% embed url="http://www.eduke32.com/" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>eduke32</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> eduke32</td></tr><tr><td><strong>Extensions</strong></td><td>.eduke32</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

{% hint style="warning" %}
Il n'y a pas de configuration automatique des contrôles pour eduke32, les touches peuvent être paramétrées depuis l'émulateur.
{% endhint %}

## Information spécifique au système

### Ajouter un jeu

Créer un fichier .txt avec un éditeur de texte.

Dans le fichier, spécifier les commandes requises pour lancer le jeu, voir les exemples ci-dessous.

Sauvergarder le fichier avec l'extension **.eduke32** dans le dossier roms\eduke32.

#### Examples:

#### Duke Nukem 3D

```
FILE = /duke/DUKE3D.GRP
```

Piur l'organisation suivante:

```
/retrobat/roms/eduke32/duke/
                           |── DUKE3D.GRP
                           └── DUKE.RTS
```

#### **Duke It Out in D.C. (expansion)**

```
FILE  = /duke/DUKE3D.GRP
FILE+ = /duke/DUKEDC.GRP
```

Piur l'organisation suivante:

```
/retrobat/roms/eduke32/duke/
                           ├── DUKE3D.GRP (Atomic Edition) 
                           └── DUKEDC.GRP
```

**Duke Caribbean: Life's a Beach**

```
FILE  = /duke/DUKE3D.GRP
FILE+ = /duke/VACATION.GRP
```

Piur l'organisation suivante:

```
/retrobat/roms/eduke32/duke/
                           ├── DUKE3D.GRP 
                           └── VACATION.GRP
```

#### **Duke: Nuclear Winter (expansion)**

```
FILE  = /duke/DUKE3D.GRP
FILE+ = /duke/NWINTER.GRP
```

Piur l'organisation suivante:

```
/retrobat/roms/eduke32/duke/
                           ├── DUKE3D.GRP
                           └── NWINTER.GRP 
```

#### **Duke Nukem's Penthouse Paradise (expansion)**

```
FILE   = /duke/DUKE3D.GRP
FILE+  = /duke/PENTHOUS.GRP
CON    = /duke/GAME.CON
```

For game files:

```
/retrobat/roms/eduke32/duke/
                          ├── DUKE3D.GRP
                          └── PENTHOUS.GRP
                          └── GAME.CON (from Penthouse Paradise)
```

<details>

<summary>Valeurs possibles</summary>

* FILE (equivalent to `-gamegrp`)
* FILE+ (equivalent to `-g`)
* CON (equivalent to `-x`)
* CON+ (equivalent to `-mx`)
* DIR (equivalent to `-j`)
* DEF (equivalent to `-h`)
* DEF+ (equivalent to `-mh`)
* MAP (equivalent to `-map`)

</details>

### Packs HD

Pour utiliser les extensions d'eduke32 comme les packs de textures HD ou les packs de sons, il faut placer les fichiers additionnels dans le répertoire `\roms\eduke32\autoload`, puis depuis le menu RetroBat activer la fonctionnalité de chargement automatique :

<div align="left"><figure><img src="https://i.imgur.com/ALBNp6e.png" alt=""><figcaption></figcaption></figure></div>

#### Exemple :

<div align="left"><figure><img src="https://i.imgur.com/MvPC3Qb.png" alt=""><figcaption></figcaption></figure></div>

