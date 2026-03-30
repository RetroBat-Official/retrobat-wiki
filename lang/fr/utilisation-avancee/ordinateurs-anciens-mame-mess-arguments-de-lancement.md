# Ordinateurs anciens - MAME/MESS - arguments de lancement

MAME (MESS) permet d'émuler une grande variété d'anciens ordinateurs. Ces ordinateurs nécessitent souvent l'utilisation de lignes de commande spécifiques pour connecter des périphériques, modifier la taille de la mémoire vive, définir les commandes de démarrage automatique, etc.

Bien que RetroBat intègre plusieurs options directement accessibles depuis son interface, nous avons laissé aux utilisateurs la possibilité d'ajouter leurs propres lignes de commande pour des systèmes ou des jeux spécifiques.

À titre d'exemple, RetroBat peut lancer le système TI99 dans MAME avec les arguments suivants :

<mark style="background-color:$warning;">`ti99_4a`</mark>` ``-ioport peb -ioport:peb:slot2 32kmem -ioport:peb:slot4 speechadapter -ioport speechsyn -cart alpiner`

## Modèles d'ordinateurs

La première commande lancée correspond au modèle d'ordinateur (<mark style="background-color:$warning;">`ti99_4a`</mark>)

Quand un ordinateur existe en plusieurs modèles (par exemple le Camputers Lynx, avec les modèles 48K, 96K ou 128K), RetroBat propose l'option permettant de sélectionner le modèle d'ordinateur à émuler. L'option se trouve dans le menu **OPTIONS AVANCÉES DU SYSTÈME > ÉMULATION** :

<figure><img src="../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Il est nécessaire d'avoir les BIOS spécifiques au modèle émulé dans le répertoire bios\\.
{% endhint %}

## Ports d'extension

La seconde partie de la commande correspond a des emplacements additionnels ou des accessoires qui peuvent être activés pour un ordinateur (`-ioport peb -ioport:peb:slot2 32kmem -ioport:peb:slot4 speechadapter -ioport speechsyn`)

RetroBat a sélectionné quelques accessoires et emplacements importants pour quelques modèles d'ordinateurs, ceux-ci sont accessibles depuis le menu **OPTIONS AVANCÉES > SLOTS D'EXTENSION** :

<figure><img src="../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Si une extension ou un accessoire est manquant, vous pouvez demander à la team RetroBat d'ajouter l'option, vous pouvez également consulter le guide pour [lignes de commande additionnelles](ordinateurs-anciens-mame-mess-arguments-de-lancement.md#additional-command-line-arguments) ci-dessous.
{% endhint %}

## Type de Média

Les anciens ordinateurs peuvent accepter différents types de médias (disquettes, cartouches, rom...). Cela se traduit dans l'exemple par la dernière partie de la ligne de commande, avec l'argument (`-cart`)

RetroBat peut détecter automatiquement le type de media en se basant sur l'extension du fichier de jeu, toutefois il est possible de forcer le type de média. L'option est disponible dans le menu **OPTIONS AVANCÉES DU SYSTÈME > ÉMULATION** :

<figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

## Commande de démarrage automatique et délai

Certains ordinateurs nécessitent certaines commandes spécifiques au démarrage pour lancer/charger un jeu.

RetroBat a une logique spécifique pour activer des commandes de démarrage automatique, la logique est détaillée ci-après, par ordre de priorité:

#### 1) Vérification de l'existence d'un fichier autorun

RetroBat vérifie si un fichier, nommé à l'identique de la rom du jeu, possédant l'extension .autorun, existe.

Si c'est le cas, RetroBat lira ce fichier, et ajoutera la 1ère ligne en tant que commande de démarrage automatique, et la seconde ligne (si elle existe) comme délai de démarrage automatique :

<div align="left"><figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure></div>

Dans l'exemple ci-dessus, le fichier est effectif pour le fichier de jeu 3DBRICK.dsk, et génère la ligne de commande suivante :&#x20;

```
-autoboot_command "LOADM\"3DBRICK\":EXEC\r" -autoboot_delay 5
```

#### 2) Vérification dans le fichier de hash MAME

MAME contient de fichiers appelé softlists, situés dans le dossier `\bios\mame\hash` de votre installation RetroBat. Certains de ces fichiers contiennent des commandes spécifiques pour lancer certains jeux.

Si l'option "**OPTIONS AVANCÉES DU SYSTÈME > ÉMULATION > DÉMARRAGE AUTO**" est activée dans le menu, RetroBat tente de déterminer la commande de démarrage en cherchant dans le fichier softlist correspondant :

<figure><img src="../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

#### 3) Logique interne

RetroBat contient également une logique interne, basée sur le système/type de média, pour démarrer automatiquement les jeux, par exemple la commande `CLOAD""\n` pour les ordinateurs Oric est appliquée automatiquement.

## Type de Joystick

Exemple d'argument en ligne de commande pour l'apple2: `-gameio joy`

Certains ordinateurs peuvent utiliser différents types de contrôleurs. L'option pour activer/changer le type de contrôleur connecté se trouve dans le menu **OPTIONS AVANCÉES DU SYSTÈME > CONTRÔLES** :

<figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Si un type de contrôleur est manquant, vous pouvez demander à la team RetroBat d'ajouter l'option, ou vous pouvez également consulter le guide pour [lignes de commande additionnelles](ordinateurs-anciens-mame-mess-arguments-de-lancement.md#additional-command-line-arguments) ci-dessous.
{% endhint %}

## Arguments de ligne de commande additionnelles

Il est également possible d'ajouter des arguments personnalisés, en complément des arguments proposés par RetroBat.

Les arguments peuvent être ajoutés aussi bien pour un type de machine / modèle d'ordinateur, que pour un jeu spécifique.

Le fichier détaillé ci-dessous devra être placés dans le même répertoire que le fichier de jeu lancé.

### Ajout de ligne de commande pour un jeu spécifique

RetroBat vérifie si un fichier, possédant le même nom que le fichier du jeu, mais avec l'extension .commands, existe.

Si c'est le cas, RetroBat ajoute chaque ligne du fichier comme un argument additionnel lors du lancement du jeu :

<div align="left"><figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure></div>

Dans cet exemple, pour le fichier **alpiner.zip,** les arguments suivants sont ajoutés :&#x20;

```
-cart "C:\retrobat\bios\ti99\Extended Basic v110.rpk"
```

### Ajout de ligne de commande pour un ordinateur / une machine

RetroBat vérifie si un fichier, possédant le même nom que le modèle d'ordinateur émulé, et avec l'extension .commands, existe.

Si c'est le cas, RetroBat ajoute chaque ligne du fichier comme un argument additionnel lors du lancement d'un jeu pour cette machine :

<div align="left"><figure><img src="../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure></div>

Dans cet exemple, ce fichier permet d'ajouter la ligne de commande suivante pour chaque jeu lancé pour la ti99\_4a :

```
-cart "C:\retrobat\bios\ti99\Extended Basic v110.rpk"
```
