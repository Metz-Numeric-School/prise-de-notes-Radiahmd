
## WDS 

= Windows Deployment Services apparu avec Windows Server 2003 SP2 
-> successeur du Serveur RIS Remote Installation Service

Rappel :
TCP -> connecté -> contrôle constant donc moins rapide
UDP -> déconnecté -> pas de dialogue, envoie plus rapide.

DHCP compris dans le WDS

Offre une capacité de flux multiples dits Multicast -> déploiement de plus de 5 PC Client.

Mode Autonome est préférable au mode Active Directory 


Fonctionnement de WDS : Stockage de l'image.wim dans PC dans Serveur 

1. Recherche d'un Serveur DHCP
2. Le Serveur envoie une offre 
3. le client accepte
4. Le serveur DHCP donne une adresse IP
5. Requête TFTP du PC Client au Serveur
6. NBP du Serveur à PC Client 



Bon à savoir : Refuser une offre DHCP est la principale cyberattaque

TP :
1. Créer deux partitions en plus -> ajouter 2 disques
2. Adresse IP Statique sur le Serveur
3. Nommer le Serveur 
4. Installer le rôle WDS Service de Déploiement Windows
5. Cocher le service de déploiement et de transport
6. Configurer WDS -> Configurer le Serveur
8. Cocher Serveur Automne !!!! Page 11
9. Chemin sur la 2ème partition !! Remplacer le c: par la lettre de la 2ème Partition 
10. Redémarrer si Echec 
11. Ajouter un groupe d'image et non une image d'installation.
12. Déploiement d'un poste Client : identifiant Nom du Serveur
