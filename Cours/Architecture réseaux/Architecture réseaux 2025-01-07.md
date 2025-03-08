# Packet Tracer :

## Topologie 1 :

2 Switch avec 2 VLAN : VLAN 10 et VLAN 20 -> 2 câbles croisés entre les SW, 1 par VLAN en fonction des interfaces.
(pas de boucle)


CLI Switch :
faire les config de base avec 12 interfaces par VLAN.
show vlan brief

Dupliquer le switch configuré : ctrl+C ctrl+V du Switch1

Ajouter des machines : 2 PC VLAN10 et VLAN20 par Switch.

BPDU : nom des messages Spanning Trip Protocole depuis les Switch

Faire les config des PC : IP, + Subnet Masque


## Topologie 2 :

Boucle entre les Switch


BID = Bridge ID
16bits                          48bits
D->65535                    MAC Destination
32767


BDI le plus petit est prioritaire dans l'élection du root bridge.
Sur le root bridge, toutes les interfaces s'appellent le designated port 

## Topologie 3 :

3 Switch 

Les connecter entre eux (triangle)

1 des switch sera le root bridge 


## Topologie 4 :

4 Switch 

Les connecter entre eux (carré + croix à l'intérieur) 6 câbles

1 des switch sera le root bridge 

Il est préférable de placer le switch root bridge en haut ->les liens directes vers le root bridge seront vert, les autres liens seront oranges donc on pourra les supprimer.




