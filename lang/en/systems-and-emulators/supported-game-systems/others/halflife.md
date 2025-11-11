---
description: xash3d_fwgs
---

# Half Life

<div align="left"><figure><img src="https://raw.githubusercontent.com/RetroBat-Official/es-theme-carbon/336b127d8e12e7a4f3357e3cc967a15cc58ae766/art/logos/halflife.svg" alt="" width="375"><figcaption></figcaption></figure></div>

Half Life decompilation.

{% embed url="https://github.com/FWGS/xash3d-fwgs" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>xash3d</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> halflife</td></tr><tr><td><strong>File extension</strong></td><td>.game</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

{% hint style="warning" %}
There is no automatic configuration for xash3d, controls can be configured within the game.
{% endhint %}

## Specific system information

### Adding a game

Create a .txt file with any notepad application.

Name the file with the name of the game that must be launched, the name must be equal to the game files subfolder (except for original Half Life).

Save the file with the **.game** extension in the roms\halflife folder.

#### Examples:

For game files:

```
/retrobat/roms/halflife/
                   |── valve/        <== put files from original game "valve" folder
                   |── gearbox/
                   |── cstrike/
                   |── half-life.game
                   |── gearbox.game
                   └── bshift.game
```

{% hint style="info" %}
With first launch, RetroBat will copy the files from xash3d into the retrobat\roms\halflife folder, this is required for the engine to work correctly
{% endhint %}
