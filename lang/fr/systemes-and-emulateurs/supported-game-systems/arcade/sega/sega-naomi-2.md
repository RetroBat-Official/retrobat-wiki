---
description: Sega
---

# Sega NAOMI 2

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/naomi2-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/naomi2.svg" alt=""></picture><figcaption></figcaption></figure></div>

Arcade - Date de création : 2000&#x20;

{% embed url="https://fr.wikipedia.org/wiki/Naomi_2" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>Libretro : flycast</li><li>flycast</li><li>demul</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> naomi2</td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .decomp</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès Rétro</th><th width="200">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-flycast: OUI<br>Flycast: OUI<br>Demul: NON</td><td>NON</td><td>lr-flycast: OUI<br>Flycast: OUI<br>Demul: OUI</td></tr></tbody></table>

## Bios

<table><thead><tr><th width="160.55555555555557">Fichier BIOS</th><th width="155">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>naomi2.zip</td><td><code>\bios\dc</code></td><td>Voir ci-dessous</td></tr></tbody></table>

{% hint style="info" %}
Pour Flycast standalone, les fichiers BIOS doivent être placés dans le dossier `emulators\flycast\data`.
{% endhint %}

### Contenu du fichier BIOS

```
naomi2.zip
- 315-6146.bin "728bfe038ce280872057e365ebfc0fee"
- 315-6215.bin "baf83367044924067e09856ba164aa6f"
- epr-23605.ic27 "6f8ad6e3ab04c8ae1cbcaa652b91cf4e"
- epr-23605a.ic27 "f3f39513484df216d9979f6ae7577942"
- epr-23605b.ic27 "ab046e62c51d67fb89eade2b8d5f6a8d"
- epr-23605c.ic27 "096a5217ff6e6c6cafe65a03336760ab"
- epr-23605c_multi.ic27 "659d579ba9aef5b025d87323044e83f4"
- epr-23607.ic27 "cbe0984d03d73869c23da5a3dd2ce207"
- epr-23607b.ic27 "b624ec7b3b90fdf3be103cdfb1679d1d"
- epr-23607c.ic27 "a9d82db14b823a5a57885bea1a998eb7"
- epr-23608.ic27 "3b1315be24dc8d17f4fa18f3bfc5fe5c"
- epr-23608a.ic27 "0143cf852cb2a8a41f217bc688f62105"
- epr-23608b.ic27 "8b88c1f5a06e9b560e887c3b9f879237"
- epr-23608c.ic27 "b49702e4fadb3b5f9143a3d20afd04b5"
- epr-23609b.ic27 "ecadb008179ca1e6f4fe3fa091ab5df2"
- main_eeprom.bin "edeed38a9795e062a9af28c3eba22040"
- sp5001.bin "14e6bffff0d4dff6a5a547e7c43680ff"
- sp5001-a.bin "689d2228b00fb59781f82af6e8ecdb78"
- sp5001-b.bin "8373a11106c1c2fc21ac839f75ea488f"
- sp5002-a.bin "7eecfb8e8f82b47ffab92a0c5528100e"
- x76f100_eeprom.bin "960ece0dc22a7c5ff81c812a2993e7cc"
```

## Contrôles

{% hint style="danger" %}
En construction.
{% endhint %}

## Informations spécifiques au système

### Fichiers CHD

La plupart des jeux NAOMI2 ne nécessitent qu'une ROM au format zip pour fonctionner, d'autres ont besoin de la présence de fichiers CHD.

Les fichiers CHD doivent être placés dans le dossier des jeux, dans un répertoire dont le nom est identique au fichier .zip.

```
roms\
└─ naomi\
   ├─ vtennis2\
   │  └─ gds-0015a.chd
   └─ vtennis2.zip
```

### Service Menu

Certains jeux disposent d'un menu qui permet de régler des paramètres avancés de la machine tels que les "dip switches", le diagnostic système ou encore des fonctionnalités de réglage des contrôles.

Pour accéder au Service Menu des jeux NAOMI 2, il est nécessaire dans un premier temps d'activer le SERVICE MODE dans les paramètres avancés du système dans RetroBat (mettre OUI):

<div align="left"><figure><img src="https://i.imgur.com/puIdIxb.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/Hxj2lbG.png" alt=""><figcaption></figcaption></figure></div>

Dès lors, l'accès au Service Menu se fait en pressant les boutons  L3 + R3 buttons de contrôleur.
