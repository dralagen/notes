---
id: idm1kh4egumycpbj3b7v73p
title: Type De Mémoire en Java
desc: ''
updated: 1708520642002
created: 1708520437475
isDir: false
---
2023-02-06

# heap memory

Mémoire principale, contenant les objets créé par l'application.

Configurable par le -Xms et -Xmx exemple 
`java -Xms4096M -Xmx6144M ClassName`

Java utilise un Garbage collector pour le nettoyage de la heap : [[java.garbage-collector]]

# Stack memory 

Stock les variables locale et les informations de méthode mais aussi les thead exécution 

Il n'est pas géré par les Garbage collector mais par la jvm directement.


# Native Memory

L'allocation de mémoire a l'extérieur de la heap java et utilisé par la jvm.
Aussi appelé off-heap memory

Utilisé pour réaliser le serialisation en lecture et écriture. 
Les performances dépend du buffer, du process de serialisation et de l'espace disque 

La JVM stock les stack de thread, les données Internet and memory mapped files.

# Direct Memory

Allocation en dehors de la java heap.
Ça représente la mémoire utilisé sur l'OS par le process de la JVM.

Java NIO utilisé cette mémoire pour écrire les données sur le réseau ou le disques

On peut limiter le direct buffer memory size en utilisant ce paramètre :
`-XX:MaxDirectMemorySize=1024M`

--- 
Tags: #java

Source:
- Memory Types in JVM https://www.baeldung.com/java-jvm-memory-types