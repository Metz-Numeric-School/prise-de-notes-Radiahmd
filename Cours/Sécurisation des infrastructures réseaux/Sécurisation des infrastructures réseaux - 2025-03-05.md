
# ACLs = Acces Control List 

Standard : 
- Numérotée : 1-99 et 1300-1999 
- Filtrage : IPv4 source
- Elles se positionnent toujours assez proches de la destination (switch près du SRV), en sortie de l'interface du switch


Etendue :
- Numérotée : 100-199 et 2000-2699
- Nommée : 
- Filtrage : IPv4 Source et Destination, IPv6 Source et Destination, Ports, Protocoles, addresses MAC (option)
- au plus proche de la source(switch près du PC , ACL en entré de l'interface du switch de 
- exemple Deny @ipv4 du PC1 -> @ipv4 du PC 2 en IN


Les Mots clés : 
- Any = toute les machines
- Host = une machine en particulier
- Established = que pour les ACL Etendue


ACLs = Wild card = inverse du subnet masque 


exemple : 
/10 on coupe l'adrresse ip à la 10ème en partant de la gauche 


autre exemple : 
255.255.255.255 
255.225.255.0/24 subnet masque 
0.0.0.255 = Wild card = ACLs = soustraction des 2 du dessus pour definir quelle zone on laisse passer afin de simplifier les ACLs

autre exemple :
255.255.255.255
255.255.255.192/26 subnet masque 
0.0.0.64 = Wild card


## ACL sont composées d'ACE (Access Control Elements) : 

Access-list : 
- une ACE à saisir 

IP access-list : 
- plusieurs ACE à saisir 

Vérification -> les commandes :
- show access-list 
- show ip interface 

Jusque 4 ACLs par interface de switch : 2 en IN (Entrée de l'information) et 2 en OUT (sortie de l'information)


Pka 4.1.4

![[Pasted image 20250305095618.png]]![[Pasted image 20250305104659.png]]
![[Pasted image 20250305105759.png]]