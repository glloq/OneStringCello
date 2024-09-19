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
on a deux facons de faire : avec un doigt toujour en appui ou avec un systeme mecanique ou electromecanique pour lever le doigt.

## Types d'archets et méthodes de mise en vibration des cordes

| Type d'archet ou méthode         | Avantages                                               | Inconvénients                                             |
|----------------------------------|---------------------------------------------------------|-----------------------------------------------------------|
| **Archet classique (poils naturels ou synthétiques)** | - Son riche et expressif<br>- Contrôle dynamique fin     | - Complexe à motoriser pour un mouvement fluide            |
| **Roue de friction (style vielle à roue)**  | - Son continu<br>- Simple à motoriser                    | - Moins de contrôle sur les nuances dynamiques             |
| **Archet rotatif**               | - Facile à automatiser<br>- Action régulière             | - Moins flexible pour les variations d’intensité           |
| **Ficelle ou bande en plastique rotative** | - Facile à motoriser<br>- Produit un son continu         | - Moins de contrôle fin sur la dynamique                   |
| **Disque en caoutchouc ou plastique rotatif** | - Bonne adhérence<br>- Son continu                       | - Qualité sonore moins raffinée que l’archet classique      |
| **Archet électromagnétique (excitation magnétique)** | - Pas de contact physique<br>- Contrôle précis des fréquences et amplitude | - Nécessite une corde métallique<br>- Complexité électronique |



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

## Comparaison des Types de Cordes

| Type de corde       | Avantages                                                | Inconvénients                                             |
|---------------------|----------------------------------------------------------|-----------------------------------------------------------|
| **Métal (acier, nickel)**  | - Son clair et puissant<br>- Durabilité élevée<br>- Stabilité sous tension | - Rigidité plus élevée<br>- Moins de chaleur dans le son  |
| **Boyau (gut)**     | - Sonorité chaude et riche<br>- Tension plus basse (plus facile à manipuler) | - Moins durable<br>- Sensible à l'humidité et à la température |
| **Synthétique (nylon, Perlon)** | - Sonorité équilibrée<br>- Stable dans différentes conditions climatiques | - Moins de brillance comparée au métal                     |
| **Carbone**         | - Très durable<br>- Bonne projection sonore               | - Plus rigide<br>- Plus cher                               |
