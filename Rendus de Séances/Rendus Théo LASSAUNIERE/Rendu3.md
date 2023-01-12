# Séance n°3 :

### Début de Séance : 

L'objectif est de prendre en main notre capteur Lidar-Lite v3hp pour le tester et le programmer. Je commence donc par me renseigner sur sa documentation pour voir 
comment ce capteur doit se brancher.

Cependant, je remarque que 2 fils sont coupés à l'extrémité. Cela me semble bizzare. J'en discute avec notre professeur (Xavier) et ce dernier va me souder les fils qui me
manquent ( les fils du protocole I2C).

Mes fils soudés et le montage fait, je me rends dans Arduino pour télécharger la librairie Lidar-Lite, qui pourra me fournir un code d'exemple pour mon capteur.
Cependant, une fois le téléversement terminé, rien ne s'affiche sur le moniteur série.

Après avoir observé mon montage, je me rends compte que j'avais intervertis les 2 fils sda et sdl. Ayant bon espoir, je retente de téléverser mon code dans le capteur.
Montage Final: 

<img src="https://user-images.githubusercontent.com/120557548/212120465-9298152c-0b8f-41f3-a80b-a5f5bb3f47b0.jpg" width : 30% heigth : 30%>



Rien ne se passe.

J'appelle donc un professeur pour qu'il vienne à ma rescousse. Tout d'abord, le problème me semblait bénin (cela devait être un mauvais montage, un faux contact)
Mais plus le professeur se penchait sur le problème, moins celui-ci avait l'air minime. Celui-ci nopus a pris en effet la séance entière pour le résoudre.

avec des Serial.println("test") dans notre code bien placé, nous avons réalisé que le capteur ne s'initialisait pas.
