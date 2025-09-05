---
description: eduke32
---

# Duke Nukem 3D



<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/0ab5d8cd36c673c827b022c2ae53042a38df33da/art/logos/eduke32.svg" alt=""><figcaption></figcaption></figure></div>

Game engine to play Duke Nukem 3D game.

{% embed url="http://www.eduke32.com/" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>eduke32</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> eduke32</td></tr><tr><td><strong>File extension</strong></td><td>.eduke32</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

{% hint style="warning" %}
There is no automatic configuration for eduke32, controls can be configured within the emulator.
{% endhint %}

## Specific system information

### Adding a game

Create a .txt file with any notepad application.

Inside the file, enter the commands as per the guide below, based on the command line to send to the emulator.

Save the file with the **.eduke32** extension in the roms\eduke32 folder.

#### Examples:

#### Duke Nukem 3D

```
FILE = /duke/DUKE3D.GRP
```

For game files:

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

For game files:

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

For game files:

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

For game files:

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

<summary>List of value for commands</summary>

* FILE (equivalent to `-gamegrp`)
* FILE+ (equivalent to `-g`)
* CON (equivalent to `-x`)
* CON+ (equivalent to `-mx`)
* DIR (equivalent to `-j`)
* DEF (equivalent to `-h`)
* DEF+ (equivalent to `-mh`)
* MAP (equivalent to `-map`)

</details>



### HD packs

In order to use eduke32 addons like HD texture pack or sound pack, place the addon files within the `\roms\eduke32\autoload` folder and activate the autoload feature in RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/ALBNp6e.png" alt=""><figcaption></figcaption></figure></div>

#### Example:

<div align="left"><figure><img src="https://i.imgur.com/MvPC3Qb.png" alt=""><figcaption></figcaption></figure></div>

