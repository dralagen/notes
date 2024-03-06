
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

Source:
- https://argo-cd.readthedocs.io/en/stable/operator-manual/upgrading/overview/
