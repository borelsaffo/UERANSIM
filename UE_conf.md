Par defaut le fichier de configuration de l'UE ressemble à :

![image](https://user-images.githubusercontent.com/27947973/203401698-b383beaf-3ef7-4065-8a12-1352e990dbdd.png)
il faut donc le mettre à jour : 
il faut définir les informations abonnées à savoir : 
le MCC :
le MNC
L'IMSI

l'adresse ip du ou des gnodeB auquel l'UE pourra se raccorder : gnbSearchList
l'image suivante illustre notre fichier open5gs-gnb.yml modifier  /UERANSIM/config# nano open5gs-ue.yaml

Pour démarré l'UE : utiliser la commande 

dans /build

./nr-ue -c ../config/open5gs-ue.yaml 

Connection de 10 UE a la GNodeB avec le paramètre "-n" suivi du nombre d'UE qu'on veut connecté a la gnodeB
Commande utilisé :  ./nr-ue -c ../config/open5gs-ue.yaml  -n 10
![image](https://user-images.githubusercontent.com/27947973/204543810-a2d6cda5-75cf-451e-aaac-49961f755b46.png)

les IMSI sont généré automatiquement en se basant sur l'IMSI déja défini dans le fichier de configuration.

du coté de la gnodeB on observe les UEs lorsqu'il se connecte

![image](https://user-images.githubusercontent.com/27947973/204544519-e8b7cc1e-b980-4c5d-b398-1dbe00282e84.png)

