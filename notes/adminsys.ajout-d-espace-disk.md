---
id: 7zrmexgow1et2u02hgzgz7t
title: Ajout d'espace disk
desc: ''
updated: 1708520819027
created: 1708520437477
isDir: false
tags:
    - linux
    - adminsys
---

Ajouter 10 Go sur la partition 
`lvextend -L10G /dev/mapper/{name-disk}`

Appliquer le resize sur la parition 
`resize2fs /dev/mapper/{name-disk}`

lien :
- [[adminsys.information-disk-lvm]] : récupération des informations de la place disponnibe
