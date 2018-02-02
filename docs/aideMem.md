# Aide mémoire pour Arduino
La programmation _Arduino_ est proche de la programmation _C/C++_, tout simplement parce que le langage _Arduino_ est [basé](https://www.arduino.cc/en/Main/FAQ#toc13) sur du _C/C++_. Les quelques [variations](https://arduino.stackexchange.com/questions/816/c-vs-the-arduino-language) résident majoritairement dans le fait que _Arduino_ ajoute ses propres [librairies](https://www.arduino.cc/reference/en/) pour le contrôle de son circuit imprimé. 
## Déclarer une variable
Avant d'utiliser une variable, il faut la déclarer :
```Arduino
String nom = "valeur";
int LED = 13;
```
La valeur est optionelle et peut être définie plus tard :
```Arduino
String test;
test = "TATA";
```
Il est intéressant de noter qu'_Arduino_ a sa propre [implémentation](https://www.arduino.cc/reference/en/language/variables/data-types/stringobject/) des `String`, ce qui peut poser problème en utilisant les `string` implémentées dans _C++_.
## Créer une fonction
La création de fonctions en _Arduino_ est pareil qu'en C/C++. Il faut préciser le Type que retourne la fonction ( `int`, `String`, `void`... ). le type `void` indique que la fonction ne retourne rien :
```Arduino
void foo(int parametre){
    //l'interieur de votre fonction
    parametre = 14;
}
```
La fonction présentée ci-dessus est appelée lorsque l'on exécute :
```Arduino
int test = 1;
foo(test); // test = 14
```
## Aspect général d'un code
```Arduino
//Declaration de variables globales
int variable_globale = 1;
//Initialisation des parametres (Entree/Sortie)
void setup() {
    //Faire quelque chose une fois
    variable_globale = 2;
}
//Le code qui sera execute en boucle
void loop() {
    //le code qui sera repete
    variable_globale += 1;
    variable_globale -= 1;
}
```
## Les spécificités Arduino
Le langage _Arduino_ permet d'utiliser plus facilement un circuit imprimé grâce a ses fonctions spécifiques :

Déclaration de l'utilisation d'une broche :
```Arduino
int broche = 13;
pinMode(broche, OUTPUT); // declarer la broche 13 comme sortie (OUTPUT)
```
Changer le voltage d'une broche :
```Arduino
int broche = 13;
digitalWrite(broche, HIGH); // fournir un courant de 5V dans la broche 13
digitalWrite(broche, LOW); // le courant passe a 0V dans la broche 13
```
Marquer un temps d'arrêt dans l'exécution du code :
```Arduino
delay(1000); // stoppe l'execution du code pendant 1 seconde
```