---
description: Pioneer
---

# Pioneer LaserActive

<div align="left"><figure><img src="../../../.gitbook/assets/image (626).png" alt="" width="480"><figcaption></figcaption></figure></div>

## Présentation

Le **LaserActive** est un lecteur LaserDisc de Pioneer sorti en 1993 (CLD-A100). Il devient une console de jeu grâce à des modules à insérer à l'avant, les « PAC » :

* le **PAC Mega-LD** (Sega) lit les disques Mega-LD, ainsi que les cartouches Mega Drive et les CD Mega-CD ;
* le **PAC LD-ROM²** (NEC) lit les disques LD-ROM², ainsi que les HuCard et CD-ROM² de la PC Engine.

Les jeux LaserActive mêlent la vidéo analogique du LaserDisc et les données du jeu : vidéo plein écran de qualité, cinématiques interactives, jeux de tir sur fond vidéo. Environ 24 jeux Mega-LD et 14 jeux LD-ROM² sont sortis, comme **Pyramid Patrol**, **Hyperion**, **Triad Stone**, **J.B. Harold: Blue Chicago Blues** (Mega-LD) ou **Vajra** et **Road Prosecutor** (LD-ROM²).

L'émulation est récente : ares est le premier émulateur à faire tourner le Mega-LD (2025), puis le LD-ROM². RetroBat propose **ares** avec deux cores, un par PAC (**MegaLD** par défaut, **NecLD**), et le core libretro **geargrafx** (LD-ROM² uniquement).

Les jeux Mega Drive, Mega-CD et PC Engine se lancent depuis leurs propres systèmes : ce système ne sert qu'aux disques LaserActive.

{% embed url="https://fr.wikipedia.org/wiki/Pioneer_LaserActive" %}

## En bref

<table><thead><tr><th width="294"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\laseractive</code></td></tr><tr><td><strong>Extensions</strong></td><td>.mmi</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>ares (MegaLD)</td></tr><tr><td><strong>BIOS</strong></td><td>Obligatoires, un par PAC (voir plus bas)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core geargrafx ; ares par raccourcis (non gérées par RetroBat)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core geargrafx (LD-ROM²)</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>syscard1.pce</code>, <code>gexpress.pce</code> dans <code>bios</code> (certains jeux LD-ROM²)</td></tr></tbody></table>

## Quel émulateur choisir ?

Le core dépend du disque : un disque Mega-LD ne se lance qu'avec **MegaLD**, un disque LD-ROM² qu'avec **NecLD** ou **geargrafx**. Les jeux LD-ROM² doivent donc être réglés sur l'un de ces deux cores.&#x20;

<table><thead><tr><th width="184.5">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>ares: MegaLD</strong> (défaut)</td><td>Seul émulateur Mega-LD. Tous les jeux Mega-LD copiés à ce jour sont jouables.</td><td>Disques Mega-LD uniquement. Sauvegardes instantanées non gérées par RetroBat.</td></tr><tr><td><strong>ares: NecLD</strong></td><td>Émulation LD-ROM² d'origine, par l'auteur de l'émulation Mega-LD.</td><td>Disques LD-ROM² uniquement. Sauvegardes instantanées non gérées par RetroBat.</td></tr><tr><td><strong>libretro: geargrafx</strong></td><td>LD-ROM² dans RetroArch : sauvegardes instantanées gérées par RetroBat, shaders, jeu en réseau.</td><td>Disques LD-ROM² uniquement.</td></tr></tbody></table>

## BIOS

Chaque PAC a son propre BIOS : placez celui du PAC de vos jeux (ou les deux) dans `bios\laseractive`.

**PAC Mega-LD (ares MegaLD)** : il faut le BIOS de la région du disque (US ou Japon).

| Fichier                                         | Région | Dossier            |
| ----------------------------------------------- | ------ | ------------------ |
| `[BIOS] LaserActive PAC-S10 (US) (v1.04).bin`   | US     | `bios\laseractive` |
| `[BIOS] LaserActive PAC-S1 (Japan) (v1.05).bin` | Japon  | `bios\laseractive` |

RetroBat accepte aussi les versions plus anciennes, si la précédente est absente : `[BIOS] LaserActive PAC-S10 (US) (v1.02).bin`, `[BIOS] LaserActive PAC-S1 (Japan) (v1.02).bin` et `[BIOS] LaserActive PAC-S1 (Japan) (v1.01).bin`.

**PAC LD-ROM² (ares NecLD, core geargrafx)** : un seul de ces fichiers suffit.

| Fichier                                          | Région                    | Dossier            |
| ------------------------------------------------ | ------------------------- | ------------------ |
| `[BIOS] LaserActive PAC-N10 (US) (v1.02).bin`    | US                        | `bios\laseractive` |
| `[BIOS] LaserActive PAC-N1 (Japan) (v1.02).bin`  | Japon                     | `bios\laseractive` |
| `[BIOS] LaserActive PCE-LP1 (Japan) (v1.02).bin` | Japon (PAC vendu par NEC) | `bios\laseractive` |

Le core geargrafx utilise les mêmes fichiers : RetroBat les copie à la racine de `bios` sous les noms attendus par le core (`pac-n10.bin`, `pac-n1.bin`, `pce-lp1.bin`).

**BIOS optionnels (ares NecLD, core geargrafx)** : certains jeux LD-ROM² demandent une carte PC Engine insérée dans la console.

<table><thead><tr><th width="167">Fichier</th><th>Description</th><th>Dossier</th></tr></thead><tbody><tr><td><code>syscard1.pce</code></td><td>System Card 1.0 (PC Engine CD)</td><td><code>bios</code></td></tr><tr><td><code>gexpress.pce</code></td><td>Games Express</td><td><code>bios</code></td></tr></tbody></table>

Avec le core geargrafx, **ÉMULATION > BIOS CD-ROM** choisit la System Card utilisée par ces jeux : SYSTEM CARD 1 par défaut si `syscard1.pce` est présent, sinon SYSTEM CARD 3 (`syscard3.pce`).

## Quel format de jeu ?

<table><thead><tr><th width="139">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.mmi</strong></td><td>Mixed Media Image : un fichier par face de disque, avec la vidéo, le son et les données du jeu. C'est le seul format lu par ares et geargrafx.</td></tr></tbody></table>

* Les fichiers sont très gros : de 28 à 36 Go par face pour la plupart des jeux, davantage pour certains.
* Le format est déjà compressé : ne le mettez pas dans une archive `.zip` ou `.7z`.
* Placez les jeux sur un **SSD** : un disque dur classique est trop lent pour lire la vidéo sans saccades.
* Un PC récent de milieu de gamme suffit pour jouer à pleine vitesse.

## Contrôles

### Configuration automatique

**PAC Mega-LD (ares MegaLD)** : manette Mega Drive 6 boutons.

<table><thead><tr><th width="246.5">Manette RetroBat</th><th>Mega Drive</th></tr></thead><tbody><tr><td>OUEST / SUD / EST</td><td>A / B / C</td></tr><tr><td>L1 / NORD / R1</td><td>X / Y / Z</td></tr><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>MODE</td></tr><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (628).png" alt="" width="225"><figcaption></figcaption></figure></div>

**PAC LD-ROM² (ares NecLD, core geargrafx)** : manette PC Engine.

<table><thead><tr><th width="231.5">Manette RetroBat</th><th>PC Engine</th></tr></thead><tbody><tr><td>EST / SUD</td><td>I / II</td></tr><tr><td>START</td><td>RUN</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr></tbody></table>

Avec le core geargrafx, **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit la manette : MANETTE PC ENGINE (par défaut), AVENUE PAD 3 ou AVENUE PAD 6. **CONTRÔLES > UTILISER LE TURBO-TAP** branche le multitap.

<div align="left"><figure><img src="../../../.gitbook/assets/image (627).png" alt="" width="225"><figcaption></figcaption></figure></div>

### Raccourcis

ares utilise les raccourcis de RetroBat (par PadToKey) :

| Action                          | Manette             | Clavier          |
| ------------------------------- | ------------------- | ---------------- |
| Quitter                         | HOTKEY + START      | `Échap`          |
| Pause                           | HOTKEY + SUD        | `P`              |
| Sauvegarde instantanée          | HOTKEY + OUEST      | `F2`             |
| Chargement                      | HOTKEY + NORD       | `F4`             |
| Emplacement précédent / suivant | HOTKEY + Bas / Haut | `F6` / `F7`      |
| Rembobiner (si activé)          | HOTKEY + Gauche     | `Retour arrière` |
| Avance rapide (maintenir)       | HOTKEY + Droite     | `L`              |
| Capture d'écran                 | HOTKEY + R3         | `F8`             |
| Plein écran                     | HOTKEY + L3         | `F`              |

Le core geargrafx utilise les raccourcis de RetroArch.

Pour plus de détails, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="352.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\laseractive</code></td></tr><tr><td>BIOS</td><td><code>bios\laseractive</code> (et <code>bios</code> pour <code>syscard1.pce</code> et <code>gexpress.pce</code>)</td></tr><tr><td>ares : sauvegardes</td><td><code>saves\laseractive\ares</code></td></tr><tr><td>Core geargrafx : sauvegardes</td><td><code>saves\laseractive</code></td></tr><tr><td>Core geargrafx : sauvegardes instantanées</td><td><code>saves\laseractive\libretro.geargrafx</code></td></tr><tr><td>ares : captures d'écran</td><td><code>screenshots\ares</code></td></tr></tbody></table>

## Guides

### Changer de face de disque (ares)

Certains jeux tiennent sur plusieurs faces (**J.B. Harold: Blue Chicago Blues**, par exemple), avec un fichier `.mmi` par face. ares ne propose pas de raccourci pour changer de face :

1. Quand le jeu demande de retourner le disque, passez en fenêtre avec HOTKEY + L3 (ou `F`).
2. Dans la barre de menus d'ares, ouvrez **LaserActive (SEGA PAC) > Change Side** (ou **LaserActive (NEC PAC) > Change Side**) et choisissez la face demandée.
3. Revenez en plein écran avec HOTKEY + L3.

### Région du PAC LD-ROM² (geargrafx)

**ÉMULATION > RÉGION LASERACTIVE** choisit le BIOS utilisé : JAPON (`PAC-N1` ou `PCE-LP1`) ou US (`PAC-N10`). Par défaut, le core choisit automatiquement.

**VIDÉO > RAPPORT D'ASPECT LASERACTIVE** change le format de l'image : 4:3 par défaut, ou 1:1 PAR, 16:9 DAR, 16:10 DAR.

## Problèmes connus

<table><thead><tr><th width="350.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Un disque LD-ROM² ne démarre pas</td><td>Le jeu est lancé avec le core MegaLD (par défaut) : choisissez le core NecLD ou geargrafx pour ce jeu.</td></tr><tr><td>ares demande le firmware « Mega LD - BIOS (US) » ou « (Japan) »</td><td>Le BIOS Mega-LD de la région du disque manque dans <code>bios\laseractive</code>.</td></tr><tr><td>ares NecLD demande le firmware « PAC-N10 (US) » ou « PAC-N1 (Japan) »</td><td>Aucun BIOS LD-ROM² dans <code>bios\laseractive</code> : un des trois fichiers suffit.</td></tr><tr><td>ares NecLD demande le firmware « System-Card 1.0 » ou « Games Express », ou le core geargrafx ne démarre pas le jeu</td><td>Ce jeu LD-ROM² a besoin de la carte PC Engine correspondante : placez <code>syscard1.pce</code> ou <code>gexpress.pce</code> dans <code>bios</code>.</td></tr><tr><td>La vidéo saccade</td><td>Placez les jeux sur un SSD et ne les compressez pas.</td></tr><tr><td>Le jeu demande de retourner le disque</td><td>Voir <strong>Changer de face de disque</strong> dans <a href="pioneer-laseractive.md#changer-de-face-de-disque-ares"><strong>Guides</strong></a>.</td></tr></tbody></table>
