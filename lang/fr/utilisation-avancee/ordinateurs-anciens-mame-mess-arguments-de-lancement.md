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

Certains ordinateurs ont besoin d'une commande tapée au démarrage. RetroBat utilise la première source disponible, dans cet ordre :

1. **Fichier autorun :** un fichier du même nom que le jeu avec l'extension `.autorun`, dans le dossier du jeu. La ligne 1 est la commande de démarrage, la ligne 2 (facultative) le délai en secondes (3 par défaut). Pour `3DBRICK.dsk`, un fichier `3DBRICK.autorun` donne : `-autoboot_command "LOADM\"3DBRICK\":EXEC\r" -autoboot_delay 5`

<div align="left"><figure><img src="../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure></div>

2. **Script LUA :** un script nommé d'après la liste logicielle du média (par exemple `bbcb_flop.lua`), dans `bios\mame\autoboot_scripts`. Utilisé quand **OPTIONS AVANCÉES > ÉMULATION > DÉMARRAGE AUTO (TENTATIVE)** est réglé sur **DEPUIS LE SCRIPT LUA**, et par défaut pour BBC Micro, Camputers Lynx, CD-i, CreatiVision, Electron, Odyssey², TVC 64 et VG 5000.
3. **Fichier hash de MAME :** la commande de démarrage indiquée dans la liste logicielle de MAME (`bios\mame\hash`), quand **DÉMARRAGE AUTO (TENTATIVE)** est réglé sur **DEPUIS LE FICHIER HASH**.

<div align="left"><figure><img src="../.gitbook/assets/image (457).png" alt=""><figcaption></figcaption></figure></div>

4. **Crochets du nom de la ROM (BBC Micro) :** avec **DÉMARRAGE AUTO (TENTATIVE)** réglé sur **DEPUIS LES CROCHETS DU NOM DE LA ROM**, le texte entre crochets est utilisé comme fichier à lancer : `Elite [ELITE].ssd` lance `chain"ELITE"`.
5. **Logique interne :** RetroBat applique des commandes intégrées selon le système et le type de média. Par exemple, l'Oric utilise `CLOAD""\n`.

## Type de Joystick

Exemple d'argument en ligne de commande pour l'apple2: `-gameio joy`

Certains ordinateurs peuvent utiliser différents types de contrôleurs. L'option pour activer/changer le type de contrôleur connecté se trouve dans le menu **OPTIONS AVANCÉES DU SYSTÈME > CONTRÔLES** :

<figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Si un type de contrôleur est manquant, vous pouvez demander à la team RetroBat d'ajouter l'option, ou vous pouvez également consulter le guide pour [lignes de commande additionnelles](ordinateurs-anciens-mame-mess-arguments-de-lancement.md#additional-command-line-arguments) ci-dessous.
{% endhint %}

## Autres options

<table><thead><tr><th width="309">Option (OPTIONS AVANCÉES > ÉMULATION)</th><th>Utilité</th></tr></thead><tbody><tr><td><strong>FORCER LA SOFTWARELIST</strong></td><td>Force l'utilisation d'une liste logicielle de MAME (dans <code>bios\mame\hash</code>) au lieu du type de média détecté par l'extension.</td></tr><tr><td><strong>UTILISER LE CHEMIN COMPLET DE LA ROM</strong></td><td>Envoie à MAME le chemin complet du jeu au lieu de son seul nom.</td></tr><tr><td><strong>AJOUTER UN DISQUE UTILISATEUR</strong> (FM Towns)</td><td>Insère une disquette en plus du CD : une disquette vierge, ou une disquette système au nom du jeu (<code>.hdm</code>) placée dans <code>saves\mame\fmtowns</code>.</td></tr></tbody></table>

**Jeux multi-disques (.m3u) :** pour l'Apple II et l'Apple IIGS, les deux premiers disques du fichier `.m3u` sont insérés dans les lecteurs 1 et 2. Pour les autres systèmes, seul un `.m3u` à un disque est pris en charge.

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

{% hint style="info" %}
Les deux fichiers ne s'additionnent pas : quand un jeu a son propre fichier `.commands`, le fichier de la machine est ignoré pour ce jeu. Le fichier de la machine porte le nom du modèle réellement lancé (par exemple `ti99_4a.commands`, ou le modèle choisi dans **MODÈLE DE MACHINE ÉMULÉE**).
{% endhint %}
