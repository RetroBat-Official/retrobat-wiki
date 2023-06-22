# AI Translation Service

## Translation Service settings

This function can be used to translate screens from games that are written in a language you do not read in to your native language (e.g. Japanese to English).

Configuration can be done in the [Main Menu ](../navigation/main-menu.md)under **GAME SETTINGS** and **AI GAME TRANSLATION**.

<div align="left">

<figure><img src="https://i.imgur.com/9PkHi7R.png" alt=""><figcaption><p>GAME SETTINGS</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/wQswVu7.png" alt=""><figcaption><p>AI GAME TRANSLATION</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/GD7f7Ay.png" alt=""><figcaption><p>AI GAME TRANSLATION options</p></figcaption></figure>

</div>

<table><thead><tr><th width="290">Configuration Item</th><th>Description</th></tr></thead><tbody><tr><td><strong>Enable AI Translation Service</strong></td><td>Turn the translation feature ON or OFF</td></tr><tr><td><strong>Target Language</strong></td><td>Select the language you want to get the screens translated into</td></tr><tr><td><strong>AI Translation service URL</strong></td><td>Enter the translation service URL</td></tr><tr><td><strong>Pause on translated screen</strong></td><td>Select whether you want to keep the game going while the translation overlay is on or pause the game</td></tr></tbody></table>

### Translation Service URL

The service from [ztranslate.net](https://ztranslate.net/) can be used to translate games.

You will need to register on the website.

<div align="left">

<figure><img src="https://i.imgur.com/rLddOm8.png" alt=""><figcaption><p>Register</p></figcaption></figure>

</div>

Once the Sign up finalized, go to Settings and retrieve you API key.

<div align="left">

<figure><img src="https://i.imgur.com/7Oe139R.png" alt=""><figcaption><p>Retrieve API key at the bottom</p></figcaption></figure>

</div>

Now, enter the URL + API key in Retrobat AI GAME TRANSLATION settings and confirm.

Use the following format:

```
http://ztranslate.net/service?api_key=XXXYYYZZZ
```

(replace XXXYYYZZZ with your own API key)

<div align="left">

<figure><img src="https://i.imgur.com/OiGEpQD.png" alt=""><figcaption></figcaption></figure>

</div>

## Calling the translation while in game

You can now call the AI translation service in-game by using the `HOTKEY` + `R1` combination.
