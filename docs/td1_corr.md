# TD1 : Initiation à Arduino:
## **Partie 1 : Allumage d'une LED** 

**Mise en place de l'initialisation**

1. Déclarer une variable globale correspondant à la LED.
```Arduino
int LED1=13;

void setup(){
}

void loop(){
}
```
2. Attribuer cette LED comme sortie.

```Arduino
int LED1=13;

void setup(){
    pinMode(LED1,OUTPUT);
}
void loop(){

}
```
**Mise en place de la boucle principale**

1. Provoquer l'allumage de la LED.

```Arduino
int LED1=13;

void setup() {
    pinMode(LED1,OUTPUT);
}

void loop() {
    digitalWrite(LED1,HIGH);
}
```
2. Marquer un temps d'arrêt dans l'execution du programme.
```Arduino
int LED1=13;

void setup() {
    pinMode(LED1,OUTPUT);
}

void loop() {
    digitalWrite(LED1,HIGH);
    delay(500);
}
```
3. Demander l'extinction de la LED.
```Arduino
int LED1=13;

void setup() {
    pinMode(LED1,OUTPUT);
}

void loop() {
    digitalWrite(LED1,HIGH);
    delay(500);
    digitalWrite(LED1,LOW);
    delay(500);
}
```
**Pour aller plus loin**
```Arduino
int LED1=13;

void blinkS(int LED){
    for(int i=0;i<3;i++){
        digitalWrite(LED,HIGH);
        delay(250);
        digitalWrite(LED,LOW);
        delay(250);
    }
}
void blinkO(int LED){
    for(int i=0;i<3;i++){
        digitalWrite(LED,HIGH);
        delay(500);
        digitalWrite(LED,LOW);
        delay(500);
    }
}

void setup() {
    pinMode(LED1,OUTPUT);
}

void loop() {
    blinkS(LED1);
    delay(500);
    blinkO(LED1);
    delay(500);
    blinkS(LED1);
    delay(500);
}
```
## **Partie 2 : Allumage de plusieurs LEDs**
1. Déclarer les nouvelles LEDs.
```Arduino
int LED1=13;
int LED2=12;
int LED3=11;

void setup() {
}

void loop() {

}
```
2. Modifier la fonction setup() afin de l'adapter à ce changement.

```Arduino
int LED1=13;
int LED2=12;
int LED3=11;


void setup() {
    pinMode(LED1,OUTPUT);
    pinMode(LED2,OUTPUT);
    pinMode(LED3,OUTPUT);
}

void loop() {

}
```
3. Modifier la fonction loop() afin de faire clignoter les LEDs une à une.


```Arduino
int LED1=13;
int LED2=12;
int LED3=11;


void setup() {
    pinMode(LED1,OUTPUT);
    pinMode(LED2,OUTPUT);
    pinMode(LED3,OUTPUT);
}

void loop() {
    // LED 1
    digitalWrite(LED1,HIGH);
    delay(500);
    digitalWrite(LED1,LOW);
    // LED 2
    digitalWrite(LED2,HIGH);
    delay(500);
    digitalWrite(LED2,LOW);
    // LED 3
    digitalWrite(LED3,HIGH);
    delay(500);
    digitalWrite(LED3,LOW);
}
```

Pour aller plus loin

```Arduino
int LED1=13;
int LED2=12;
int LED3=11;

void blinkS(int LED){
    for(int i=0;i<3;i++){
        digitalWrite(LED,HIGH);
        delay(250);
        digitalWrite(LED,LOW);
        delay(250);
    }
}
void blinkO(int LED){
    for(int i=0;i<3;i++){
        digitalWrite(LED,HIGH);
        delay(500);
        digitalWrite(LED,LOW);
        delay(500);
    }
}


void setup() {
    pinMode(LED1,OUTPUT);
    pinMode(LED2,OUTPUT);
    pinMode(LED3,OUTPUT);
}

void loop() {
    blinkS(LED1);
    delay(500);
    blinkO(LED2);
    delay(500);
    blinkS(LED3);
    delay(500);
}
```