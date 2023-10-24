---
description: NEC
---

# NEC PC-8800

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/pc88-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/pc88.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Micro-ordinateur - Date de sortie : 1981

{% embed url="https://fr.wikipedia.org/wiki/PC-88" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro : quasi88</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> pc88</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.d88 .u88 .m3u</td><td></td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="193">Fichier BIOS</th><th width="182.03610108303252">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>N88.ROM</td><td><code>\bios\quasi88</code></td><td>4f984e04a99d56c4cfe36115415d6eb8</td></tr><tr><td>N88SUB.ROM</td><td><code>\bios\quasi88</code></td><td>793f86784e5608352a5d7f03f03e0858</td></tr><tr><td>N88N.ROM</td><td><code>\bios\quasi88</code></td><td>2ff07b8769367321128e03924af668a0</td></tr><tr><td>N88EXT0.ROM</td><td><code>\bios\quasi88</code></td><td>d675a2ca186c6efcd6277b835de4c7e5</td></tr><tr><td>N88EXT1.ROM</td><td><code>\bios\quasi88</code></td><td>e844534dfe5744b381444dbe61ef1b66</td></tr><tr><td>N88EXT2.ROM</td><td><code>\bios\quasi88</code></td><td>6548fa45061274dee1ea8ae1e9e93910</td></tr><tr><td>N88EXT3.ROM</td><td><code>\bios\quasi88</code></td><td>fc4b76a402ba501e6ba6de4b3e8b4273</td></tr></tbody></table>

## Contrôles

Utiliser la fonctionnalité [Pad2Key](../../../../controleurs/pad2key.md).

{% hint style="danger" %}
En construction.
{% endhint %}

## Information spécifique au système

### Jeux Multi-disques

Utiliser un fichier m3u pour les jeux multi-disques.&#x20;

Créer un fichier .txt et le sauvegarder avec le nom `<jeu>.m3u`. Renseigner dans le fichier le nom des fichiers des ROMs de jeu, un fichier par ligne, dans l'ordre des disques.&#x20;

Ci-dessous un exemple de fichier m3u:

`Ys II.m3u`

```
# Ys II (Falcom)
Ys II (Program disk).d88
Ys II (Disk A).d88
Ys II (Disk B).d88
Ys II (User disk).d88
```

Ensuite, lorsque le prompt demandant le changement de disque apparaît dans le jeu , appuyez sur la gâchette L pour le lecteur 1 et R pour le lecteur 2.&#x20;

En maintenant la gâchette, tout en appuyant sur les directions gauche et droite du D-pad, choisir chacun des volumes du lecteur. Lorsque la gâchette est relâchée, le disque choisi est inséré.
