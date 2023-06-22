---
description: Fujitsu
---

# FM-TOWNS

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/fmtowns.svg" alt=""><figcaption></figcaption></figure>

</div>

Micro-ordinateur - Durée de vie : 1989 - 1997

{% embed url="https://fr.wikipedia.org/wiki/FM_Towns" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro : mame</li><li>tsugaru</li><li>mame64 : fmtownsux</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> fmtowns</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .d88 .d77 .xdf .cue .iso .game .cd .chd</td><td></td></tr><tr><td><strong>Groupe</strong></td><td>MESS</td><td></td></tr><tr><td><strong>Modèle émulé</strong></td><td>fmtowns, fmtownsux, fmtmarty</td><td></td></tr><tr><td><strong>Softlists</strong></td><td>fmtowns_cd, fmtowns_flop_cracked, fmtowns_flop_misc, fmtowns_flop_orig</td><td></td></tr><tr><td><strong>Types de média</strong></td><td>disquette, cdrom, disque dur, carte mémoire</td><td></td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="209.55555555555557">Fichier BIOS</th><th width="189">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>fmtowns.zip</td><td><code>\bios</code></td><td>Voir ci-dessous</td></tr><tr><td>fmtownsux.zip</td><td><code>\bios</code></td><td>Voir ci-dessous</td></tr><tr><td>FMT_DIC.ROM</td><td><code>\bios\fmtowns</code></td><td>8fa4e553f28cfc0c30a0a1e589799942</td></tr><tr><td>FMT_DOS.ROM</td><td><code>\bios\fmtowns</code></td><td>0585b19930d4a7f4c71bcc8a33746588</td></tr><tr><td>FMT_F20.ROM</td><td><code>\bios\fmtowns</code></td><td>ac0c7021e9bf48ca84b51ab651169a88</td></tr><tr><td>FMT_FNT.ROM</td><td><code>\bios\fmtowns</code></td><td>b91300e55b70227ce98b59c5f02fa8dd</td></tr><tr><td>FMT_SYS.ROM</td><td><code>\bios\fmtowns</code></td><td>86fb6f7280689259f0ca839dd3dd6cde</td></tr></tbody></table>

### Contenu des fichiers

```
fmtowns.zip
- fmt_dic.rom "34847786d7de94b5d1133c956ab1d75d"
- fmt_dos.rom "0585b19930d4a7f4c71bcc8a33746588"
- fmt_fnt.rom "eb44f2093f51eb7159f03e170b13af76"
- fmt_sys.rom "feaf8c5675151e00cfe3ad27673bff29"

fmtownsux.zip
- fmt_dic.rom "8fa4e553f28cfc0c30a0a1e589799942"
- fmt_dos_a.rom "03c8fac9a5f5f5f35fb5de5a5d0d018f"
- fmt_fnt.rom "b91300e55b70227ce98b59c5f02fa8dd"
- fmt_sys_a.rom "90b5e01d42aaa93e8f4503a5e94e120b"
- mytownsux.rom "1a15f6c1b58ec7e5f850118610a787a7"
```

## Contrôles

Utiliser la fonctionnalité [Pad2Key](../../../../controleurs/pad2key.md).

{% hint style="danger" %}
En construction
{% endhint %}

## Information spécifique au système

### Ajouter des jeux pour l'émulateur Tsugaru

Le dossier des jeux (contenant les fichiers **.cue** et .bin) doit être renommé en ajoutant **.game** ou **.cd** à la fin du nom.

Par exemple, le dossier **Super Street Fighter II** doit être renommé:

* `Super Street Fighter II.game`, ou
* `Super Street Fighter II.cd`

<div align="left">

<figure><img src="https://i.imgur.com/wsunOFc.png" alt=""><figcaption></figcaption></figure>

</div>

Les jeux au format \*.iso doivent simplement être placés dans le dossier `roms/fmtowns`.
