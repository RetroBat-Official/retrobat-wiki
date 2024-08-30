---
description: Sony
---

# PlayStation Vita

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/psvita-w.svg" media="(prefers-color-scheme: dark)"><img src="https://i.imgur.com/as0rgjr.png" alt=""></picture><figcaption></figcaption></figure>

</div>

Console de jeu portable - Durée de vie : 2011 - 2019

{% embed url="https://fr.wikipedia.org/wiki/PlayStation_Vita" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>vita3k</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> psvita</td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .psvita .vpk</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>NON</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="182">Fichier BIOS</th><th width="198.03610108303252">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>PSP2UPDAT.PUP</td><td><code>install in emukator</code></td><td>8B5F60B56C3DA8365B973DBA570C53A5</td></tr><tr><td>PSVUPDAT.PUP</td><td><code>install in emukator</code></td><td>F2C7B12FE85496EC88A0391B514D6E3B</td></tr></tbody></table>

## Contrôles

Vita3K reconnaît automatiquement le contrôleur connecté, aucune configuration n'est requise.

## Information spécifique au système

### Emplacement des fichiers

<table><thead><tr><th width="254">Fichier(s)</th><th>Chemin (relatif au dossier RetroBat)</th></tr></thead><tbody><tr><td>pref-path</td><td>saves\psvita\vita3k*<br><br>*Le dossier est défini par l'utilisateur lors de l'installation, RetroBat ne le modifie pas.</td></tr></tbody></table>

### Installation & premier démarrage

Utiliser le menu RetroBat pour télécharger Vita3k ou télécharger la dernière version disponible de l'émulateur sur le site web Vita3k : [https://vita3k.org/#download](https://vita3k.org/#download)

{% hint style="warning" %}
Ne démarrez pas de jeu avant d'avoir installer et configurer vita3k depuis le menu retrobat, cette étape est nécessaire pour initialiser l'utilisateur de la PSVita et pour installer les firmwares.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/k9c9vpN.png" alt=""><figcaption></figcaption></figure>

</div>

Au premier démarrage, l'émulateur a besoin d'être paramétré, la première étape est de choisir la langue :

<div align="left">

<figure><img src="https://i.imgur.com/8MeZjaA.png" alt=""><figcaption></figcaption></figure>

</div>

**Étape importante, définir le "pref-path" : il s'agit de l'emplacement dans lequel les jeux seront installés.**&#x20;

L'emplacement sélectionné à cette étape ne sera pas remplacé ou modifié par RetroBat.

<div align="left">

<figure><img src="https://i.imgur.com/bKZh9Ap.png" alt=""><figcaption></figcaption></figure>

</div>

Télécharger aussi bien le _Firmware_ et le _Font Package_ depuis le site de Sony et installer les à l'aide du bouton **INSTALL FIRMWARE FILE** :

<div align="left">

<figure><img src="https://i.imgur.com/7kfwreX.png" alt=""><figcaption></figcaption></figure>

</div>

Le statut de l'installation changera (V)

<div align="left">

<figure><img src="https://i.imgur.com/JmQbJpH.png" alt=""><figcaption></figcaption></figure>

</div>

Cliquer sur le bouton "SUIVANT" jusqu'à la fin du paramétrage :

<div align="left">

<figure><img src="https://i.imgur.com/SS4fC7b.png" alt=""><figcaption></figcaption></figure>

</div>

FÉLICITATIONS : L'émulateur Vita3k a été initialisé avec succès :

<div align="left">

<figure><img src="https://i.imgur.com/y9Abjp5.png" alt=""><figcaption></figcaption></figure>

</div>

### Ajouter les jeux

Les jeux PS Vita doivent dans un premier temps être installés via l'émulateur, un guide détaillé est disponible pour cela sur le site Vita3K : [https://vita3k.org/quickstart.html](https://vita3k.org/quickstart.html)

Vita3K supporte actuellement les fichiers .pkg, NoNpDrm, FAGDec, ou les jeux décryptés manuellement.&#x20;

Le jeu doit être au format .zip ou .vpk pour être installé dans l'émulateur, il est également possible de faire un glisser - déposer du répertoire de jeu dans le dossier `emulators\vita3k\ux0\app` (cette méthode n'est pas valable pour les dumps NoNpDrm ni les fichier .pkg).

2 cas de figures se présentent :

1. Le jeu est déjà installé dans Vita3k
2. Le jeu est dans votre répertoire `roms\psvita` est n'est pas encore installé dans Vita3k

{% hint style="info" %}
Les jeux sont installés dans le dossier`\ux0\app` de l'emplacement "pref-path" défini lors de la configuration initiale de l'émulateur.
{% endhint %}

#### Cas 1 : Le jeu est déjà installé dans Vita3k

Créer un fichier .m3u portant le nom du jeu dans le répertoire`\roms\psvita` de votre installation RetroBat :

<div align="left">

<figure><img src="https://i.imgur.com/tfILs19.png" alt=""><figcaption></figcaption></figure>

</div>

A l'intérieur du fichier, renseigner l'**ID de jeu** et sauvegarder :

<div align="left">

<figure><img src="https://i.imgur.com/Fs8a98E.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
L'ID de jeu peut être trouvé en lançant directement l'émulateur Vita3k.
{% endhint %}

<figure><img src="https://i.imgur.com/XFt1Iop.png" alt=""><figcaption></figcaption></figure>

#### Cas 2 : Le jeu se trouve dans votre répertoire roms et n'est pas encore installé dans l'émulateur

RetroBat prend en charge automatiquement l'installation du jeu lorsque vous le lancez pour la 1ère fois, sous réserve que le jeu soit dans le bon format.

2 formats sont acceptés et permettent l'installation automatique :

* dossier de jeu
* package .vpk

{% hint style="warning" %}
Il est obligatoire que le nom de votre répertoire .psvita ou le nom du fichier .vpk contienne l'ID de jeu entre crochets, comme sur l'illustration ci-dessous, sinon l'installation ne fonctionne pas.
{% endhint %}

Si vous utilisez un jeu au format "dossier", le répertoire doit être renommé avec ".psvita" à la fin. Il est également nécessaire de s'assurer qu'un fichier eboot.bin se trouve à l'intérieur du répertoire. Voici un exemple d'une structure de fichier correcte :

<div align="left">

<figure><img src="https://i.imgur.com/Anjm21x.png" alt=""><figcaption></figcaption></figure>

</div>

Si vous utilisez un fichier .vpk, il faut s'assurer que le fichier soit correctement nommé, avec l'ID de jeu entre crochets :

```
Street fighter [PCSE00005].vpk
```

Lors du premier lancement du jeu au format .vpk, Retrobat l'installera automatiquement dans l'émulateur. Il faudra patienter jusqu'à ce que l'opération s'achève (cela peut prendre un certain temps) :

<div align="left">

<figure><img src="https://i.imgur.com/bYSh81f.png" alt=""><figcaption></figcaption></figure>

</div>

Une fois l'installation effectuée, le prochain démarrage sera plus rapide.
