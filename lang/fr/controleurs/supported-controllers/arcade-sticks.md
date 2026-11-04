# 🕹️ Sticks Arcade

Les sticks arcade (fight sticks, hitbox, panels arcade avec encodeur USB) sont gérés comme des manettes dans RetroBat. En plus, RetroBat peut reproduire sur votre stick la **disposition des boutons de la borne d'origine**, grâce à l'option **DISPOSITION DES BOUTONS**.

## Choisir le bon mode sur votre stick

La plupart des sticks récents ont un sélecteur de mode ou une combinaison de boutons (voir la notice de votre stick) : **XInput / PC / X**, **DirectInput / D**, **PlayStation / PS**, **Switch / NS**…

{% hint style="success" %}
**Utilisez le mode XInput dès que votre stick le propose.** Le stick est alors reconnu comme une manette Xbox standard : il est configuré automatiquement, et ses boutons correspondent aux dispositions décrites ci-dessous sans aucun réglage.
{% endhint %}

<table><thead><tr><th width="240.25">Mode</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>XInput</strong> (recommandé)</td><td>Configuration automatique. Les 8 boutons sont A, B, X, Y, LB, RB, LT, RT.</td></tr><tr><td><strong>PlayStation / Switch</strong></td><td>Fonctionne aussi (les boutons sont gérés par position), mais XInput reste le plus simple.</td></tr><tr><td><strong>DirectInput</strong> (encodeurs USB génériques, Zero Delay…)</td><td>Doit être configuré une fois dans <strong>MENU PRINCIPAL > PARAMÈTRES DES MANETTES > CONFIGURER UNE MANETTE</strong>. Configurez les boutons selon la disposition de référence ci-dessous, pour que les dispositions fonctionnent correctement.</td></tr></tbody></table>

**Levier** : si votre stick a un sélecteur **DP / LS / RS**, laissez-le sur **DP** (croix directionnelle). N'utilisez **LS** (stick gauche) que pour les jeux qui demandent une commande analogique.

### Configurer un stick DirectInput

Dans **CONFIGURER UNE MANETTE**, configurez les boutons par position, comme sur un panel « moderne » 8 boutons :

|                    | Bouton 1 | Bouton 2 | Bouton 3 | Bouton 4 |
| ------------------ | -------- | -------- | -------- | -------- |
| **Rangée du haut** | OUEST    | NORD     | R1       | L1       |
| **Rangée du bas**  | SUD      | EST      | R2       | L2       |

Configurez aussi **START**, **SELECT** (utilisé comme Coin) et **RACCOURCI** (en général le même bouton que SELECT).

## Choisir la disposition (DISPOSITION DES BOUTONS)

L'option **DISPOSITION DES BOUTONS** se trouve dans la configuration avancée du système (ou du jeu) > **CONTRÔLES**. Elle indique à RetroBat comment sont disposés les boutons de votre stick, pour que chaque jeu utilise les mêmes boutons que sur la borne d'origine.

Les schémas ci-dessous indiquent les boutons tels qu'ils sont nommés en **XInput** (équivalent PlayStation : X = □, Y = △, A = ✕, B = ○, LB/RB = L1/R1, LT/RT = L2/R2).

| Valeur                          | Rangée du haut  | Rangée du bas   | Pour                                                                             |
| ------------------------------- | --------------- | --------------- | -------------------------------------------------------------------------------- |
| **MANETTE (SNES)** (par défaut) | –               | –               | Manettes : le mappage est pensé pour une manette.                                |
| **MODERNE 8 BOUTONS**           | X · Y · RB · LB | A · B · RT · LT | La plupart des fight sticks et hitbox (Hori, Qanba, Mayflash, 8BitDo, Victrix…). |
| **8 BOUTONS ALTERNATIF**        | X · Y · LB · LT | A · B · RB · RT | Panels dont les 3e et 4e colonnes sont LB/RB et LT/RT.                           |
| **6 BOUTONS**                   | X · Y · LB      | A · B · RB      | Panels 6 boutons (type Astro City).                                              |
| **CLASSIQUE 8 BOUTONS**         | X · Y · LB      | A · B · RB      | Utilise actuellement la disposition 6 BOUTONS.                                   |

{% hint style="info" %}
Pour trouver votre disposition, regardez les inscriptions sur votre stick (ou appuyez sur chaque bouton dans **Configurer les contrôleurs de jeu USB** de Windows, `joy.cpl`), puis choisissez la ligne qui correspond à ce qu'envoient vos rangées du haut et du bas.
{% endhint %}

Exemples (MODERNE 8 BOUTONS) :

* **Jeu à 3 boutons** (ex. Golden Axe) : boutons 1-2-3 sur la rangée du haut.
* **Jeu à 6 boutons** (ex. Street Fighter II) : les poings sur la rangée du haut, les pieds sur la rangée du bas, comme sur la borne d'origine.

### Émulateurs compatibles avec les dispositions

<table><thead><tr><th width="349">Émulateur</th><th>Jeux</th></tr></thead><tbody><tr><td><strong>MAME</strong> (standalone, HBMAME, GroovyMAME)</td><td>Tous les jeux, avec la disposition exacte de la borne pour les jeux fournis par RetroBat.</td></tr><tr><td>Core <strong>RetroArch - MAME</strong></td><td>Tous les jeux, avec la disposition exacte de la borne pour les jeux fournis par RetroBat.</td></tr><tr><td>Cores <strong>RetroArch - Flycast</strong> et <strong>Supermodel</strong></td><td>Jeux présents dans les fichiers de mappage.</td></tr><tr><td><strong>FBNeo</strong> (standalone)</td><td>Jeux présents dans le fichier de mappage.</td></tr><tr><td><strong>Flycast</strong> (standalone, Naomi / Atomiswave)</td><td>Jeux présents dans le fichier de mappage.</td></tr><tr><td><strong>Supermodel</strong> (Model 3)</td><td>Jeux présents dans le fichier de mappage.</td></tr><tr><td><strong>TeknoParrot</strong></td><td>Jeux présents dans le fichier de mappage.</td></tr><tr><td><strong>Lindbergh</strong> (linuxloader)</td><td>Tous les jeux.</td></tr><tr><td><strong>PCSX2x6</strong> (Namco System 246/256)</td><td>Tous les jeux.</td></tr><tr><td><strong>ArcadeDuck</strong> (Zinc)</td><td>Tous les jeux, avec des dispositions propres au jeu quand elles existent.</td></tr></tbody></table>

Les jeux non listés utilisent le mappage standard de RetroBat. Vous pouvez ajouter ou modifier des dispositions par jeu dans `user\inputmapping` : voir la page [Mappage des contrôles spécifiques aux émulateurs](../configuration-des-touches-specifique-par-emulateur/).

## Boutons arcade

| Fonction        | Stick             | Clavier   |
| --------------- | ----------------- | --------- |
| Start (J1 / J2) | START             | `1` / `2` |
| Coin (J1 / J2)  | SELECT            | `5` / `6` |
| Test            | R3                | `0`       |
| Service         | L3                | `9`       |
| Quitter le jeu  | RACCOURCI + START | `Échap`   |

{% hint style="info" %}
La plupart des sticks n'ont pas de boutons L3/R3 : utilisez les touches `9` / `0` du clavier pour ouvrir les menus opérateur (Test / Service), ou le sélecteur L3/R3 de votre stick s'il en a un.
{% endhint %}

Voir le [Guide Arcade](../../systemes-and-emulateurs/arcade-guide.md) pour plus de détails sur les contrôles arcade et les romsets.

## Sticks reconnus comme un clavier (I-PAC2, X-Arcade Tankstick)

Certains sticks et encodeurs sont vus par Windows comme un **clavier**. RetroBat fournit des configurations prêtes à l'emploi :

* **RetroArch** : **PARAMÈTRES DES JEUX > OPTIONS RETROARCH > CONTRÔLES > CONFIGURER LES STICKS ARCADE DE TYPE CLAVIER**.
* **MAME** : configuration avancée du système > CONTRÔLES > **PROFIL DE CONFIGURATION DES MANETTES** (IPAC2 ou X-ARCADE).
* **PCSX2x6** : configuration avancée du système > CONTRÔLES > **CONFIGURER LES STICKS ARCADE DE TYPE CLAVIER**.

Tous les détails sont sur la page [Contrôleurs spéciaux](gamepads/controleurs-speciaux.md#sticks-arcade-reconnus-comme-un-clavier-i-pac2-x-arcade-tankstick).

{% hint style="info" %}
Si votre encodeur peut fonctionner comme une manette (XInput), préférez ce mode : le stick profite alors de la configuration automatique et des dispositions ci-dessus.
{% endhint %}

## Mappage personnalisé d'un stick (RetroArch)

Pour un stick reconnu comme une manette, vous pouvez aussi forcer un mappage RetroArch dédié avec le fichier `arcade_sticks.json` et l'option **UTILISER UN MAPPING PERSO POUR LES STICKS ARCADE** : voir la page [Contrôleurs spéciaux](gamepads/controleurs-speciaux.md#mappage-personnalise-des-sticks-arcade-retroarch).
