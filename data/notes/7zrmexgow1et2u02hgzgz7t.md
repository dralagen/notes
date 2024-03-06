
Ajouter 10 Go sur la partition 
`lvextend -L10G /dev/mapper/{name-disk}`

Appliquer le resize sur la parition 
`resize2fs /dev/mapper/{name-disk}`

lien :
- [[adminsys.information-disk-lvm]] : récupération des informations de la place disponnibe
