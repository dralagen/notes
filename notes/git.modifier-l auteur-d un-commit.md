---
id: bkxga1oq004fxpq0ac1bp2z
title: Modifier L Auteur D Un Commit
desc: ''
updated: 1709028925468
created: 1674565200000
isDir: false
tags:
    - git
---

# Remplacer un user un autre utilisateur

``` Shell
git filter-branch --env-filter '
OLD_EMAIL="your-old-email@example.com"
CORRECT_NAME="Your Correct Name"
CORRECT_EMAIL="your-correct-email@example.com"
if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$CORRECT_NAME"
    export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$CORRECT_NAME"
    export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags

git filter-repo --mailmap git-mailmap
```
# Reset les informations pour un commit HEAD

``` Shell
git commit --amend --no-edit --reset-author
```

# Rebase l'historique 

```Shell
git rebase -r <some commit before all of your bad commits> \
    --exec 'git commit --amend --no-edit --reset-author'
```

`-r root` pour l'ensemble de l'historique 

---

Source:
- [Stackoverflow - rebase with me](https://stackoverflow.com/a/1320317)
