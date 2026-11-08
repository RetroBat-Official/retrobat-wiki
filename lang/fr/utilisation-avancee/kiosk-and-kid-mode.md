# Mode Kiosque et Enfant

RetroBat (EmulationStation) propose trois **modes d'interface** :

<table><thead><tr><th width="104.5">Mode</th><th width="216">Pour</th><th>Effet</th></tr></thead><tbody><tr><td><strong>Complet</strong></td><td>Vous (par défaut)</td><td>Tout est accessible.</td></tr><tr><td><strong>Kiosque</strong></td><td>Invités, bornes d'arcade</td><td>Tous les jeux sont jouables, mais les paramètres, les métadonnées, les collections et la suppression de jeux sont verrouillés. Les jeux cachés restent cachés.</td></tr><tr><td><strong>Enfant</strong></td><td>Enfants</td><td>Mêmes verrous que Kiosque, et <strong>seuls les jeux marqués « Jeu enfant »</strong> sont affichés. Les favoris ne peuvent pas être modifiés.</td></tr></tbody></table>

## Avant de passer en mode Enfant : marquer les jeux

Le mode Enfant n'affiche que les jeux dont la métadonnée **Jeu enfant** est activée. À faire tant que vous êtes en mode **Complet** :

1. Dans une liste de jeux, sélectionnez le jeu et ouvrez le menu [**OPTIONS DU JEU**](../navigation/game-options.md).
2. Choisissez **ÉDITER LES MÉTADONNÉES DU JEU**.
3. Activez **Jeu enfant**, puis enregistrez.

<div align="left"><figure><img src="../.gitbook/assets/image (415).png" alt=""><figcaption></figcaption></figure></div>

> **Astuce :** vous pouvez aussi ajouter `<kidgame>true</kidgame>` aux jeux dans le `gamelist.xml` du système (EmulationStation fermé).

Si aucun jeu n'est marqué, le mode Enfant n'a rien à afficher, et EmulationStation revient automatiquement en mode **Complet**.

## Passer en mode Kiosque ou Enfant

1. Ouvrez le **MENU PRINCIPAL** (START) > **PARAMÈTRES SYSTÈME**.

<div align="left"><figure><img src="../.gitbook/assets/image (416).png" alt=""><figcaption></figcaption></figure></div>

2. Réglez **RESTRICTIONS DE L'INTERFACE** sur **Kiosque** ou **Enfant**.

<div align="left"><figure><img src="../.gitbook/assets/image (417).png" alt=""><figcaption></figcaption></figure></div>

3. Fermez le menu. Un message affiche le **code de déverrouillage**. Notez-le, puis confirmez avec **OUI**.

<div align="left"><figure><img src="../.gitbook/assets/image (418).png" alt=""><figcaption></figcaption></figure></div>

## Ce qui est verrouillé

<table><thead><tr><th width="524.5"></th><th align="center">Kiosque</th><th align="center">Enfant</th></tr></thead><tbody><tr><td>Menu principal réduit à RETROACHIEVEMENTS, INFORMATIONS, DÉVERROUILLER L'INTERFACE et QUITTER</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Options du jeu : pas d'édition des métadonnées, pas de collections, pas de suppression</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Filtres et options des listes de jeux réduits</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Systèmes et collections vides masqués</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Éditeur PadToKey en lecture seule</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Jeux cachés jamais affichés</td><td align="center">✔</td><td align="center"></td></tr><tr><td>Seuls les jeux « Jeu enfant » affichés</td><td align="center"></td><td align="center">✔</td></tr><tr><td>Options SELECT et raccourci favoris désactivés</td><td align="center"></td><td align="center">✔</td></tr><tr><td>Aide « MENU » masquée (START ouvre toujours le menu réduit)</td><td align="center"></td><td align="center">✔</td></tr></tbody></table>

Les sauvegardes d'état restent accessibles dans les deux modes.

<div align="left"><figure><img src="../.gitbook/assets/image (419).png" alt=""><figcaption><p>Le menu principal en mode enfant</p></figcaption></figure></div>

## Revenir en mode Complet

1. Ouvrez le **MENU PRINCIPAL** (START) > **DÉVERROUILLER L'INTERFACE**.
2. Quand **SAISIR LE CODE DE DÉVERROUILLAGE** s'affiche, appuyez sur les boutons du code l'un après l'autre.

<div align="left"><figure><img src="../.gitbook/assets/image (420).png" alt=""><figcaption></figcaption></figure></div>

Le code par défaut est **A, A, A, B, A**. Les lettres désignent la **position des boutons**, pas les lettres imprimées :

| Code | Position         | Xbox | PlayStation | Nintendo |
| ---- | ---------------- | ---- | ----------- | -------- |
| A    | bouton du bas    | A    | ✕           | B        |
| B    | bouton de droite | B    | ○           | A        |

Le code est donc **A A A B A** sur une manette Xbox, **✕ ✕ ✕ ○ ✕** sur une manette PlayStation et **B B B A B** sur une manette Nintendo.

## Changer le code de déverrouillage (avancé)

1. Fermez EmulationStation.
2. Ouvrez `emulationstation\.emulationstation\es_settings.cfg`.
3. Ajoutez cette ligne avant `</config>` (elle n'existe pas dans le fichier tant que le code par défaut est utilisé) :

```xml
<string name="UIMode_passkey" value="aaaba" />
```

4. Remplacez `aaaba` par votre séquence, avec `a` (bouton du bas) et `b` (bouton de droite), puis relancez RetroBat.

> **Remarque :** si vous appuyez sur un mauvais bouton pendant la saisie du code, recommencez la séquence depuis le début.

## Forcer le mode avec retrobat.ini

Pour verrouiller durablement une borne ou un poste pour enfants, réglez le mode dans `retrobat.ini` (dossier racine de RetroBat), section `[EmulationStation]` :

```ini
[EmulationStation]
InterfaceMode=2
```

<table><thead><tr><th width="114">Valeur</th><th>Mode</th></tr></thead><tbody><tr><td>0</td><td>Normal (utilise le réglage RESTRICTIONS DE L'INTERFACE)</td></tr><tr><td>1</td><td>Kiosque</td></tr><tr><td>2</td><td>Enfant</td></tr></tbody></table>

> **Attention :** quand `InterfaceMode` vaut 1 ou 2, le mode est **forcé à chaque démarrage**, et le code de déverrouillage est sans effet. Pour revenir en mode Complet, fermez RetroBat et remettez `InterfaceMode=0`.
