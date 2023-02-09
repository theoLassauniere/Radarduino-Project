# Séance 6

Aujourdh'hui, nous avons reçu notre capteur définitif pour notre projet. Il s'agit du Lidar-lite v3. Etant neuf, il a bien fonctionné pour le code de test, celui
affichant la distance en cm sur le moniteur série, à l'aide du bus I2C.

Maintenant, à partir de cette distance, il faut calculer une vitesse. J'ai commencé à formuler un début de code, mais celui-ci à tendance à mesurer des vitesses trop
faussées réalistiquement parlant (certaines de l'ordre de 1000m/s). il faudra donc voir comment améliorer ce code.

Maintenant, il faut commencer à afficher les données sur notre écran. 
**Problème** : notre écran ne marche plus... (décidemment)

De plus, il n'en apparait plus de disponible pour la même référence. Donc soit on opte pour un écran plus grand, soit on récolte et affiche les données sur l'ordinateur
(à l'aide de python par exemple).

Le problème avec l'écran plus grand est qu'il faudra réimprimer certaines pièces de notre squelette, celui ci ayant partiellement été imprimé entre temps (grâce à mon binôme).

L'objectif principal des séances à suivre concernera donc principalement la partie code pour ma part.

Image du Capteur :

<img src="https://user-images.githubusercontent.com/120557548/217836961-c365bb8a-a8f9-49ad-bb84-ea3f1bec4975.jpg" width = 30% heigth = 30%>



[Codes séance 6.zip](https://github.com/Younisse/Radarduino/files/10698021/Codes.seance.6.zip)
