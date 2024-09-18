# OneStringCello
l'idée est de faire un systeme qui viend jouer d'un instrument a corde frotée de type violon, violoncelle, etc.

l'objectif est de faire un test de plusieurs techniques pour jouer sur un instrument a corde

## les choix techniques pour les accords

### servommoteurs
en utilisant un pca9685 nous pouvons facilement controller 16 servomoteurs

### solenoides
avec un mpc23017 et deuxs uln2803, nous pouvons controller 16 solenoides (500mA par solenoides max) 

### moteurs pas a pas
avec un driver et un moteur pas a pas, on peut faire un reglage des positions via software.

## les choix techniques pour l'archet

une roue qui entoure la caisse de resonance ou qui y est abaissé contre la corde a la reception d'une noteOn

une roue de plus petite qui est plus facile a mettre en place 


