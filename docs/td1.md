# TD1 : Initiation à Arduino
Pour compléter sans soucis ce TD, nous vous conseillons de vous munir des [diapos](https://rawgit.com/Anthagonas/arduino/master/docs/diapos.pdf) et des aides mémoire pour coder du [C/C++](https://rawgit.com/Anthagonas/arduino/master/docs/aideC.pdf) dans [Arduino](https://rawgit.com/Anthagonas/arduino/master/docs/aideArd.pdf).

Créez un fichier `led.c` dans lequel vous écrirez le code.
## Allumage d'une LED
Le but içi sera de faire clignotter une LED à intervalles précises. Cette LED est positionnée sur le port _13_ de la carte Arduino.

Voici un schéma récapitulatif de la carte Arduino :
**_INSERER SCHEMA_**

### Mise en place du setup
Pour faire clignotter la LED il faut d'abord indiquer à Arduino quelles sont les entrée/sorties utilisées par le programme.
Pour cela il faut :
1. Déclarer une variable globale correspondant a la LED.
1. Attribuer cette LED comme sortie.
### Mise en place de la boucle principale
Une fois les entrées/sorties définies, il faut déterminer le comportement général des éléments connectés à la carte Arduino. Nous désirons içi faire clignotter notre LED déclarée précédemment.
Pour faire clignotter la LED :
1. Provoquer l'allumage de la LED.
1. Marquer un temps d'arrêt dans l'execution du programme.
    _(Voir le fonctionnement de la fonction `delay()`)_
1. Demander l'extinction de la LED.

_**Note** : La fonction `loop()` se comporte comme une boucle, penser a marquer un temps d'arret supplémentaire entre l'extinction et l'allumage de la LED._

### Pour aller plus loin
Si vous vous sentez motivé, tentez de créer un signal S.O.S avec votre LED !
Pour cela :
1. Créer une fonction `blinkS()` qui fait clignotter votre LED 3 fois lentement. _(correspondant à la lettre S en morse)_
1. Créer une fonction `blinkO()` faisant clignotter 3 fois votre LED rapidement. _(correspondant à la lettre O en morse)_
1. Utiliser les fonction `blinkS()` et `blinkO()` dans la fonction `loop()` afin de créer un S.O.S

_**Note** : Il est nécessaire de marquer un temps d'arrêt entre chaque lettre en morse._

## Allumage de plusieurs LEDs
Dans cette partie, la carte Arduino a été modifiée afin d'accueillir 3 LEDs au lieux d'une. Les LEDs sont placées aux ports _11_,_12_ et _13_.
Voici un schéma de la nouvelle configuration :
**_INSERER SCHEMA_** 
Modifier le code précédent afin de :
1. Déclarer les nouvelles LEDs.
1. Modifier la fonction `setup()` afin de l'adapter à ce changement.
1. Modifier la fonction `loop()` afin de faire clignotter les LEDs une à une.

_**Note** : Si vous avez implémenté les fonctions `blinkO()` et `blinkS()`, vous pouvez tenter de faire correspondre chaque lettre du message S.O.S à une LED.
(On aura alors la première LED clignottant "S", puis la deuxième "O", puis la troisième "S")_