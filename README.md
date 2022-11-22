# UERANSIM + 5G Core
5G-AN simulator UE + gnb

# Installation et configuration UERANSIM sur Ubuntu 

Open5gs WebUI
![image](https://user-images.githubusercontent.com/27947973/203394279-5d1f888a-07a0-4d8a-be3d-ac492eb52b94.png)

On Virtualbox
![image](https://user-images.githubusercontent.com/27947973/203394442-676c3dde-de17-4dc8-837c-4313b63fb7c5.png)

on mobilXtern
![image](https://user-images.githubusercontent.com/27947973/203394937-5ffdf0cb-0443-4df0-b80e-4eadabaf7036.png)

192.168.56.9 on eth1   private host only and 10.0.2.15 eth0  NAT   ------ 5Gc core Network function
192.168.56.8 on eth1   private host only and 10.0.2.15 eth0  NAT    ------ UE + NR-AN
192.168.56.7 on eth1   private host only and 10.0.2.15 eth0  NAT    ------ UE + NR-AN

All this is on ubuntu 
![image](https://user-images.githubusercontent.com/27947973/203395751-03f9de74-901b-4cd3-9c70-e3c7bc256d3e.png)

mkdir UERANSIM
cd UERANSIM
git clone https://github.com/aligungr/UERANSIM
![image](https://user-images.githubusercontent.com/27947973/203396145-2911c13e-f608-47d7-8e8b-ed40ea74e984.png)
go to the UERANSIM folder
![image](https://user-images.githubusercontent.com/27947973/203396232-248fc39e-e6c5-4952-99a7-1d59eb09e2af.png)
it's better to update your apt repositories 
sudo apt update
sudo apt upgrade

Install the the list of dependencies
 apt install make
 apt install gcc
 apt install g++
 apt install libsctp-dev lksctp-tools
apt install iproute2
sudo snap install cmake --classic

And  then finaly build using : make
This could take several minutes
cd ~/UERANSIM
make

![image](https://user-images.githubusercontent.com/27947973/203397311-b24276b0-6de5-455f-af79-33d95ad2c8a7.png)
![image](https://user-images.githubusercontent.com/27947973/203397375-c8453a59-bae8-4027-ab08-ecb88d32aee1.png)
![image](https://user-images.githubusercontent.com/27947973/203397447-92042df7-737f-42cb-97a5-4d62e7e246cb.png)
![image](https://user-images.githubusercontent.com/27947973/203397505-aba3d3a0-f280-42fb-9dd4-b14b1ab8f050.png)
![image](https://user-images.githubusercontent.com/27947973/203397606-b9303268-872d-4c43-9912-0125a3ab9a79.png)
![image](https://user-images.githubusercontent.com/27947973/203397657-77f20df8-5141-4add-b369-1574954c8937.png)
![image](https://user-images.githubusercontent.com/27947973/203398678-c9360d96-2774-4549-8006-0a1e94cdf70a.png)

Une fois que la compilation est terminé, les exécutable se trouve dans ~/UERANSIM/build et les fichiers de configuration de 
l'UE et de la gnodeB dans ~/UERANSIM/config
![image](https://user-images.githubusercontent.com/27947973/203399321-f420886e-5fff-4666-aec9-a094443bf839.png)




