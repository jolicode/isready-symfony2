Si cette commande retourne : *Proxy Classes are always regenerating.*

C’est parce que l’`auto_generate_proxy_classes` est en mode debug. Afin de désactiver le kernel.debug, il faut lancer cette commande :
```sh
$ php app/console doctrine:ensure-production-settings --no-debug --env=prod
```