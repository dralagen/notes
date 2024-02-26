---
id: x8q4m8igz0w6pcv4zawkzpx
title: Information Disk Lvm
desc: ''
updated: 1708520437477
created: 1708520437477
isDir: false
tags:
  - adminsys
  - linux
---
Affichage des groupes de volumes

`vgdisplay`

exemple de sortie:
```
# vgdisplay new_vg
  --- Volume group ---
  VG Name               new_vg
  System ID
  Format                lvm2
  Metadata Areas        3
  Metadata Sequence No  11
  VG Access             read/write
  VG Status             resizable
  MAX LV                0
  Cur LV                1
  Open LV               0
  Max PV                0
  Cur PV                3
  Act PV                3
  VG Size               51.42 GB
  PE Size               4.00 MB
  Total PE              13164
  Alloc PE / Size       13 / 52.00 MB
  Free  PE / Size       13151 / 51.37 GB
  VG UUID               jxQJ0a-ZKk0-OpMO-0118-nlwO-wwqd-fD5D32
  ```

affiche les groupes volumes en compact
`vgs` 

lien:
- [[adminsys.ajout-d-espace-disk]]
