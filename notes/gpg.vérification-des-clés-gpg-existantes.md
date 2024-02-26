---
id: 6w38q3wgub03yzdh707d8oa
title: Vérification Des Clés Gpg Existantes
desc: ''
updated: 1708520437478
created: 1708520437478
isDir: false
---
2023-01-24

# Liste les clés existantes

```shell
gpg --list-secret-keys --keyid-format=long
```

Possible de faire de la récupération de clé publique : [[gpg.récupération-de-la-clé-publique]]
ou de régénérer une nouvelle clé [[gpg.génération-d un-nouvelle-clé-gpg]]

--- 
Tags:  #git #gpg

Source:
- https://git-scm.com/book/fr/v2/Utilitaires-Git-Signer-votre-travail
- https://docs.github.com/fr/authentication/managing-commit-signature-verification/checking-for-existing-gpg-keys
