# Séance n°3 :

L'objectif est de prendre en main notre capteur Lidar-Lite v3hp pour le tester et le programmer. Je commence donc par me renseigner sur sa documentation pour voir 
comment ce capteur doit se brancher.

Cependant, je remarque que 2 fils sont coupés à l'extrémité. Cela me semble bizzare. J'en discute avec notre professeur (Xavier) et ce dernier va me souder les fils qui me
manquent ( les fils du protocole I2C).

Mes fils soudés et le montage fait, je me rends dans Arduino pour télécharger la librairie Lidar-Lite, qui pourra me fournir un code d'exemple pour mon capteur.
Cependant, une fois le téléversement terminé, rien ne s'affiche sur le moniteur série.

Après avoir observé mon montage, je me rends compte que j'avais intervertis les 2 fils sda et sdl. Ayant bon espoir, je retente de téléverser mon code dans le capteur.
Montage Final: 



<img src="https://user-images.githubusercontent.com/120557548/212122825-50c953c3-f277-41c7-a54f-eb792a8bb9f5.jpg" width = 30% heigth = 30%>

Rien ne se passe.

J'appelle donc un professeur pour qu'il vienne à ma rescousse. Tout d'abord, le problème me semblait bénin (cela devait être un mauvais montage, un faux contact)
Mais plus le professeur se penchait sur le problème, moins celui-ci avait l'air minime. Celui-ci nopus a pris en effet la séance entière pour le résoudre.

Avec des Serial.println("test") dans notre code bien placé, nous avons réalisé que le capteur ne s'initialisait pas.
Mr Xavier essaye donc de débuguer le .cpp de la librairie pour voir où l'initialisation plante.

Et en effet, elle plante bout de 3 tests sur 7, révélant un problème de type Wire.write.
Après avoir mesuré les tensions aux bornes de nos composants, il s'avère tout simplement que les fils du protocole I2C du Capteur sont HS. On a comparé avec un capteur de couleur utilisé en TP et celui-ci marchait très bien dans notre montage.

Etude du montage à l'oscilloscope : 


<img src="https://user-images.githubusercontent.com/120557548/212121577-bbcbbf8a-f77f-487e-847d-eb2de42405bd.jpg" heigth = 30% width = 30%>

Pour la prochaine séance, il faudra essayer d'utiliser ce capteur avec la PWM. Si ce ne marche toujours pas, on devra en changer.
Cependant, le problème de la séance dernière avec l'écran est résolu. En effet, un autre écran couleur nous a été fournit, et il est fonctionnel ! Il ne restera plus
qu'a le coder.
