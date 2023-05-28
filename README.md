
# 02_Batt_Alim_4p

Module Batt_alim avec 4 pins.

<img src="media/IMG_20230522_134024.jpg" width="50%" height="50%">

Le module Batt_Alim permet de gérer la charge d'une batterie Lipo constituée d'une seule cellule (4.2V) à partir d'une source de type 5V USB.
Il permet aussi de récupérer cette tension batterie variable et de reconstituer un 5V constant grâce à un DCDC.

[La licence est celle du CERN Open Hardware Licence version 2; CERN-OHL-P ; permissive.](https://github.com/Thierry-oshw/02_Batt_Alim_4p/blob/main/LICENSE.txt)

## Schéma et fonctionnement

Ci-joint le schéma de la version de 2021_02_23 // Here schematic of version 2021_02_23:
![02_Batt_Alim](./media/schema.png "schéma du module")

Le module fonctionne de la façon suivante:
Il faut l'alimenter avec une tension 5V +-5% (typiquement celle de l'USB classique) sur la pin Vext. (Ne pas oublier GND bien sûr).

Il faut brancher la batterie Lipo sur V_bat+ et GND. La batterie Lipo doit être constituée d'une seule cellule, qui doit être chargée à 4.2V, présente une tension de 3.7V typique, et dont la tension de mise en protection est de 3V. La résistance R7 de 10kOhms permet de régler la puce TP4056 sur un courant de charge de 130mA. La batterie Lipo doit donc avoir une capacité d'au moins 2*130mAh, soit 260mAh au minimum. Plus d'information sur [www.tp4056.com](www.tp4056.com).

La sortie 5V est une tension issue du DCDC.

La LED D6 indique la présence de 5V à la sortie du DCDC, avec "5V ON" comme étiquette.

Les LEDs D2 et D3 indiquent respectivement la charge et le mode standby du TP4056. Les étiquettes sont "CHG" et "STBY".


## Fonctionnalités
- Petit (28x25.2 mm)
- Faible coût (2 couches avec composants d'un seul côté)
- Connecteur avec pas de 2.54 mm + empreinte crénelée pour connexion carte à carte

## Outils utilisés

- [Kicad V6](https://www.kicad.org/)

## Fabrication du circuit

Ce circuit a été testé de fond en comble sur de nombreux projets

## Contributeurs

- Thierry Orlandi ([Hardware Freelance](https://www.linkedin.com/in/thierry-orlandi))
- Yohann Belair ([R&D Freelance](https://github.com/ciborg971))

## Licence
[CERN Open Hardware Licence Version 2](https://github.com/Thierry-oshw/17_CAN_Controller/blob/main/LICENSE.txt)