Prérequis : exécuter un garbage collector pour vider la mémoire afin de mieux détecter un memory leak [[programation.java.execute-garbage-collector]]

Into docker :

`jmap -dump:format=b,file=<filename>`

Or

`jcmd <PID> GC.heap_dump -all dump`

