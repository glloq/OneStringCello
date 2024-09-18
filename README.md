# OneStringCello
l'idée est de faire un systeme qui viend jouer d'un instrument a corde frotée de type violon, violoncelle, etc.

l'objectif est de faire un test de plusieurs techniques pour jouer sur un instrument a une corde afin d'avoir une base adaptable jusqu'a 4 cordes dans l'avenir

## les choix techniques pour les accords

### servommoteurs
en utilisant un pca9685 nous pouvons facilement controller 16 servomoteurs

### solenoides
avec un mpc23017 et deuxs uln2803, nous pouvons controller 16 solenoides (500mA par solenoides max) 

### moteurs pas a pas
avec un driver et un moteur pas a pas, on peut faire un reglage des positions via software.

## les choix techniques pour l'archet

- une roue qui entoure la caisse de resonance ou qui y est abaissé contre la corde a la reception d'une noteOn
- une roue de plus petite au dessus de la corde qui est plus facile a mettre en place 
- un systeme de corde fermée
- un archet directement controlé (beaucoup plus encombrant)


# la position des frettes

Pour déterminer les positions des frettes sur une corde d'un violoncelle en fonction de sa longueur, nous utilisons la règle des frettes, qui suit une division logarithmique. La position de chaque frette est calculée en utilisant la formule suivante :
 
d_n = L - (L / (2 ^ (n / 12)))

ou:
- `d_n` est la distance entre le sillet et la n-ième frette,
- `L` est la longueur vibrante de la corde (du sillet au chevalet),
- `n` est le numéro de la frette.

## Longueurs des Cordes Vibrantes pour Instruments à Cordes Frottées

| Instrument         | Longueur de corde vibrante (en mm) |
|--------------------|------------------------------------|
| Violon             | 325 - 330 mm                       |
| Alto               | 370 - 380 mm                       |
| Viole d'amour      | 400 - 450 mm                       |
| Nyckelharpa        | 400 - 450 mm                       |
| Violoncelle        | 680 - 700 mm                       |
| Viole de gambe     | 700 - 750 mm                       |
| Contrebasse        | 1040 - 1060 mm                     |

