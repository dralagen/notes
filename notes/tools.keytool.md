---
id: 0dblxvk6yt2rb0lcndaysg4
title: Keytool
desc: ''
updated: 1708959644561
created: 1675256400000
isDir: false
---

Voir le certificat d'un site
```Shell
openssl s_client -showcerts -connect google.fr:443
```


Voir la liste des clé dans un truststore
```shell
keytool -list -v -keystore truststore.jks
```
