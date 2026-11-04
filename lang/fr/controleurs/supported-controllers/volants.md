---
description: Vroum vroum
---

# 🛞 Volants

{% hint style="warning" %}
**En cours de développement** : la gestion des volants dans RetroBat est encore en construction. Seuls quelques volants ont une configuration prête pour chaque émulateur, et ils n'ont pu être testés qu'avec les volants que possède l'équipe.

**Nous avons besoin de vous !** Si vous avez un volant qui n'est pas encore configuré, créez son mappage (voir plus bas) et partagez-le sur le Discord RetroBat ou sur GitHub, pour qu'il soit ajouté à RetroBat pour tout le monde.
{% endhint %}

## Fonctionnement

Quand les volants sont activés, RetroBat :

1. détecte les volants branchés grâce à leur identifiant USB (voir la liste des volants détectés) ;
2. cherche le mappage de ce modèle de volant dans le fichier de mappage de l'émulateur (`system\resources\inputmapping\wheels`) ;
3. écrit ce mappage dans la configuration de l'émulateur (direction, pédales, vitesses, boutons).

Si un volant n'est pas dans la liste des volants détectés, ou n'a pas de mappage pour l'émulateur, RetroBat ne le configure pas comme un volant.

{% hint style="info" %}
* Un volant **avec pédalier** est nécessaire (accélérateur et frein) : RetroBat ne propose pas de jouer avec un volant sans pédales.
* Le levier de vitesses est optionnel. Sur certains volants Thrustmaster, le levier est un périphérique séparé : c'est géré par la valeur `DeportedShifter` des fichiers de mappage.
{% endhint %}

## Activer les volants

Les volants **ne sont pas activés automatiquement**. Activez-les pour un système ou pour un jeu :

* Pour un système : ouvrez les [Options d'affichage](../../navigation/view-options.md) du système, choisissez **CONFIGURATION AVANCÉE DU SYSTÈME**, puis **VOLANTS DE COURSE**, et réglez **ACTIVER LES VOLANTS** sur **ON**.
* Pour un jeu : même option dans les [Options du jeu](../../navigation/game-options.md) > **CONFIGURATION AVANCÉE DU JEU** > **VOLANTS DE COURSE**.

<div align="left"><figure><img src="../../.gitbook/assets/image (362).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (363).png" alt=""><figcaption></figcaption></figure></div>

Le sous-menu **VOLANTS DE COURSE** contient aussi les options volant de chaque émulateur (retour de force, disposition des boutons…), voir le tableau plus bas.

### Jeux au volant

RetroBat sait quels jeux se jouent au volant :

* Une icône de volant s'affiche à côté de leur nom dans la liste des jeux (**MENU PRINCIPAL > PARAMÈTRES D'AFFICHAGE > ICÔNES > AFFICHER L'ICÔNE VOLANT**).

<div align="left"><figure><img src="../../.gitbook/assets/image (364).png" alt=""><figcaption></figcaption></figure></div>

* La collection **VOLANT** contient tous les jeux au volant.

<div align="left"><figure><img src="../../.gitbook/assets/image (365).png" alt=""><figcaption></figcaption></figure></div>

La liste des jeux au volant est dans le fichier `emulationstation\resources\gamesdb.xml` (jeux marqués `<wheel/>`). Pour la personnaliser, copiez le fichier dans `emulationstation\.emulationstation\resources\gamesdb.xml` et modifiez la copie : elle est lue en priorité et n'est pas écrasée par les mises à jour de RetroBat.

<div align="left"><figure><img src="https://i.imgur.com/2wr4B4z.png" alt=""><figcaption></figcaption></figure></div>

## Émulateurs compatibles

<table><thead><tr><th width="149">Émulateur</th><th width="153">Systèmes</th><th>Fichier de mappage</th><th>Options volant (sous-menu VOLANTS DE COURSE)</th></tr></thead><tbody><tr><td><strong>Model 2 Emulator</strong></td><td>Sega Model 2</td><td><code>model2_wheels.yml</code></td><td>ACTIVER LE RETOUR DE FORCE, GARDER LES VITESSES</td></tr><tr><td><strong>Supermodel</strong></td><td>Sega Model 3</td><td><code>model3_wheels.yml</code></td><td>ACTIVER LE RETOUR DE FORCE, FORCER L'INDEX DU VOLANT</td></tr><tr><td><strong>Flycast</strong></td><td>Dreamcast, Naomi, Atomiswave</td><td><code>flycast_wheels.yml</code> (Dreamcast), <code>flycast_racing_wheels.yml</code> (Dreamcast avec <strong>UTILISER LE RACING CONTROLLER</strong>), <code>flycast_arcade_wheels.yml</code> (arcade)</td><td>UTILISER LE RACING CONTROLLER, DISPOSITION DES BOUTONS DU VOLANT</td></tr><tr><td><strong>PCSX2</strong></td><td>PlayStation 2</td><td><code>pcsx2_wheels.yml</code></td><td>TYPE DE VOLANT JOUEUR 1, ACTIVER LE RETOUR DE FORCE, SIMULER LE VOLANT AVEC LA MANETTE…</td></tr><tr><td><strong>PCSX2x6</strong></td><td>Namco System 246/256</td><td><code>pcsx2x6_wheels.yml</code></td><td>ACTIVER LE RETOUR DE FORCE</td></tr><tr><td><strong>TeknoParrot</strong></td><td>Arcade sur PC</td><td><code>teknoparrot_wheels.yml</code></td><td>BOUTONS COIN &#x26; START, BOUTONS TEST &#x26; SERVICE, PROFIL PERSONNALISÉ…</td></tr><tr><td><strong>RetroArch - lr-flycast</strong></td><td>Dreamcast, Naomi, Atomiswave</td><td><code>libretro_flycast_wheels.yml</code>(pas encore fourni)</td><td>ACTIVER LES VOLANTS</td></tr></tbody></table>

### Volants avec un mappage prêt

| Volant                         | Model 2 | Supermodel | Flycast | PCSX2 / PCSX2x6 | TeknoParrot |
| ------------------------------ | :-----: | :--------: | :-----: | :-------------: | :---------: |
| Logitech G29                   |    ✔    |      ✔     |    ✔    |        ✔        |      ✔      |
| Logitech G920                  |    ✔    |            |    ✔    |                 |      ✔      |
| Logitech G923 (PlayStation)    |    ✔    |            |    ✔    |        ✔        |      ✔      |
| Logitech G923 (Xbox)           |    ✔    |            |    ✔    |                 |      ✔      |
| Logitech Driving Force GT      |         |            |    ✔    |        ✔        |             |
| Thrustmaster T300RS (mode PS3) |    ✔    |            |    ✔    |        ✔        |      ✔      |
| Moza R5                        |         |            |    ✔    |        ✔        |      ✔      |

TeknoParrot a aussi un mappage pour de nombreux autres volants (Logitech G Pro, Thrustmaster T150 / TMX / T248 / T300RS PS4 / T500RS / TX / TS-XW, Fanatec, Moza R9 / R12 / R16, Simucube, Simagic, Asetek, Cammus, PXN V9) et un mappage `default` utilisé pour les autres volants détectés.

{% hint style="info" %}
**Thrustmaster T300RS** : réglez les pédales en mode **séparé** (split) dans le Thrustmaster Control Panel, et vérifiez qu'elles ne sont pas inversées (corrigé en maintenant **MODE + L3 + R3**).
{% endhint %}

## Ajouter ou modifier le mappage d'un volant

{% hint style="info" %}
Les fichiers de mappage des volants fournis par RetroBat sont dans `system\resources\inputmapping\wheels`. Vos propres fichiers vont dans `user\inputmapping` .
{% endhint %}

Chaque fichier de mappage contient **un bloc par modèle de volant**, nommé avec le nom RetroBat du volant (voir Volants détectés). Les lignes du bloc sont indentées de 2 espaces.

{% hint style="warning" %}
Chaque émulateur utilise **sa propre notation** pour les boutons et les axes (boutons numérotés à partir de 0 ou de 1, noms des axes…). Partez toujours d'un bloc existant **du même fichier** (le bloc `LogitechG29` est un bon exemple) et lisez les explications en haut du fichier.
{% endhint %}

### Exemple : Model 2 Emulator

Le bloc `LogitechG29` de `model2_wheels.yml` :

```yaml
LogitechG29:
  DeportedShifter: false
  Up: hatup
  Down: hatdown
  Left: hatleft
  Right: hatright
  Steer: axis0
  Throttle: axis1
  Brake: axis2
  ShiftDown: button5
  ShiftUp: button4
  South: button0
  East: button2
  West: button1
  North: button3
  Start: button9
  Select: button8
  Gear1: button12
  Gear2: button13
  Gear3: button14
  Gear4: button15
  GearN: button18
  Service: button10
  Test: button11
```

* `axis0`, `axis1`… sont les axes du volant (direction, accélérateur, frein). Utilisez `axisinv` au lieu de `axis` pour inverser un axe.
* `button0`, `button1`… sont les boutons du volant, **numérotés à partir de 0**. Dans le panneau des contrôleurs de jeu de Windows (`joy.cpl` > Propriétés), les boutons sont numérotés à partir de 1 : retirez 1.
* `DeportedShifter: true` ne sert que pour les volants dont le levier de vitesses est un périphérique séparé.

Pour ajouter votre volant :

1. Copiez le fichier dans `user\inputmapping` (par exemple `user\inputmapping\model2_wheels.yml`) : RetroBat lit cette copie en priorité, et elle n'est pas écrasée par les mises à jour.
2. Dupliquez le bloc `LogitechG29` et renommez-le avec le nom de votre volant (par exemple `ThrustmasterT150:`).
3. Remplacez les valeurs par les axes et boutons de votre volant, puis testez en jeu.
4. Vérifiez `emulationstation\emulatorLauncher.log` : les lignes `[WHEELS]` indiquent le volant détecté et le mappage utilisé.

{% hint style="info" %}
Pour **Flycast** et **PCSX2**, le plus simple est de configurer le volant une fois dans l'émulateur lui-même, puis de reporter les valeurs du fichier de configuration qu'il crée (pour Flycast : `emulators\flycast\mappings`). La valeur `name` doit être le nom exact du volant affiché par l'émulateur.
{% endhint %}

{% hint style="success" %}
Votre mappage fonctionne ? Partagez-le sur le Discord RetroBat ou sur GitHub, pour qu'il soit ajouté à RetroBat !
{% endhint %}

### RetroArch (lr-flycast)

La gestion des volants est prête pour le core **lr-flycast** (option **ACTIVER LES VOLANTS**), mais **RetroBat ne fournit pas encore de fichier de mappage pour ce core**. Pour utiliser votre volant avec lr-flycast, créez le fichier `libretro_flycast_wheels.yml` dans `user\inputmapping`, avec un bloc par volant :

* les clés sont les entrées RetroArch : `a`, `b`, `x`, `y`, `start`, `select`, `up`, `down`, `left`, `right`, `l`, `r`, `l2`, `r2`, `l3`, `r3`, `l_x_minus`, `l_x_plus`, `l_y_minus`, `l_y_plus`… ;
* une valeur qui commence par `+` ou `-` est un **axe** (par exemple `-0` pour l'axe 0 dans le sens négatif), toute autre valeur est un numéro de **bouton** ;
* la clé optionnelle `driver` indique le pilote d'entrée RetroArch à utiliser avec ce volant (`sdl2`, `dinput`…).

```yaml
LogitechG29:
  driver: sdl2
  l_x_minus: ...   # direction à gauche (axe)
  l_x_plus: ...    # direction à droite (axe)
  r2: ...          # accélérateur (axe)
  l2: ...          # frein (axe)
  a: ...           # bouton
  b: ...           # bouton
  start: ...       # bouton
```

Si vous créez ce fichier, partagez-le avec l'équipe !

## Volants détectés

<details>

<summary>Noms RetroBat des volants et identifiants USB</summary>

VID\_2433\&PID\_F300 : AsetekInvicta\
VID\_2433\&PID\_F301 : AsetekForte\
VID\_2433\&PID\_F303 : AsetekLaPrima\
VID\_2433\&PID\_F306 : AsetekTonyKannan\
VID\_3416\&PID\_0301 : CammusC5\
VID\_3416\&PID\_0302 : CammusC12\
VID\_0EB7\&PID\_0001 : FanatecClubSportWheelBaseV2\
VID\_0EB7\&PID\_0004 : FanatecClubSportWheelBaseV25\
VID\_0EB7\&PID\_0005 : FanatecCSLElitePS4\
VID\_0EB7\&PID\_0006 : FanatecPodiumDD1\
VID\_0EB7\&PID\_0007 : FanatecPodiumDD2\
VID\_0EB7\&PID\_0011 : FanatecCSRElite\
VID\_0EB7\&PID\_0020 : FanatecDD\
VID\_0EB7\&PID\_0E03 : FanatecCSLElite\
VID\_046D\&PID\_C202 : LogitechWingmanFormula\
VID\_046D\&PID\_C20E : LogitechWingmanFormulaGP\
VID\_046D\&PID\_C24F : LogitechG29\
VID\_046D\&PID\_C260 : LogitechG29\
VID\_046D\&PID\_C262 : LogitechG920\
VID\_046D\&PID\_C266 : LogitechG923PS\
VID\_046D\&PID\_C267 : LogitechG923PS\
VID\_046D\&PID\_C26D : LogitechG923X\
VID\_046D\&PID\_C26E : LogitechG923X\
VID\_046D\&PID\_C272 :  LogitechGPro\
VID\_046D\&PID\_C293 : LogitechWingmanFormulaForce\
VID\_046D\&PID\_C294 : LogitechDrivingForce\
VID\_046D\&PID\_C295 : LogitechMomoForce\
VID\_046D\&PID\_C298 : LogitechDrivingForce\
VID\_046D\&PID\_C299 : LogitechG25\
VID\_046D\&PID\_C29A : LogitechDrivingForceGT\
VID\_046D\&PID\_C29B : LogitechG27\
VID\_046D\&PID\_C29C : LogitechSpeedForce\
VID\_046D\&PID\_CA03 : LogitechMomoRacing\
VID\_046D\&PID\_CA04 : LogitechRacingWheel\
VID\_045E\&PID\_001A : MicrosoftSideWinder\
VID\_045E\&PID\_0034 :  MicrosoftSideWinder\
VID\_346E\&PID\_0000 : MozaR16\
VID\_346E\&PID\_0002 : MozaR9\
VID\_346E\&PID\_0004 : MozaR5\
VID\_346E\&PID\_0005 : MozaR3\
VID\_346E\&PID\_0006 : MozaR12\
VID\_0483\&PID\_0522 : SimagicM10\
VID\_16D0\&PID\_0D5A : Simucube1\
VID\_16D0\&PID\_0D5F : Simucube2Ultimate\
VID\_16D0\&PID\_0D60 : Simucube2Pro\
VID\_16D0\&PID\_0D61 : Simucube2Sport\
VID\_1FC9\&PID\_804C : SimXperienceAccuForcePro\
VID\_044F\&PID\_B56A : ThrustmasterF430FF\
VID\_044F\&PID\_B56E : ThrustmasterT500RS\
VID\_044F\&PID\_B605 : ThrustmasterNascarProFF2\
VID\_044F\&PID\_B651 : ThrustmasterFGTRumbleForce\
VID\_044F\&PID\_B653 : ThrustmasterRGT\
VID\_044F\&PID\_B654 : ThrustmasterFGTFF\
VID\_044F\&PID\_B669 : ThrustmasterTX\
VID\_044F\&PID\_B66D : ThrustmasterT300RSPS4\
VID\_044F\&PID\_B66E : ThrustmasterT300RSPS3\
VID\_044F\&PID\_B66F : ThrustmasterT300RSPS3ADV\
VID\_044F\&PID\_B677 : ThrustmasterT150\
VID\_044F\&PID\_B67F : ThrustmasterTMX\
VID\_044F\&PID\_B689 : ThrustmasterTSPC\
VID\_044F\&PID\_B692 : ThrustmasterTSXW\
VID\_044F\&PID\_B696 : ThrustmasterT248\
VID\_0483\&PID\_A355 :  VRSDirectForcePro\
VID\_11FF\&PID\_0511 : PXNV9

</details>

Votre volant n'est pas dans la liste ? Relevez son VID et son PID dans le Gestionnaire de périphériques de Windows (Propriétés > Détails > ID du matériel) et envoyez-les à l'équipe sur Discord ou GitHub.
