
Outis open source, pour réaliser du cache d'image docker directement sur le cluster.

Sélecteur sur le noeud controle-plan qui gère le cluster.
Limite le pull des images sur les registry publiques. Afin de gérer l'indispo du registry ou la suppression des images ou de ne pas dépasser les limites de pull.

1er version en 2022.

--- 

Source:
- https://enix.io/fr/blog/caching-image-conteneurs-kubernetes/
- https://github.com/enix/kube-image-keeper