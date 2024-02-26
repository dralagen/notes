---
id: lwdjj5vhknopsrlhgnu1ea1
title: Firewall with Iptables
desc: ''
updated: 1708520437477
created: 1708520437477
isDir: false
---
2023-08-05

# autoriser le trafic local 

```bash
iptables -A INPUT -i lo -j ACCEPT
```
# autoriser le trafic sur un port spécifique

```bash
iptables -A INPUT -p tcp --dport 80 -j ACCEPT
```

# supprimer le trafic indésirable
Ajout d'une règle strict a inserer en dernier
```bash
iptables -A INPUT -j DROP
```
Changement de policy pour refuser le trafic si aucune règle fonctionne 
```
iptables --policy INPUT DROP
```

# supprimer une règle
```bash
iptables -D INPUT <Number>
```

# enregistrer vos modifications

Sauvegarder les règles pour les conserver lors du reboot

```bash
iptables-save -c
```



--- 
Tags: #adminsys #security 

Source:
- https://help.ovhcloud.com/csm/fr-dedicated-servers-firewall-iptables?id=kb_article_view&sysparm_article=KB0043442