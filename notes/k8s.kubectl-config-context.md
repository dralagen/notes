---
id: 63rf94fwo6w3hgiwu40zkyb
title: Kubectl Config Context
desc: ''
updated: 1708520437478
created: 1691582400000
isDir: false
tags:
  - k8s
  - kubernetes
---

# changement de context 
```Shell
kubectl config use-context <context-name>
```


# création d'un cluster
```shell
kubectl config --kubeconfig=config-demo set-cluster development --server=https://1.2.3.4 --certificate-authority=fake-ca-file
```

# création d'un credentials
```shell
kubectl config --kubeconfig=config-demo set-credentials developer --client-certificate=fake-cert-file --client-key=fake-key-seefile
```

# création d'un context
```shell
kubectl config --kubeconfig=config-demo set-context dev-storage --cluster=development --namespace=storage --user=developer
```

# suppression de context 
- To delete a user you can run `kubectl --kubeconfig=config-demo config unset users.<name>`
- To remove a cluster, you can run `kubectl --kubeconfig=config-demo config unset clusters.<name>`
- To remove a context, you can run `kubectl --kubeconfig=config-demo config unset contexts.<name>`


---

Source:
- https://kubernetes.io/docs/concepts/configuration/organize-cluster-access-kubeconfig/
- https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/