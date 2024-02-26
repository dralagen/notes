---
id: zri37q2nxvpiejwn8h45c72
title: K3s   Install
desc: ''
updated: 1708520437478
created: 1708520437478
isDir: false
---
2023-08-05

## SERVER

# Disable traefik
```
export INSTALL_K3S_EXEC="server --disable=traefik --cluster-init"
```

# Create k3s cluster
```
curl -sfL https://get.k3s.io | K3S_TOKEN="SECRET" sh -s - server --cluster-init
```

Ajout d'un noeud serveur

```
curl -sfL https://get.k3s.io | K3S_TOKEN=SECRET sh -s - server \
    --server https://<ip or hostname of server1>:6443 
```
## AGENT 


# Add server as a worker node
Récupération du token  sur le serveur maitre:
```
sudo cat /var/lib/rancher/k3s/server/node-token
```

Sur le future node :
```
curl -sfL https://get.k3s.io | K3S_TOKEN="SECRET" sh -s - agent --server https://IP_SERVER_MASTER:6443
```



--- 
Tags: #k8s #kubernetes 

Source:
- https://docs.k3s.io/quick-start
- https://docs.k3s.io/datastore/ha-embedded