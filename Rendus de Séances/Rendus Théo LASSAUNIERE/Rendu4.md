# Séance 4

#### Séance de la soutenance de projet

Lors de cette séance, nous avons présenté notre projet et son avancement à nos professeurs. Il s'agissait donc d'une séance particulière.
Cependant, nous avons eu aussi le temps d'avancer sur notre projet. Voici donc mon compte-rendu :

L'objectif pour moi lors de cette sénace était de voir si notre capteur marchait quand on le branchait en mode PWM. Le montage réalisé et le capteur codé, je m'empressai
de vérifier si il marchait. 

**Problème :** Il ne marchait pas. Comme les professeurs faisait passer les soutenances et que je n'ai pas pu régler le problème par moi-même, j'ai décidé à la fois de
répéter mon oral et d'essayer de voir avec mon binôme pour la partie modélisation.

L'oral passé, un des professeurs m'a recommandé de mesurer la tension aux bornes de la résistance du circuit et d'en tirer les conclusions qui s'imposaient.

Schéma du montage :
-----
<img src="https://user-images.githubusercontent.com/120557548/213485519-f448e312-71a7-4fc9-9e1d-c32a9d13e430.png">

Ceci fait, je m'aperçu en effet que l'on obtenait pas les valeurs escomptées. En effet, comme la derniere fois avec les mesures des fils du bus I2C, on obtenait des tensions
variant de 0 à 1V.

Le capteur Lidar était donc inutilisable. 
A la fin du cours, on nous à confié un capteur Doppler d'une fréquence de 10.525Ghz
A la différnce du Lidar, celui-ci mesure directement la vitesse à l'aide d'une onde et de sa réflexion en utilisant l'effet Dopller.
En fin de séance, je l'ai programmé pour tester son fonctionnement et je dois maintenant trouver comment afficher la vitesse mesurée.

Image du capteur :
-----

<img src="https://user-images.githubusercontent.com/120557548/213487747-ab14ac6b-9797-48ce-a694-277e72498f62.jpg" width = 30% heigth = 30%>

Image du montage :
-----

<img src="https://user-images.githubusercontent.com/120557548/213488034-0e9ac6dd-ab9a-4cd7-86fd-06c2b81e1227.jpg" width =30% heigth = 30%>





