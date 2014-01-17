On vérifie que doctrine est correctement configurée pour un environnement de production à l’aide de la commande :
```sh
$ php app/console doctrine:ensure-production-settings --env=prod
```

Cette commande va permettre de vérifier si on a bien les méta données Doctrine en cache dans le fichier `config_prod.yml`