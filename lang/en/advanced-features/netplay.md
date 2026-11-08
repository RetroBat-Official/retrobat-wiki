# Netplay

## What is netplay?

Netplay lets you play multiplayer games over a network, as if your friends were next to you on the same console. Each player runs the game on his own PC, and the players' inputs are sent over the network.

{% hint style="warning" %}
Netplay does not emulate the online features of the original consoles, and there is no dedicated server. Games or modes that needed an online service (Phantasy Star Online on Dreamcast, for example) do not work with netplay.
{% endhint %}

Netplay works with the **RetroArch cores** that support it.

## Enabling netplay

1. Open the **MAIN MENU** > **GAME SETTINGS** > **NETPLAY SETTINGS**.
2. Turn on **ENABLE NETPLAY**.
3. Enter a **NICKNAME**: it is the name the other players see.

<div align="left"><figure><img src="../.gitbook/assets/image (405).png" alt=""><figcaption></figcaption></figure></div>

4. Go back: RetroBat indexes your games (see below).

## Options

<table><thead><tr><th width="259">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>PORT</strong></td><td>Network port used when you host a game (55435 by default).</td></tr><tr><td><strong>USE RELAY SERVER</strong></td><td>Goes through a relay server instead of a direct connection. Useful when the players cannot connect directly (closed ports, some Internet boxes). Choose the closest server, or <strong>CUSTOM</strong> to enter your own server in <strong>CUSTOM RELAY SERVER</strong>.</td></tr><tr><td><strong>AUTOMATICALLY CREATE LOBBY</strong></td><td>When it is on (default), every compatible game you launch normally also creates a netplay game that other players can join.</td></tr><tr><td><strong>SHOW RELAY SERVER GAMES ONLY</strong></td><td>Only lists the games hosted through a relay server, which are easier to join (on by default).</td></tr><tr><td><strong>SHOW UNAVAILABLE GAMES</strong></td><td>Also lists the games that are not on your PC (on by default).</td></tr></tbody></table>

{% hint style="info" %}
To launch your games alone, without creating a netplay game, disable **AUTOMATICALLY CREATE LOBBY**. You can still host a game from the game options (see below).
{% endhint %}

## Game indexes

Indexing computes a fingerprint (CRC) of your games, so that RetroBat can check that you have the same game as the other players.

* **INDEX NEW GAMES AT STARTUP** (on by default): new games are indexed each time RetroBat starts.
* **INDEX GAMES**: indexes your games now (useful after adding many games).

## Hosting a game

1. In the game list, highlight the game and hold **SOUTH** to open the **GAME OPTIONS**.
2. Choose **START A NETPLAY GAME**.
3. Set the options if needed:
   * **PUBLICLY ANNOUNCE GAME**: shows your game in the public list of games, for all RetroArch and RetroBat players. Leave it off to play only with friends who know your game.
   * **PLAYER PASSWORD**: password asked to the players who join.
   * **VIEWER PASSWORD**: password asked to the spectators.
4. Choose **HOST A NETPLAY GAME**: the game starts and waits for the other players.

<div align="left"><figure><img src="../.gitbook/assets/image (406).png" alt=""><figcaption></figcaption></figure></div>

## Joining a game

1. In the [system view](../navigation/system-view-and-game-view.md#system-view), press **NORTH** (**NETPLAY**) to open the list of games.
2. The list shows the **LAN GAMES** (on your local network), the **AVAILABLE GAMES** (games that you have) and the **UNAVAILABLE GAMES** (games that you do not have).
3. Choose a game, then:
   * **JOIN GAME** to play;
   * **WATCH GAME** to watch as a spectator.

<div align="left"><figure><img src="../.gitbook/assets/image (407).png" alt=""><figcaption></figcaption></figure></div>

Each game shows a status:

<table><thead><tr><th width="271.5">Status</th><th>Meaning</th></tr></thead><tbody><tr><td><strong>SAME ROM</strong></td><td>You have exactly the same game as the host: you can join.</td></tr><tr><td><strong>DIFFERENT ROM</strong></td><td>You have the game, but not the same version: the game will not work correctly.</td></tr><tr><td><strong>UNKNOWN ROM VERSION</strong></td><td>The version of the game could not be checked.</td></tr><tr><td><strong>UNAVAILABLE CORE</strong></td><td>The core used by the host is not available on your PC.</td></tr></tbody></table>

Press **REFRESH** to update the list.

## Good to know

### Hosting

To host a game, the other players must be able to connect to your PC:

* your Internet box must support **UPnP**, which opens the port automatically;
* otherwise, open the port (55435 by default, or your own **PORT**) in the settings of your box;
* or use a relay server (**USE RELAY SERVER**), which avoids opening a port.

### Limitations

* **Connection:** a stable connection with a low ping is essential. The quality of the game depends on the slowest player.
* **Same version:** all players must have the **same game** (same ROM, check the SAME ROM status) and the **same core version**, so ideally the same RetroBat version.
* **Compatible core:** only the RetroArch cores that support netplay can be used.
* **Same architecture:** some cores do not allow netplay between different architectures. A message is shown when the core starts.
