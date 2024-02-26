---
id: x4bafmpsd6bcj4a0e2z9s42
title: Génération D Un Nouvelle Clé Gpg
desc: ''
updated: 1708520437477
created: 1674565200000
isDir: false
tags:
    - git
    - gpg
---

Si vous utilisez la version 2.1.17 ou une version ultérieure
```shell
gpg --full-generate-key
```

Possible de custom l'aglo :
```shell
gpg --default-new-key-algo rsa4096 --gen-key
```


---

Related:
- [[gpg.vérification-des-clés-gpg-existantes]]

Source:
- https://docs.github.com/fr/authentication/managing-commit-signature-verification/generating-a-new-gpg-key
