---
id: bkb12ngveca6qyetiwtbpxq
title: Execute Heapdump
desc: ''
updated: 1708959761681
created: 1677070800000
isDir: false
tags:
    - jcmd 
    - jmap 
    - memory-leak
---
Prérequis : exécuter un garbage collector pour vider la mémoire afin de mieux détecter un memory leak [[programation.execute-garbage-collector]]

Into docker :

`jmap -dump:format=b,file=<filename>`

Or

`jcmd <PID> GC.heap_dump -all dump`

