
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

Source:
- https://docs.docker.com/config/pruning/

