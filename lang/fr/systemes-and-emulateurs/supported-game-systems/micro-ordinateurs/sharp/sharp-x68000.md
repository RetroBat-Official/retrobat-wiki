---
description: Sharp
---

# Sharp X68000

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/x68000.svg" alt=""><figcaption></figcaption></figure>

</div>

Micro-ordinateur - Durée de vie : 1987 - 1993

{% embed url="https://fr.wikipedia.org/wiki/Sharp_X68000" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>Libretro : px68k</li><li>xm6pro</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> x68000</td></tr><tr><td><strong>Extensions</strong></td><td>.dim .img .d88 .88d .hdm .dup .2hd .xdf .hdf .cmd .m3u .zip .7z</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès Rétro</th><th width="200">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-px68k : NON<br>XM6Pro : NON</td><td>lr-px68k : OUI<br>XM6Pro : NON</td><td>lr-px68k : OUI<br>XM6Pro : NON</td></tr></tbody></table>

## Bios

<table><thead><tr><th width="224">Fichier BIOS</th><th width="169">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>iplrom.dat</td><td><code>\bios\keropi</code></td><td>7fd4caabac1d9169e289f0f7bbf71d8e</td></tr><tr><td>cgrom.dat</td><td><code>\bios\keropi</code></td><td>cb0a5cfcf7247a7eab74bb2716260269</td></tr></tbody></table>

## Contrôles

Utiliser la fonctionnalité [Pad2Key](../../../../controleurs/pad2key.md).

| Retrobat                                          | X68000    |
| ------------------------------------------------- | --------- |
| START                                             | JOY\_TRG6 |
| SELECT                                            | JOY\_TRG7 |
| D-PAD                                             | D-PAD     |
| Stick analogique gauche                           | D-PAD     |
| Stick analogique droit                            |           |
| ![](<../../../../.gitbook/assets/image (32).png>) | JOY\_TRG3 |
| ![](<../../../../.gitbook/assets/image (19).png>) | JOY\_TRG2 |
| ![](<../../../../.gitbook/assets/image (6).png>)  | JOY\_TRG1 |
| ![](<../../../../.gitbook/assets/image (34).png>) | JOY\_TRG4 |
| L1                                                | JOY\_TRG5 |
| R1                                                | JOY\_TRG8 |
| L2                                                | Menu      |
| R2                                                |           |

## Information spécifique au système

### Jeux multi-disques

Utiliser un fichier m3u pour les jeux multi-disques.

Créer un fichier .txt et le sauvegarder avec le nom `<game>.m3u`.&#x20;

Renseigner dans le fichier le nom des fichiers des ROMs, un fichier par ligne, dans l'ordre des disques.&#x20;

Ci-dessous un exemple de fichier m3u:

`foo.m3u`

```
foo (Disk 1).dim
foo (Disk 2).dim
foo (Disk 3).dim
```
