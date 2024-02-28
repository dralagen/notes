---
id: kw378st8l48lk9ple0o3jcu
title: Cron Validator
desc: ''
updated: 1709112841660
created: 1709110530738
---

petit validator en ligne pour se rappeler des crons : https://crontab.guru/

exemple : 
```
5 4 * * *
```


field | value | alternative
---------|----------|---------
 minute | 0-59 | 
 heure | 0-23 | 
 day of mounth | 1-31 | 
 mounth | 1-12 | JAN-DEC
 day of week | 0-6 0=SUN | 7=SUN (non standard)
 year | vide ou 1970-2099 | 

l'année n'est pas toujours renseigné. il est présent sur les jobs quatz 

# quelques tips :

Tip 1: If the day-of-month or day-of-week part starts with a *, they form an intersection. Otherwise they form a union. * * 3 * 1 runs on the 3rd day of the month and on Monday (union), whereas * * */2 * 1 runs on every second day of the month only if it's also a Monday (intersection). The [[manpage|https://crontab.guru/crontab.5.html]] is incorrect about this detail. More info.


Tip 2: Run your servers including the cron process in UTC timezone. [[Why?|http://yellerapp.com/posts/2015-01-12-the-worst-server-setup-you-can-make.html]]

Tip 3: Some cron implementations allow to specify years and seconds. However, cron is not the best tool if you need to operate at those levels, which is also why crontab.guru doesn't support them.

Tip 4: Don't use `@reboot` because it has too many [[issues|http://unix.stackexchange.com/questions/109804/crontabs-reboot-only-works-for-root]].

Tip 5: More difficult schedules can be realized by combining multiple cron expressions. For example, if you need to run X every 90 minutes, create one crontab entry that runs X every 3 hours on the hour (0 */3 * * *), and a second crontab entry that runs X every 3 hours with an offset (30 1/3 * * *).

---

Sources : 
- https://crontab.guru/tips.html
- http://www.quartz-scheduler.org/documentation/quartz-2.3.0/tutorials/crontrigger.html