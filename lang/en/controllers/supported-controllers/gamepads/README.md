# 🎮 Gamepads

Almost every gamepad recognized by Windows works with RetroBat.

* **Wired gamepads** are plug-and-play: connect them, then configure them in RetroBat if needed.
* **Bluetooth gamepads** must first be paired in the Windows Bluetooth settings.

When a new gamepad is detected, RetroBat asks you to configure it (see [Controllers configuration](../../controller-configuration.md)). Most common gamepads are configured automatically.

{% hint style="info" %}
To check that Windows detects your gamepad and all its buttons, test it on [gamepad-tester.com](https://gamepad-tester.com/).
{% endhint %}

## XInput or DirectInput?

Windows uses two kinds of gamepads:

<table><thead><tr><th width="137">Type</th><th width="305.5">Gamepads</th><th>In RetroBat</th></tr></thead><tbody><tr><td><strong>XInput</strong></td><td>Xbox gamepads and gamepads in "Xbox / X-input" mode</td><td>✅ Recommended: recognized the same way by all emulators</td></tr><tr><td><strong>DirectInput / SDL</strong></td><td>PlayStation, Switch Pro, generic gamepads, 8BitDo in Switch or D-input mode…</td><td>Works, but some older emulators may need extra configuration</td></tr></tbody></table>

{% hint style="warning" %}
Windows only manages **4 XInput gamepads** at the same time. Beyond 4 players, use gamepads in another mode.
{% endhint %}

## Xbox gamepads (and any XInput gamepad)

![](<../../../.gitbook/assets/image (299).png>)![](<../../../.gitbook/assets/image (300).png>)

Xbox gamepads are the most compatible with RetroBat.

<table><thead><tr><th width="335.25">Model</th><th>Connection</th></tr></thead><tbody><tr><td>Xbox Series X|S, Xbox One S, Xbox Elite Series 2</td><td>USB, Bluetooth or Xbox Wireless Adapter</td></tr><tr><td>Xbox One (first model, without Bluetooth)</td><td>USB or Xbox Wireless Adapter</td></tr><tr><td>Xbox 360 wired</td><td>USB</td></tr><tr><td>Xbox 360 wireless</td><td>Xbox 360 Wireless Receiver for Windows (the Xbox One adapter does not work)</td></tr></tbody></table>

## 8BitDo gamepads

<div align="left"><figure><img src="../../../.gitbook/assets/image (301).png" alt=""><figcaption></figcaption></figure></div>

8BitDo gamepads work very well with RetroBat. Most models offer several **modes**, which change how Windows sees the gamepad.

{% hint style="success" %}
**Which mode for RetroBat?**

* **X-input mode**: recommended. The gamepad is seen as an Xbox gamepad and works the same way in all emulators.
* **Switch mode**: only if you need **motion controls** (gyroscope) for Wii U or Switch games. X-input mode does not support motion controls.
{% endhint %}

### Changing the mode

<table><thead><tr><th width="326">Model</th><th width="149.75">X-input</th><th width="133.75">Switch</th><th width="129.75">D-input</th></tr></thead><tbody><tr><td>Bluetooth models with buttons (SN30 Pro, SN30 Pro+, Lite, M30…): <strong>turn the gamepad off, then turn it on with</strong></td><td><strong>START + X</strong></td><td><strong>START + Y</strong></td><td><strong>START + B</strong></td></tr><tr><td>Models with a mode switch on the back (Pro 2…): <strong>set the switch to</strong></td><td><strong>X</strong></td><td><strong>S</strong></td><td><strong>D</strong></td></tr><tr><td>Wired models and USB connection: <strong>hold the button while plugging in the cable</strong></td><td><strong>X</strong></td><td><strong>START + Y</strong></td><td><strong>B</strong></td></tr><tr><td>Models with a 2.4 GHz USB dongle (Ultimate 2.4G, Ultimate 2C…)</td><td>Use the dongle (X-input by default)</td><td>—</td><td>—</td></tr></tbody></table>

To turn a gamepad off, hold **START** for about 3 seconds (8 seconds on some models).

The LEDs show the current mode on most models: for example on the Pro 2, LED 2 blinking = X-input, LED 1 = D-input, LED 3 = macOS, rotating LEDs = Switch or pairing.

{% hint style="warning" %}
**After changing the mode of a Bluetooth gamepad**, Windows sees it as a new device:

1. Remove the gamepad from the Windows Bluetooth settings.
2. Turn the gamepad on in the new mode, then put it in pairing mode (hold the **pair** button for 3 seconds).
3. Pair it again in Windows.
4. If RetroBat asks you to, configure the gamepad again (a gamepad in another mode is a different gamepad for RetroBat).
{% endhint %}

{% hint style="info" %}
* The available modes depend on the model: check the manual of your gamepad.
* Keep your gamepad up to date with the **8BitDo Ultimate Software** or the **8BitDo Updater** (Windows), available on the [8BitDo support website](https://support.8bitdo.com/).
{% endhint %}

## PlayStation gamepads

### DualSense (PS5) and DualShock 4 (PS4)

![](<../../../.gitbook/assets/image (302).png>)![](<../../../.gitbook/assets/image (303).png>)

DualSense and DualShock 4 work over USB and Bluetooth, and support motion controls.

By default, RetroBat uses them in **standard mode**, which works with all emulators. The **PS4/PS5 ENHANCED** option (**MAIN MENU** > **GAME SETTINGS** > **CONTROLS** > **SPECIAL CONTROLLERS**, or per system) enables rumble and motion in emulators that support it (DuckStation, Switch emulators…).

{% hint style="warning" %}
Once the enhanced mode has been used, the gamepad stays in this mode until it is turned off: emulators using DirectInput may then no longer detect it. **Turn the gamepad off and on again** if an emulator does not respond, or keep the option disabled.
{% endhint %}

### DualShock 3 (PS3)

<div align="left"><figure><img src="../../../.gitbook/assets/image (304).png" alt="" width="188"><figcaption></figcaption></figure></div>

The DualShock 3 is not supported natively by Windows: install a driver such as [DsHidMini](https://github.com/nefarius/DsHidMini) and use its **XInput** mode for the best compatibility.

## Nintendo gamepads

### Switch Pro Controller

![](<../../../.gitbook/assets/image (18).png>)

The Switch Pro Controller works over USB and Bluetooth. It is ideal for Wii U and Switch emulators (Cemu, Eden, Citron, Ryujinx…), which support its motion controls.

{% hint style="warning" %}
Nintendo button names are swapped compared to Xbox (A is on the right, B at the bottom). RetroBat uses the **position** of the buttons: the South button (B on a Nintendo gamepad) always validates.
{% endhint %}

### Joy-Cons

<div align="left"><figure><img src="../../../.gitbook/assets/image (305).png" alt="" width="188"><figcaption></figcaption></figure></div>

Joy-Cons connected together are seen as **a single gamepad** by RetroBat.

## Handheld PCs

<table><thead><tr><th width="292.75">Device</th><th>Built-in controls</th></tr></thead><tbody><tr><td>ASUS ROG Ally, Lenovo Legion Go, MSI Claw…</td><td>Seen as an Xbox (XInput) gamepad: they work directly</td></tr><tr><td>Steam Deck (with Windows)</td><td>Needs Steam (Steam Input) or a driver to be seen as an Xbox gamepad. Mouse and gun settings: <strong>CONTROLLER SETTINGS</strong> > <strong>STEAMDECK MOUSE/GUN SETTINGS</strong></td></tr></tbody></table>

## Common issues

<table><thead><tr><th width="242.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The gamepad appears twice</td><td>A tool creates a virtual Xbox gamepad in addition to the real one (DS4Windows, DsHidMini, Steam Input…). Hide the real gamepad (for example with HidHide), or close the tool.</td></tr><tr><td>Steam Input changes the controls</td><td>Close Steam, or disable Steam Input for this gamepad, before starting RetroBat.</td></tr><tr><td>The players are in the wrong order</td><td>Choose the gamepad of each player in <strong>CONTROLLER SETTINGS</strong> (see <a href="../../controller-configuration.md">Controllers configuration</a>).</td></tr><tr><td>A gamepad does not work in one emulator only</td><td>Set <strong>AUTOCONFIGURE CONTROLLERS</strong> to <strong>OFF</strong> for this system and configure the controls in the emulator, then report the problem to the RetroBat team.</td></tr></tbody></table>

## Special controllers

RetroBat also maps some special controllers automatically: N64, Mega Drive / Genesis, Saturn… style controllers. See [Special controllers](special-controllers.md).
