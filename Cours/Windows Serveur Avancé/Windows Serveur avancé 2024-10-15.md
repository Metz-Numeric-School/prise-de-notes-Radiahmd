
## DNS : Domain Name System/Service/Serveur 

# Système DNS

L'ICANN est un organisme qui gère la liste des Top Level Domain (TLD) -> .com .fr .gouv
L'ICANN délègue la gestion de chaque TLD à un organisme (registry -> rôle technique )

-> AFNIC gère le registre des .fr
-> VeriSign gère le registre des .com/.net/.org/.name/.info/.biz

Chaque registry autorise des registrars à vendre des TLD 
Registrars -> rôle commercial

ccTLD = TLD d'un pays .fr/.ma

13 Serveurs racines dans le monde.  On connaît leurs addresses ip 

## Service DNS 

FQDL = Fully Qualified Domain Name qui se termine par un point plus la racine DNS

Domaine Inverse : adresse Ip reseau en nom de domaine avec l'ajout d'un domaine spécial in-addr.arpa à la fin 

Délégation (plus tard)

Zone primaire et zone secondaire :
-> Transfert de zones entre serveur maître primaire et un autre serveur secondaire 
-> Scénarios possibles : 
- Serveur cache : le but est d'effectuer des requêtes DNS pour se rappeler de la réponse pour la prochaine requête. Avantages : Réduction de la bande passante et de la latence. Exemple : Boxe maison
- Serveur primaire (maître) : le but est de contenir des enregistrements DNS (zone DNS). Peut être imaginaire mais seulement sur un réseau local fermé, non connecter à Internet
- Serveur secondaire (esclave) : le but est de contenir une copie des zones configurées sur le serveur maître. Avantages : Recommandé sur les réseaux, importants, plus rapide lorsque le serveur maître est occupé
- Serveur stub, 

Enregistrements DNS : le but est de mapper nom d'hôte/adresse IP et adresse IP /nom d'hôte

- Enregistrement SOA Start Of Autority -> Mappage Serveur DNS de la zone principale/Adresse ip
- Enregistrement NS Name Server -> Mappage Serveur DNS/Adresse Ip
- Enregistrement A -> Mappage Hôte/Adresse IP v4
- Enregistrement AAAA -> Mappage Hôte/Adresse IP v6

Préconfiguration : nom NetBios + Adresse Ip

Erreur diapo -> Mettre le point à la fin dans Config SOA et NS, Forcer OK si encore erreur 

DHCP : Dynamic Host 