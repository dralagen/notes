---
id: fdy1qq99u362rhnpkdr9au5
title: Upgrade Argocd
desc: ''
updated: 1708520437479
created: 1708520437479
isDir: false
---
2023-02-12

`<version>` correspond au tag argocd comme `v2.6.1`

# Non-HA

```Shell
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/<version>/manifests/install.yaml
```

# HA

```Shell
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/<version>/manifests/ha/install.yaml
```


--- 
Tags: #k8s #kubernetes 

Source:
- https://argo-cd.readthedocs.io/en/stable/operator-manual/upgrading/overview/
