---
id: c6lx3qxvj6b2xxwz49xgo5s
title: Rebase Branche to Change Base Branch
desc: ''
updated: 1708520437478
created: 1678453200000
tags:
  - git
isDir: false
---

2023-03-10

Git permet de réécrire l'historique avec un rebase de déplacer une branche vers une autre. Ce cas d'usage peut-être utile pour déplacer une feature d'une branche de support vers une autre version a cause d'un changement de périmètre.

Ce changement peut se réaliser en une simple ligne de command :  

```console
git rebase --onto $targetBranch $fromBranch $featureBranch
```

- `$targetBranch` : la branche de destination sur lequel les commits seront rejoués
- `$fromBranch` : la branche de base des commits à rejouer, les commits de cette branche seront exclus
- `$featureBranch` : la branche contenant les commits qui vont être rejoués

---

Source:
- https://git-scm.com/book/fr/v2/Les-branches-avec-Git-Rebaser-Rebasing