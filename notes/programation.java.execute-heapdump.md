---
id: bkb12ngveca6qyetiwtbpxq
title: Execute Heapdump
desc: ''
updated: 1709028742143
created: 1677070800000
tags:
  - java
isDir: false
---
Prérequis : exécuter un garbage collector pour vider la mémoire afin de mieux détecter un memory leak [[programation.java.execute-garbage-collector]]

Into docker :

`jmap -dump:format=b,file=<filename>`

Or

`jcmd <PID> GC.heap_dump -all dump`

