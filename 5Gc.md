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
![image](https://user-images.githubusercontent.com/27947973/203410210-c417be97-7932-4b5d-b8bd-f623e82deb04.png)

root@vagrant:/etc/open5gs# sudo systemctl restart open5gs-amfd
root@vagrant:/etc/open5gs# sudo systemctl status  open5gs-amfd

![image](https://user-images.githubusercontent.com/27947973/203410284-316f4ce6-b787-4a5f-9278-ffec9eec1267.png)
![image](https://user-images.githubusercontent.com/27947973/203410661-733de9ee-4fb7-4af9-9c42-cc63bb9a042c.png)
![image](https://user-images.githubusercontent.com/27947973/203410817-e381e7d8-9c2f-4708-95da-d209791fdb7c.png)
![image](https://user-images.githubusercontent.com/27947973/203410987-00c38721-e728-4d92-b1e1-00e6dcf602d1.png)

![image](https://user-images.githubusercontent.com/27947973/203413838-f7db9bdd-1042-44ef-a3c8-3702437bd223.png)
![image](https://user-images.githubusercontent.com/27947973/203413640-73406788-74f5-4b9e-8d49-aa52df3ac5d0.png)
root@borel:/home/vagrant/UERANSIM/UERANSIM# build/nr-ue  -c  config/open5gs-ue.yaml
![image](https://user-images.githubusercontent.com/27947973/203414492-82277d91-3e71-43ab-aaf0-0ac6677e5615.png)
![image](https://user-images.githubusercontent.com/27947973/203414626-8ea9c814-69c3-48f5-bb38-b1806bc5548a.png)
![image](https://user-images.githubusercontent.com/27947973/203414786-8213b0c6-f669-421a-b6fe-254575bdcfaa.png)
lorsque le MCC et MCN du gnodeB qu'on veut associer a un AMF ne correspond pas au paramètre MCC et MNC definit dans le fichier


de configuration de l'amf (amf.yml) 
coté Coeur, le GnodeB ne pourra pas se connecter a L'amf via l'interface N2
![image](https://user-images.githubusercontent.com/27947973/203417744-eb34ce6c-88aa-4590-a998-9bdceeb282b3.png)
![image](https://user-images.githubusercontent.com/27947973/203418221-a13c2551-8b09-4ccd-801f-b062ee3a127b.png)







