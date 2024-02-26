---
id: 5yda6qtlbfbnwpiijnb555n
title: Docker Clean Useless Image
desc: ''
updated: 1708520437477
created: 1708520437477
isDir: false
---
2023-06-06

# Remove all images without tags :
```Shell
docker rmi $(docker images -f "dangling=true" -q)
```

# cleanup images unsused :
```Shell
docker image prune -a
```
Possible d'ajouter un filtre exemple créé il y a plus de 24h :
`--filter "until=24h"`

--- 
Tags: #Docker #purge 

Source:
- https://docs.docker.com/config/pruning/

