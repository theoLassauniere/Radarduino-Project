# Séance n°7

Lors de cette séance, mon principal objectif est de coder les pièces ensembles pour enfin mesurer la vitesse d'un objet.

Pour ce faire, une idée m'est venue.

Je n'arrêtai pas de tomber sur des vidéos de radars improvisés en arduino qui calculaient tous la vitesse à l'aide de 2 capteurs. Nommons les capteurs A et B.
Lorsque l'objet passe devant le capteur A, on mesure un temps, et même chose quand celui ci passe devant un capteur B. Connaisant la distance entre les deux capteurs, 
il ne reste plus qu'à soustraire temps(B) - temps(A) et de diviser la distance avec cette valeur pour obtenir la vitesse.
Cela est tellement pkus simple.

Comme nous ne possédons qu'un seul capteur, je pensais qu'il fallait nécessairement 'tracker' l'objet et mesurer sa distance par rapport au capteur à certains points
du temps pour obtenir sa vitesse.

Quand l'idée m'est venue de faire de mon capteur à a fois le capteur A et à la fois le capteur B.

L'idée est de calibrer le capteur sur la position A et de mesurer la distance en continu. Quand l'objet passe, la disatnce mesurée se réduit considérablement.
Le capteur pivote donc grâce au servomoteur dans la position B, et l'objet "recoupe" le laser du capteur (bien sûr, il faut que le servomoteur aille assez vite...)

Il ne reste plus qu'à enregistrer le temps en A et en B, et connaissant approximativement la distance de coupe de l'objet (ici, points rouges), on peut en déduire sa
vitesse.

Schéma de fonctionnement du radar :

<img src="https://user-images.githubusercontent.com/120557548/219400028-538490d0-85b0-4375-b212-c9aa7b86ac75.jpg">

En début de, séance, je prends donc le servomoteur plus en main et essaye de trouver l'angle le plus judicieux entre vitesse et précision. Pour l'instant, le capteur est
simplement fixé avec du scotch double face au servomoteur.

Test du servomoteur : 

<img src="https://user-images.githubusercontent.com/120557548/219400531-3b201f50-9d93-4bd7-95b1-9ab14fbb87b1.jpg" width=30% heigth=30%>

80° d'angle entre les 2 mesures semble bien convenir.
Enfin, je branche également le capteur pour le faire fonctionner avec le servomoteur.
Image du branchement :


<img src="https://user-images.githubusercontent.com/120557548/219401705-3ffc9173-f309-4b49-a1e0-4436cff7ebaa.jpg" width=30% heigth=30%>

Je tente de formuler un code à partir des codes de tests du capteur et du servomoteur, et ça commence à rendre plutôt bien.
Ici, j'ai programmé le fait que le capteur se calibre sur la position A, et dès qu'il me détecte quand je passe devant, il se tourne en position B.
Seulement, la rotation est un peu étrange... arrivé au bout, le capteur fait des rotaions successives à droites et à gauche sans s'arrêter, à voir comment corriger ça
la prochaine fois.

Code arduino :
[Code_projet.zip](https://github.com/Younisse/Radarduino/files/10757311/Code_projet.zip)

