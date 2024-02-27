---
id: 40g9w6l00rhquijjy2kod6y
title: Signer Ces Commits
desc: ''
updated: 1709028972179
created: 1674565200000
isDir: false
tags:
    - git
    - gpg
---

prérequis : 
- Avoir l'ID de la clé gpg [[gpg.vérification-des-clés-gpg-existantes]]
- connaitre la clé public gpg [[gpg.récupération-de-la-clé-publique]]

Ajout au config git 
```Shell
git config --global user.signingkey ID
```

Force la signature des commits
```Shell
git config --global commit.gpgsign true
```


--- 

Source:
- https://git-scm.com/book/fr/v2/Utilitaires-Git-Signer-votre-travail
- https://docs.github.com/fr/authentication/managing-commit-signature-verification/telling-git-about-your-signing-key
- https://docs.github.com/fr/authentication/managing-commit-signature-verification/adding-a-gpg-key-to-your-github-account
