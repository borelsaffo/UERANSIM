5Gc = 5G core
l'architechture du Coeur de réseau 5G est donner par L'image suivante



le Coeur de réseau 5G est divisé ou comprend deux partie : le CP (control plan) et le UP (User plan) 
le CP (control plan) est responsable des politiques d'accès, gère les données et profil des abonnées
le UP (User plan) s'occupe de l'aiguillage du trafic
Dans le UP, on retrouve essentiellement L'UPF (User Plan function), qui assure le routage,l'acheminement des paquets entrant et sortant du Coeur de réseau
l'UPF est donc le point ou l'interface entre le Coeur les data network (DN) et le coeur de réseau.
dans un système 5G on peut utilisé un UPF pour interconnecté plusieurs Data Network au Coeur 5G.


Open5Gs est une implémentation en langage C et Opensource du Coeur de réseaux 5G.
l'objectif ici est de déployer toutes les composants du Coeur 5G, des les interconnecté dans le but d'analysé les flow de données entre différents 
composants.

Listes des différents fonctions réseaux qu'on y retrouve : 

  NRF - NF Repository Function
  SCP - Service Communication Proxy
  AMF - Access and Mobility Management Function
  SMF - Session Management Function
  UPF - User Plane Function
  AUSF - Authentication Server Function
  UDM - Unified Data Management
  UDR - Unified Data Repository
  PCF - Policy and Charging Function
  NSSF - Network Slice Selection Function
  BSF - Binding Support Function

suivre les instructions ci-dessous pour le déployement du 5Gc dans une Machine Virtuel 
apt-get update
![image](https://user-images.githubusercontent.com/27947973/203404865-84e1d05f-891d-4db1-9585-fa5853f5eb3d.png)
apt-get install gnupg
![image](https://user-images.githubusercontent.com/27947973/203405386-c5fdf4be-90d5-487d-a95f-33c2f7469859.png)
Import public key
![image](https://user-images.githubusercontent.com/27947973/203405543-f07143b2-68e9-4bd4-82b5-7a77afb10727.png)


apt update
Install MongoDG 
sudo apt install -y mongodb-org
![image](https://user-images.githubusercontent.com/27947973/203406229-d122f5c7-a41e-4da1-9028-e1c6281bd83a.png)
assuréz-vous que mongodb est bien démarré:
systemctl start mongod 
lancé mongodb au démarrage du système
affiché le status de mongodb
![image](https://user-images.githubusercontent.com/27947973/203406386-fbefc1c2-be90-403e-bc2a-d1a7b6486495.png)

### Installation Open5Gs
sudo add-apt-repository ppa:open5gs/latest
![image](https://user-images.githubusercontent.com/27947973/203406810-69c06864-0acf-4d71-a161-9e9fb5014224.png)
apt-get update
![image](https://user-images.githubusercontent.com/27947973/203406990-5ad6bb66-4d01-4bcd-a165-d3cb808a9f58.png)
sudo apt install open5gs
![image](https://user-images.githubusercontent.com/27947973/203407104-d2bf3dda-6456-4e05-892a-5dac5c3ed68f.png)
Une fois l'installation terminé, le dossier d'installation et les fichiers de configurations de chaque 
VNF se trouve dans /etc/open5gs comme le montre l'image suivante
![image](https://user-images.githubusercontent.com/27947973/203407454-c3e8080d-33b8-4097-8a95-99dce5a974b3.png)


###Configuration amf 
###Configuration Upf
###Configuration UDR
###Configuration 


Configuration 




