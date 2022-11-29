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

build# ./nr-ue -c ../config/open5gs-ue.yaml 

Connection de 10 UE a la GNodeB avec le paramètre "-n" suivi du nombre d'UE qu'on veut connecté a la gnodeB
Commande utilisé :

build# ./nr-ue -c ../config/open5gs-ue.yaml  -n 10

![image](https://user-images.githubusercontent.com/27947973/204543810-a2d6cda5-75cf-451e-aaac-49961f755b46.png)

les IMSI sont généré automatiquement en se basant sur l'IMSI déja défini dans le fichier de configuration.

du coté de la gnodeB on observe les UEs lorsqu'il se connecte

![image](https://user-images.githubusercontent.com/27947973/204544519-e8b7cc1e-b980-4c5d-b398-1dbe00282e84.png)


Afficher tous les UEs et gNodeB

build# ./nr-cli --dump

![image](https://user-images.githubusercontent.com/27947973/204545964-7d888587-41cd-4ae3-9533-56d49b05c5d9.png)

CLI gNodeB

![image](https://user-images.githubusercontent.com/27947973/204546930-4db7f5cd-ea5b-49e3-9397-a4e0fe76a0e1.png)
![image](https://user-images.githubusercontent.com/27947973/204547324-c37e2e58-eb64-4e7d-ac9b-e816cbe109aa.png)

CLI UE 
![image](https://user-images.githubusercontent.com/27947973/204547771-cdb7981a-0bc2-4482-95bb-ae44d5d420a5.png)
![image](https://user-images.githubusercontent.com/27947973/204547986-01937312-76f3-43ac-ba63-c323418d3e44.png)
![image](https://user-images.githubusercontent.com/27947973/204548413-34d3bef9-e79f-4782-b910-42bc066da2d8.png)
![image](https://user-images.githubusercontent.com/27947973/204549170-009155eb-f95e-44eb-8e89-70c1c2caafd5.png)
![image](https://user-images.githubusercontent.com/27947973/204550282-5efda448-6afe-477c-abde-c40edb82777d.png)


