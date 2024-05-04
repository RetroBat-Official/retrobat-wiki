# Netplay

## What is netplay ?

Netplay is a feature that enables multiplayer gaming over network, like if you were playing with a friend on the same console.

{% hint style="warning" %}
Netplay feature is not a simulation of the actual hardware network capabilities of a system. It does not provide dedicated servers to play games that have online options. For example it is not possible to play Phantasy Star Online with the Flycast Core like it would be possible on Dreamcast, the original hardware.
{% endhint %}

## Enabling Netplay

From the [MAIN MENU](../navigation/main-menu.md#system-settings) > System Settings, open **NETPLAY SETTINGS**

<div align="left">

<figure><img src="https://i.imgur.com/YzDNvgT.png" alt=""><figcaption></figcaption></figure>

</div>

Enable Netplay and enter a **NICKNAME**

<div align="left">

<figure><img src="https://i.imgur.com/fHM5DdV.png" alt=""><figcaption></figcaption></figure>

</div>

## **Indexing Games**

Retrobat will need to index games with NetPlay capabilities, this is done from the INDEX GAMES menu, you can also setup the system to index new games at startup.

<div align="left">

<figure><img src="https://i.imgur.com/UDjXs0o.png" alt=""><figcaption></figcaption></figure>

</div>

## Joining a NetPlay game

Once NetPlay is activated, when in the System View, use the ![](<../.gitbook/assets/image (50).png>)  button to display NetPlay Games

<div align="left">

<figure><img src="https://i.imgur.com/dfzVYyY.png" alt=""><figcaption></figcaption></figure>

</div>

This will open the list of currently available NetPlay sessions

<div align="left">

<figure><img src="https://i.imgur.com/bR2g3Ab.png" alt=""><figcaption></figcaption></figure>

</div>

Select one of the available games and launch it to join a netplay session.



## Hosting a NetPlay game

If you want to host a NetPlay game session, select the game in your Gamelist and from the [Game Options](../navigation/game-options.md) menu choose **START A NETPLAY GAME**

<div align="left">

<figure><img src="https://i.imgur.com/XriDKwq.png" alt=""><figcaption></figcaption></figure>

</div>

In the next screen, select HOST A NETPLAY GAME to start a NetPlay session.

<div align="left">

<figure><img src="https://i.imgur.com/t1ENzuy.png" alt=""><figcaption></figcaption></figure>

</div>

The session will be visible in the Netplay Sessions screen and other players will be able to join.

{% hint style="info" %}
You can also add passwords to your session to allow only designated people to join the session.
{% endhint %}

## NetPlay considerations

### NetPlay hosting

When hosting a Netplay server, make sure that your network is either compatible with UPNP to automatically open the right port, or you can define your own port in the settings, and configure your router and network to keep this port open from the outside.



### NetPlay limitations

* You need a very stable Internet connection, with a low ping value. Your user experience is heavily depending on the quality of your internet connection.&#x20;
* All players in a Netplay session need to have the same core version, and the same ROM to play together. That means that you need to use the same Retrobat version, and you should always check and compare the MD5 checksums of the ROM that all members in your party are going to use.
* Check that you use a core that is compatible with Netplay - see below for the list of cores that support Netplay.
* Check that all the members of your party are using the same architecture. Some cores don't enable cross-architecture Netplay. Whenever this happens, you'll see a message popping-up upon launching the core.
