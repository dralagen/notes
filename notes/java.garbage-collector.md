---
id: cgl4ub0a4klbpoh6y1jdtd7
title: Garbage Collector Java
desc: ''
updated: 1708520628973
created: 1677416400000
tags:
  - java
isDir: false
---

Le Garbage collector permet de nettoyer une partie de la mémoire de l'application. Au niveau de la heap.
[[java.type-de-memoire]] 

# Mémoire Heap
La heap est divisée en deux zones :
**Young generation** : zone jeune est l'endroit où les objets nouvellement créés sont stockés. Encore devisé en deux "Eden Space" et "survivor spaces". Les objets qui sont conservées dans la young generation est promu dans la old generation.
**Old generation** : zone de stockage long, où les objets ont survécu à plusieurs cycle de collection dans la young generation.
La zone est aussi subdivisé en deux espaces, l'espace permanent "permanent space" et l'espace de la pile "stack memory "

# type de collector 
- **Serial GC**, GC par défaut pour les applications a faible consommation de mémoire, monothread. La collecte est relativement simple. `-XX:+UseSerialGC`
- **Parallel GC**, pour les applications a forte consommation de mémoire, multithreads. La collecte exécuter en parallèle sur plusieurs thread pour améliorer les performances. `-XX:+UseParallelGC`
- **Concurrent-Mark sweep GC**, pour les applications avec des temps de réponse rapide, ou la latence est un facteur critique. La collecte fonctionne en arrière plan pour minimiser la durée de la pause de collection. `-XX:+UseConcMarkSweepGC`
- **Garbage-First GC (G1)**, pour les applications a forte consommation mémoire et contrainte de temps de réponse strictes. Fonctionne en parallèle sur plusieurs thread pour les performances utilisé aussi un tri de tas pour optimiser les performances. `-XX:+UseG1GC`

# Fonctionnement du Garbage collector
Le GC s'exécute en arrière plan, à la recherche des objets plus référencés par le programme et les marque pour la suppression.
Le traitement de nettoyage est déclenché lorsque la JVM détecte que l'espace disponible sur le tas est devenu insuffisant pour allouer de nouveau objet.

Dans la zone jeune, la stratégie de GC se base sur le comptage de référence dans l'application.
Une fois qu'un objet n'est plus référencé, le GC les marques comme objet à supprimer.
Une fois un objet a survécu à plusieurs cycles, l'objet est promu à la zone ancienne.

Dans la zone ancienne, le GC utilise une stratégie de marque et de balayage. 
Cette stratégie marque tous les objets encore référencés, puis balayage la mémoire pour supprimer les objets non marqué.
Cette stratégie peu engendrer une pause dans la JVM ce qui peut affecter les performances.

Les performances du GC depends de beaucoup de facteur comme la taille de l'application, le nombre d'allocations, le nombre de thread.

Des tests de performances sont a effectué pour attribuer la meilleure stratégie de GC.

---

Source:
- https://kotlin-java.fr/garbage-collector-jvm/