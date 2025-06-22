# Singe

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/fb69ee3e5daf0db1c90d85d4a743edf1cc8a1843/art/logos/singe.svg" alt="" width="375"><figcaption></figcaption></figure></div>

Moteur de jeu SINGE

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>hypseus</li><li>singe2</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> singe</td></tr><tr><td><strong>Extensions</strong></td><td>.hypseus .zip</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

| Retrobat                                       | Hypseus    |
| ---------------------------------------------- | ---------- |
| START                                          | START 1    |
| SELECT                                         | COIN 1     |
| D-PAD                                          | DIRECTIONS |
| Left analog stick                              | DIRECTIONS |
| ![](<../../../.gitbook/assets/image (33).png>) | SKILL 1    |
| ![](<../../../.gitbook/assets/image (20).png>) | BUTTON 1   |
| ![](<../../../.gitbook/assets/image (7).png>)  | BUTTON 2   |
| ![](<../../../.gitbook/assets/image (35).png>) | SKILL 2    |
| L1                                             | SKILL 3    |
| R1                                             | BUTTON 3   |
| L3                                             | SERVICE    |
| R3                                             | TEST       |

## Information spécifique au système

### Ajouter des jeux SINGE (méthode zip)

Il s'agit de la méthode la plus simple pour l'ajout de jeux SINGE, tous les jeux ne sont pas encore disponibles dans ce format.

Télécharger la dernière version zip du jeu ici:\
[https://github.com/DirtBagXon/hypseus\_singe\_data/tree/master/00-zip-roms](https://github.com/DirtBagXon/hypseus_singe_data/tree/master/00-zip-roms)

Créer la structure de fichier suivante:

```
roms\
└─ singe\
   ├─ roms\
   │  └─ timegal.zip
   ├─ vldp\
      └─ timegal\
         ├─ timegal.dat
         ├─ timegal.m2v
         ├─ timegal.ogg
         └─ timegal.txt
```

Placerle fichier zip dans le dossier singe\roms.

Placer les fichiers framework et médias (non fournis) dans le sous-dossier du jeu dans le dossier vldp.

### Ajouter des jeux SINGE (ancienne méthode - dossier)

Il est également possible d'utiliser l'ancienne méthode de dossier ".daphne":

[Ajout de jeux SINGE](../arcade/daphne-laserdisc.md#ajout-de-jeux-singe-singe2-hypseus)
