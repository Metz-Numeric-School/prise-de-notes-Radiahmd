SVI dans chaque vlan : switch virtual interface

Topologie 2 : 

Reprendre les 3 switch de la topologie 1. 

Ajouter le Switch 3560 24PS (le deuxième dans packet) 

Dans Physical il faut ajouter AC Power Supply afin de power on le switch 

CLI du Switch ajouté : 

En  

Conf t  

Hostname SW-L3 

^z 

wr 

Show run (pour voir) 

Conf t 

Interface range G1/0/1-6 

Sw mode trunk 

Exit 

Vtp mode client 

Vtp domain BSRC2 

Vtp password MNS 

^z 

Wr 

Création d’une interface VLAN 10 : 

Dans SW-L3 : 

En 

Conf t 

Interface vlan 10 

Ip add 172.16.0.254 255.255.255.0 

^z 

wr 

Ainsi de suite afin de créer toutes les interfaces