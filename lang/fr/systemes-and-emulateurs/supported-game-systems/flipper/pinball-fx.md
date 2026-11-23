---
description: Zen Studios
---

# Pinball FX

<div align="left"><figure><img src="../../../.gitbook/assets/image (1).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**Pinball FX** est la plateforme de flipper de **Zen Studios** sortie en 2023 (accès anticipé sur l'Epic Games Store en 2022), successeur de Pinball FX3. Le jeu est gratuit ; les tables s'achètent à l'unité ou par collection. Wild West Rampage, Fish Tales et Sorcerer's Lair sont gratuites.

RetroBat lance directement une table, dans le mode de jeu choisi.

{% embed url="https://fr.wikipedia.org/wiki/Pinball_FX" %}

## En bref

<table><thead><tr><th width="285.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\pinballfx</code></td></tr><tr><td><strong>Extensions</strong></td><td>.table</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>pinballfx (version steam)</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Par le jeu (RetroBat ne la modifie pas)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

L'émulateur `pinballfx` a deux versions (core) :

<table><thead><tr><th width="174.5">Version</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>steam</strong> (par défaut)</td><td>Le jeu installé avec Steam est lancé par Steam, directement sur la table choisie.</td><td>Steam doit être installé, avec le jeu.</td></tr><tr><td><strong>nonsteam</strong></td><td>Lance directement l'exécutable du jeu, sans passer par Steam.</td><td>Le jeu doit se trouver dans <code>emulators\pinballfx</code>.</td></tr></tbody></table>

Pour **nonsteam**, RetroBat cherche `PinballFX.exe` dans le dossier `emulators\pinballfx`. Si le jeu n'y est pas, un message indique le dossier attendu.

## BIOS

Aucun BIOS nécessaire.

## Ajouter des tables

Chaque table est un petit fichier texte `.table` qui contient le **numéro de la table** :

1. Dans `roms\pinballfx`, créez un fichier texte, par exemple `Wild West Rampage.txt`.
2. Écrivez le numéro de la table sur la première ligne (75 pour Wild West Rampage).
3. Enregistrez, puis remplacez l'extension `.txt` par `.table`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Seules les tables que vous possédez se lancent depuis RetroBat (en plus des tables gratuites).
{% endhint %}

<details>

<summary>Numéros des tables</summary>

| N°  | Table                                                 |
| --- | ----------------------------------------------------- |
| 1   | Civil War                                             |
| 2   | Star Wars™ Pinball: Masters of the Force              |
| 4   | South Park™: Super Sweet Pinball                      |
| 5   | Fear Itself                                           |
| 6   | Star Wars™ Pinball: Starfighter Assault               |
| 7   | Thor                                                  |
| 10  | Star Wars™ Pinball: Han Solo                          |
| 12  | Star Wars™ Pinball: Episode IV A New Hope             |
| 17  | Marvel's The Avengers                                 |
| 20  | Excalibur                                             |
| 21  | Ghost Rider                                           |
| 22  | Deadpool                                              |
| 23  | Pasha                                                 |
| 24  | Star Wars™ Pinball: Episode VI Return of the Jedi     |
| 27  | Biolab                                                |
| 28  | Star Wars™ Pinball: Darth Vader                       |
| 29  | Adventure Land                                        |
| 30  | Doctor Strange                                        |
| 31  | Rome                                                  |
| 33  | Sorcerer's Lair                                       |
| 36  | Super League Football                                 |
| 38  | Fantastic Four                                        |
| 40  | CastleStorm                                           |
| 43  | Star Wars™ Pinball: Episode V The Empire Strikes Back |
| 45  | Blade                                                 |
| 46  | Spider-Man                                            |
| 47  | Star Wars™ Pinball: The Clone Wars                    |
| 48  | Captain America                                       |
| 49  | Moon Knight                                           |
| 50  | Marvel's Guardians of the Galaxy                      |
| 53  | Star Wars™ Pinball: Boba Fett                         |
| 55  | South Park™: Butters' Very Own Pinball Game           |
| 56  | World War Hulk                                        |
| 58  | Star Wars™ Pinball: Droids™                           |
| 59  | X-Men                                                 |
| 60  | The Infinity Gauntlet                                 |
| 65  | Iron Man                                              |
| 66  | Secrets of the Deep                                   |
| 67  | Epic Quest                                            |
| 71  | Wolverine                                             |
| 73  | Venom                                                 |
| 75  | Wild West Rampage                                     |
| 77  | Star Wars™ Pinball: Star Wars Rebels™                 |
| 78  | Marvel's Avengers: Age of Ultron                      |
| 79  | Marvel's Ant-Man                                      |
| 80  | Son of Zeus                                           |
| 88  | Star Wars™ Pinball: The Force Awakens™                |
| 89  | Star Wars™ Pinball: Might of the First Order          |
| 90  | Fallout™ Pinball                                      |
| 91  | The Elder Scrolls V: Skyrim™ Pinball                  |
| 92  | DOOM™ Pinball                                         |
| 93  | Marvel's Women of Power: A-Force                      |
| 94  | Marvel's Women of Power: Champions                    |
| 95  | Jaws™ Pinball                                         |
| 96  | E.T.™ Pinball                                         |
| 97  | Back to the Future™ Pinball                           |
| 98  | Star Wars™ Pinball: Rogue One™                        |
| 100 | Jurassic Park™ Pinball                                |
| 101 | Jurassic World™ Pinball                               |
| 102 | Jurassic Park Pinball Mayhem™                         |
| 103 | Star Wars™ Pinball: The Last Jedi™                    |
| 104 | Star Wars™ Pinball: Ahch-To Island                    |
| 105 | Star Wars™ Pinball: Solo                              |
| 106 | Star Wars™ Pinball: Calrissian Chronicles             |
| 107 | Star Wars™ Pinball: Battle of Mimban                  |
| 108 | Fish Tales                                            |
| 109 | Williams™ Medieval Madness™                           |
| 110 | Williams™ JunkYard™                                   |
| 111 | Williams™ The Getaway: High Speed II™                 |
| 112 | Curse of the Mummy                                    |
| 113 | Sky Pirates: Treasures of the Clouds                  |
| 117 | Williams™ Theatre of Magic™                           |
| 118 | Williams™ Black Rose™                                 |
| 119 | Williams™ Attack from Mars™                           |
| 120 | Williams™ The Party Zone™                             |
| 121 | Williams™ The Champion Pub™                           |
| 122 | Williams™ Safe Cracker™                               |
| 123 | Pinball Noir                                          |
| 124 | Williams™ White Water™                                |
| 125 | Williams™ Red and Ted's Road Show™                    |
| 126 | Williams™ Hurricane™                                  |
| 127 | Williams™ Cirqus Voltaire™                            |
| 128 | Williams™ No Good Gofers™                             |
| 129 | Williams™ Space Station™                              |
| 130 | Williams™ Monster Bash™                               |
| 131 | Williams™ Creature from the Black Lagoon™             |
| 132 | Williams™ Tales of the Arabian Nights™                |
| 133 | Williams™ Indiana Jones™: The Pinball Adventure       |
| 134 | Williams™ FunHouse™                                   |
| 135 | Williams™ Dr. Dude and his Excellent Ray™             |
| 136 | Star Wars™ Pinball: The Mandalorian                   |
| 137 | Star Wars™ Pinball: Classic Collectibles              |
| 138 | Hasbro's MY LITTLE PONY                               |
| 139 | DreamWorks Kung Fu Panda Pinball                      |
| 140 | DreamWorks Trolls Pinball                             |
| 141 | DreamWorks How to Train Your Dragon Pinball           |
| 145 | Garfield Pinball                                      |
| 146 | Peanuts' Snoopy Pinball                               |
| 147 | Wrath of the Elder Gods                               |
| 148 | Williams™ The Machine™: Bride of Pin·Bot™             |
| 149 | Williams™ Swords of Fury™                             |
| 150 | Homeworld®: Journey to Hiigara Pinball                |
| 151 | Brothers in Arms®: Win the War Pinball                |
| 152 | Borderlands®: Vault Hunter Pinball                    |
| 153 | Kong Pinball                                          |
| 154 | World War Z Pinball                                   |
| 155 | Grimm Tales                                           |
| 156 | Williams™ The Addams Family                           |
| 157 | Williams™ World Cup Soccer                            |
| 158 | Godzilla Pinball                                      |
| 160 | Godzilla vs Kong Pinball                              |
| 161 | Crypt of the NecroDancer Pinball                      |
| 162 | Williams™ Twilight Zone                               |
| 163 | Williams™ Pinball: Star Trek™: The Next Generation    |
| 164 | Verne's Mysterious Island                             |
| 165 | A Samurai's Vengeance                                 |
| 166 | Star Trek™ Pinball: Kelvin Timeline                   |
| 167 | Xena: Warrior Princess Pinball                        |
| 168 | Williams™ Whirlwind                                   |
| 169 | Star Trek™ Pinball: Discovery                         |
| 170 | Battlestar Galactica Pinball                          |
| 172 | Star Trek™ Pinball: Deep Space Nine                   |
| 173 | Terraforming Mars Pinball                             |
| 177 | Knight Rider Pinball                                  |
| 178 | Exploding Kittens®: A Pinball Cat-astrophe            |
| 179 | Gloomhaven™ Pinball                                   |
| 181 | A Charlie Brown Christmas™ Pinball                    |
| 182 | Tomb Raider Pinball: Adventures of Lara Croft         |
| 183 | System Shock Pinball                                  |
| 184 | The Princess Bride Pinball                            |
| 186 | Pacific Rim Pinball                                   |
| 187 | Goat Simulator Pinball                                |
| 188 | Banzai Run™                                           |
| 189 | Earthshaker!™                                         |
| 190 | Black Knight™ 2000                                    |
| 191 | Camp Bloodbrook                                       |
| 192 | Tomb Raider Pinball: Secrets of Croft Manor           |
| 194 | PIN·BOT™                                              |
| 195 | WHO dunnit™                                           |
| 196 | TAXI™                                                 |
| 197 | Williams™ Pinball: Elvira and the Party Monsters      |
| 198 | Williams™ Pinball: Scared Stiff                       |
| 199 | Comet™                                                |
| 200 | Fire!™                                                |
| 201 | Diner™                                                |
| 202 | Judge Dredd™                                          |

Liste officielle : [pinballfx.com](https://www.pinballfx.com/?page_id=7754).

</details>

Version Epic Games Store : lancée avec la version **nonsteam** (dossier `emulators\pinballfx`), la table démarre, mais sans les services en ligne d'Epic (pas de classements).

## Contrôles

Le jeu gère la manette lui-même (manette XInput conseillée) : RetroBat ne change pas sa configuration. Les commandes se modifient dans les options du jeu.

<table><thead><tr><th width="310.25">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Flipper gauche</td><td>L1 ou L2</td></tr><tr><td>Flipper droit</td><td>R1 ou R2</td></tr><tr><td>Lancer la bille</td><td>Stick droit vers le bas (tirer puis relâcher)</td></tr><tr><td>Lancement automatique de la bille</td><td>SUD</td></tr><tr><td>Vue du fronton</td><td>Stick droit vers le haut</td></tr><tr><td>Bousculer la table</td><td>Stick gauche</td></tr><tr><td>Extras visuels</td><td>EST</td></tr><tr><td>Pouvoir de magicien</td><td>OUEST</td></tr><tr><td>Changer de vue</td><td>NORD</td></tr><tr><td>Menu</td><td>START ou SELECT</td></tr></tbody></table>

## Raccourcis

<table><thead><tr><th width="185.25">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Quitter le jeu</td><td>HOTKEY + START</td></tr></tbody></table>

Le Game Control Center n'est pas disponible pour ces systèmes.

## Options utiles

Dans les options avancées du système ou du jeu :

* **OPTIONS DU JEU > MODE DE JEU** : mode lancé avec la table. Sans réglage, le jeu garde le mode choisi dans son menu.

<table><thead><tr><th width="297.75">Choix</th><th>Mode de jeu</th></tr></thead><tbody><tr><td>Classique</td><td>Partie classique (<code>Classic</code>)</td></tr><tr><td>Pro</td><td>Mode Pro (<code>Pro</code>)</td></tr><tr><td>Entraînement</td><td>Entraînement (<code>Practice</code>)</td></tr><tr><td>Chacun son tour 2 / 3 / 4 joueurs</td><td>Partie à plusieurs, chacun son tour (<code>Hotseat_2</code> à <code>Hotseat_4</code>)</td></tr><tr><td>Défi 1 bille</td><td>Une seule bille (<code>Challenge_BallLimited</code>)</td></tr><tr><td>Défi 5 minutes</td><td>Partie limitée à 5 minutes (<code>Challenge_TimeLimited</code>)</td></tr><tr><td>Défi de distance</td><td>Défi de distance (<code>Challenge_DistanceLimited</code>)</td></tr><tr><td>Défi des flips</td><td>Nombre de coups de flipper limité (<code>Challenge_FlipLimited</code>)</td></tr></tbody></table>

* **VIDÉO > RÉSOLUTION DE L'ÉCRAN** : résolution de Windows pendant la partie.
* **ÉMULATION > FERMER LE LAUNCHER EN QUITTANT** : ferme Steam en quittant le jeu (version steam).

Un mode qui n'existe pas pour la table est ignoré : la table démarre avec ses réglages par défaut.

## Dossiers

<table><thead><tr><th width="310.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Tables</td><td><code>roms\pinballfx</code></td></tr><tr><td>Jeu (version nonsteam)</td><td><code>emulators\pinballfx</code></td></tr><tr><td>Sauvegardes, scores, réglages</td><td>Gérés par le jeu (et par Steam)</td></tr></tbody></table>

## Problèmes connus

* **Le jeu s'ouvre sans lancer la table** : vous ne possédez pas la table, ou son numéro est faux.
* **« '….table' must contain the table number on its first line. »** : le fichier `.table` est vide ou ne contient pas un numéro.
* **« Game not found: copy it in '…' »** (version nonsteam) : le jeu n'est pas dans le dossier indiqué, ou son exécutable porte un autre nom.
* **« Steam is not installed. »** (version steam) : Steam est introuvable.
