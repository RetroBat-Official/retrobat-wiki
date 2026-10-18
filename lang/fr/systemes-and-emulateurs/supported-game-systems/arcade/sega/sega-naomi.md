---
description: Sega
---

# Sega NAOMI

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/naomi-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/naomi.svg" alt=""></picture><figcaption></figcaption></figure></div>

Arcade - Date de création : 1998&#x20;

{% embed url="https://fr.wikipedia.org/wiki/Naomi_(syst%C3%A8me_d'arcade)" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>Libretro : flycast</li><li>flycast</li><li>demul</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> naomi</td></tr><tr><td><strong>Extensions</strong></td><td>.bin .dat .lst .zip .7z .decomp</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès Rétro</th><th width="200">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-flycast: OUI<br>Flycast: OUI<br>Demul: NON</td><td>NON</td><td>lr-flycast: OUI<br>Flycast: OUI<br>Demul: OUI</td></tr></tbody></table>

## Bios

<table><thead><tr><th width="160.55555555555557">Fichier BIOS</th><th width="155">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>naomi.zip</td><td><code>\bios\dc</code></td><td>eb4099aeb42ef089cfe94f8fe95e51f6</td></tr></tbody></table>

{% hint style="info" %}
Pour Flycast standalone, les fichiers BIOS doivent être placés dans le dossier `emulators\flycast\data`.
{% endhint %}

## Contrôles

{% hint style="danger" %}
En construction.
{% endhint %}

## Informations spécifiques au système

### Fichiers CHD

La plupart des jeux NAOMI ne nécessitent qu'une ROM au format zip pour fonctionner, d'autres ont besoin de la présence de fichiers CHD.

Les fichiers CHD doivent être placés dans le dossier des jeux, dans un répertoire dont le nom est identique au fichier .zip.

```
roms\
└─ naomi\
   ├─ ikaruga\
   │  └─ gdl-0010.chd
   └─ ikaruga.zip
```

### Service Menu

Certains jeux disposent d'un menu qui permet de régler des paramètres avancés de la machine tels que les "dip switches", le diagnostic système ou encore des fonctionnalités de réglage des contrôles.

Pour accéder au Service Menu des jeux NAOMI, il est nécessaire dans un premier temps d'activer le SERVICE MODE dans les paramètres avancés du système dans RetroBat (mettre OUI):

<div align="left"><figure><img src="https://i.imgur.com/puIdIxb.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/Hxj2lbG.png" alt=""><figcaption></figcaption></figure></div>

Dès lors, l'accès au Service Menu se fait en pressant les boutons  L3 + R3 buttons de contrôleur.
