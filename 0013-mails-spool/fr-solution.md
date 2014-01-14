Afin d'utiliser le "spool", il faut utiliser la configuration suivante :
```yaml
# app/config/config.yml
swiftmailer:
    # ...
    spool:
        type: file
        path: /path/to/spool
```
Lor de l'envoi d'un email depuis l'application Symfony2, il ne sera pas réellement envoyé mais ajouté au fichier dont le chemin est indiqué dans ```path```.
Afin d'envoyer manuellement les messages présents dans le spool il faudra alors taper la commande suivante :
```sh
$ php app/console swiftmailer:spool:send --env=prod
```
Il est bien sûr conseillé de lancer cette commande automatiquement à intervalle régulier par une tâche cron ou une tâche planifiée.