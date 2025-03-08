
# Virtualisation vs Conteneurisation :

Conteneurisation = regrouper les noyaux des systèmes d'exploitation afin de gagner de la place de mémoire 
-> on peut en créer et en supprimer presque instantanément 
-> exemple Youtube : passer d'un conteneur à un autre ne se voit -> sur les machines virtuelles c'est plus complexe 

Conteneurisation : Docker
-> simplifié sous Linux et open source

< Les images Docker c'est comme les oignons, ça a plusieurs couches >
En résumé, Docker utilise un système de couches pour optimiser la gestion des images et des conteneurs, permettant une meilleure réutilisation et une exécution efficace.

Fichier execution et de config --BUILD> Docker image --RUN> Docker Container 


TP :
ip : 141.95.167.158

commande : ssh -i ./id_rsa_bsrc2 debian@141.95.167.158


AWS :
commande : docker run -it public.erc.aws/ubuntu/ubuntu:24.04_stable bash 

