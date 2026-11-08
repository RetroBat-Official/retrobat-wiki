# AI Translation Service

The AI translation service translates the text of a game on the fly. When you press the hotkey, RetroArch takes a screenshot of the game, sends it to an online service that reads and translates the text, then shows the translation over the game.

{% hint style="info" %}
* The service only works with **RetroArch cores**.
* An **Internet connection** is needed.
* The translation is automatic: it can be approximate, and some text (stylized fonts, small text) may not be read correctly.
{% endhint %}

## Enabling the translation

1. Open the [**MAIN MENU**](../navigation/main-menu.md) > **GAME SETTINGS**, **RETROARCH OPTIONS** group > **AI GAME TRANSLATION**.
2. Turn on **ENABLE AI TRANSLATION SERVICE**.
3. Choose your **TARGET LANGUAGE**: the language in which the text is translated. The language of the game is detected automatically.

<div align="left"><figure><img src="../.gitbook/assets/image (408).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="311.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>ENABLE AI TRANSLATION SERVICE</strong></td><td>Enables the translation in RetroArch games.</td></tr><tr><td><strong>TARGET LANGUAGE</strong></td><td>Language of the translation.</td></tr><tr><td><strong>AI TRANSLATION SERVICE URL</strong></td><td>Address of the translation service. Leave it empty to use the default service (see below).</td></tr><tr><td><strong>PAUSE ON TRANSLATED SCREEN</strong></td><td>Pauses the game while the translation is shown.</td></tr></tbody></table>

## Translating during a game

| Action                                               | Controller        |
| ---------------------------------------------------- | ----------------- |
| Translate the screen                                 | HOTKEY + R1       |
| Hide the translation (and resume the game if paused) | HOTKEY + R1 again |

<div align="left"><figure><img src="../.gitbook/assets/image (409).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
If you customized your hotkeys, use your own combination. See the Hotkeys page.
{% endhint %}

## Translation service

By default, RetroBat uses the **ZTranslate** service with a shared key: it works without any account. As this key is shared by many players, the service can be slow or unavailable at times.

To use your own key:

1. Create a free account on [ztranslate.net](https://ztranslate.net), then get your API key in your profile.

<div align="left"><figure><img src="../.gitbook/assets/image (411).png" alt=""><figcaption></figcaption></figure></div>

2. In **AI TRANSLATION SERVICE URL**, enter: `http://ztranslate.net/service?api_key=YOUR_KEY` (replace `YOUR_KEY` with your key).

<div align="left"><figure><img src="../.gitbook/assets/image (410).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Write the address with `http://`, not `https://`. RetroBat adds the language and display settings at the end of the address by itself: do not add them.
{% endhint %}

## Common problems

<table><thead><tr><th width="350.25">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>Nothing happens when pressing HOTKEY + R1</td><td>Check that the service is enabled and that the game uses a RetroArch core. Check your Internet connection.</td></tr><tr><td>The translation takes long or never appears</td><td>The shared service may be overloaded: try again later, or use your own key.</td></tr><tr><td>The translation is wrong or incomplete</td><td>The text could not be read correctly (stylized font, small text). Try on a screen with clearer text.</td></tr></tbody></table>
