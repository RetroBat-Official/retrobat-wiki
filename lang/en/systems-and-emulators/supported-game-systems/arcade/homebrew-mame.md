---
description: MAME Team
---

# HomeBrew MAME

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/hbmame.svg" alt=""><figcaption></figcaption></figure>

</div>

**HBMAME** (HomeBrew MAME) is a derivative of MAME 0.245, and contains various hacks and homebrews.

{% embed url="https://arcade.mameworld.info/hbmame/index.html" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>Libretro: mame</li><li>Libretro: mame2003_plus</li><li>Libretro: mame2003</li><li>Libretro: mame2003_midway</li><li>Libretro: mame2016</li><li>mame64</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> hbmame</td></tr><tr><td><strong>File extension</strong></td><td>.zip .7z</td></tr></tbody></table>

## Bios Information

Refer to the [MAME page](mame.md#bios-information), HBMAME requires the same bioses as MAME 0.245.

## Controls

[Refer to the MAME page.](mame.md#controls)

## Specific system information

### Adding HBMame games to RetroBat

Most Romsets for HBMame come in a "merged" presentation, meaning that the rom will contain the main game and the hack inside of the same zip file.

In order for RetroBat to see the Hack version, the rom will have to be "un-merged", here is an example for the "Arrange Ver. 1.1" hack for DoDonPachi:

<div align="left">

<figure><img src="https://i.imgur.com/5Zh2T6D.png" alt=""><figcaption></figcaption></figure>

</div>

#### **Step 1: checking the rom**

Check that the rom you have is correct, this can be achieved by downloading the official HBMameUI software [here](https://hbmame.1emulation.com/), placing the rom in the rom folder of the downloaded HBMame and auditing the set.

#### **Step 2: un-merging the rom**

Place your rom in the `\roms\hbmame` folder of your RetroBat installation.

Open the rom archive and extract the hack you want to launch from RetroBat.

Here for example we will extract ddonpacha from the archive:

<div align="left">

<figure><img src="https://i.imgur.com/uPE1ZDY.png" alt=""><figcaption></figcaption></figure>

</div>

Now, go inside the extracted ddonpacha folder and zip the content, the zip name must be `ddonpacha.zip` (the official hack name):

<div align="left">

<figure><img src="https://i.imgur.com/QiLS3QV.png" alt=""><figcaption></figcaption></figure>

</div>

The content of the zip should look as follows:

<div align="left">

<figure><img src="https://i.imgur.com/dmRocxJ.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="danger" %}
When zipping, ensure there is no ddonpacha subdirectory before the rom files !
{% endhint %}

#### **Step 3: run the game**

Now both roms will appear in RetroBat : the main one and the hack

<div align="left">

<figure><img src="https://i.imgur.com/hVLvQ5N.png" alt=""><figcaption></figcaption></figure>

</div>

And you will be able to run the hack rom with the emulators / cores provided in RetroBat:

<div align="left">

<figure><img src="https://i.imgur.com/ERVSQi8.png" alt=""><figcaption></figcaption></figure>

</div>

### ROM set versions&#x20;

Current ROM set : 0.245

### CHD or IMG files

Refer to the [Arcade Guide section](../../arcade-guide.md#chd-or-img-files) about CHD.

### **Sample files**

Refer to the [Arcade Guide "sample file" section](../../arcade-guide.md#samples).
