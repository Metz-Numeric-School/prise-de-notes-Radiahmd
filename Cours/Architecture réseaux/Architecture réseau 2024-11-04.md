
## Rappels

4 bits = 16 combinaisons
8 bits = 256 
16 bits = 65536


1234(10) = 1 *1024 + 1 128 + 1  64 + 1 16  + 1 2

-> 0100 1101 0010

Table de vérité :

8421
0000 = 0
0001 = 1
0010 = 2
0011=3
0100=4
0101=5
0110=6
0111=7
      8
      9
      A
      B
      C
      D
      E
      F

Modèle OSI : 

7 Application : 

6 Présentation : 

5 Session : 

4 Transport : Firewall/pare-feu, ID : Port 16 bits MESSAGE : Segment

3 Réseaux : routeur IDENTIFIANT : adresse IPv4 32 bits, adresse IPv6 128 bits MESSAGE : Paquet/Packet

2 Liaisons de données : switch/commutateur, IDENTIFIANT : adresse mac 48bits, MESSAGE : Trames/Frame

1 Physique : câbles Ethernet, coaxial, fibre (photons dans un tube en verre), ondes éléctromagnétique ex Wifi, Hub (ancien concentrateur, 0 sécurité) 

Classe :
adresse de début 0.0.0.0          adresse de fin 255.255.255.255

Classe A : grande entreprises 0.0.0.0 à 127.255.255.255

Classe B : moyenne entreprises 128.0.0.0 à 191.255.255.255

Classe C : petites entreprises 192.0.0.0 à 223.255.255.255

Classe D : adresse multicast (groupe d'adresse unicast) 224.0.0.0 à 239.255.255.255

Classe E : adresses non distribués, garder au cas où 240.0.0.0 à 255.255.255.255

128 64 52 16  8 4 2 1 
1     0   0    0  0 0 0 0    = 128 ( Fin exclu de la classe A)
1     1   0     0 0 0 0 0      = 192 ( fin exclu de la classe B)
1     1   1     0 0 0 0 0      = 224 (fin exclu de la classe C)
1      1  1      1 0 0 0 0      = 240 (fin exclu de la classe D)



# Découpage de plages d'adresse 

taille du bloc /24 -> 256 combinaisons
            /23 -> 128 combinaisons
             /25 -> 512 combinaisons 



Adresse du réseaux = première ip de la plage/du bloc

172.16.1.0/23 n'est pas l'adresse du réseaux


Procédure : 

Protocole VTP -> mode trunk pour les switch, mode trunk = pouvoir véhiculer les informations sur plusieurs vlan

Mode accès pour les terminaux 

![[Pasted image 20241104160832.png]]

Protocole vtp    
   
Dans les switchs (une fois en mode server, le reste de fois en mode client)    

- En    
    
- Conf t   
    
- Vtp mode server   
    
- Vtp domain BSRC2   
    
- Vtp password MNS   
    
- Hostname SW-1   
    

   
Dans le switch server, créer les vlan :   

- En   
    
- Conf t    
    
- Vlan 10   
    
- Name SALES   
    
- Exit   
    
- Vlan 20 et ainsi de suite pour les départements différents   
    

Pour vérifier que tout a été pris en compte (ne pas oublier le ctrl-z – wr), tapper la commande “show vlan brief)   
   
Configurer les liens trunks :   

- Conf t    
    
- Int G0/2 ou 3 selon le switch   
    
- Switchport mode trunk   
    

Pour vérifier que tout a été pris en compte (ne pas oublier le ctrl-z – wr), tapper la commande “show int tr)

show vlan brief =  cmd pour afficher le résumé des vlan 
-> sh vlan br

show int trunk = cmd pour aficher les interfaces
-> sh vlan tr

Dans le switch 1 :
conf t
int G0/2
switchport mode tr

Dans le switch 1 :
conf t
interf range G0/1-2
sw mo tr
^z
wr


Dans le SW1 serveur pour attribuer les ports dans d'autres VLAN :
conf t
int range F0/1-18
sw mo ac
sw ac vlan 10
^z
wr