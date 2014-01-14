Si cette commande retourne : *Proxy Classes are always regenerating.*

C’est parce que l’auto_generate_proxy_classes est en mode debug. Afin de désactiver le kernel.debug, il faut lancer cette commande :
```sh
$ php app/console doctrine:ensure-production-settings --no-debug --env=prod
```
Si après cela la commande renvoie une erreur de type :
```sh
PHP Fatal error:  Class 'isReady\CoreBundle\Entity\Checklist' not found in /home/jolicode/isReady/app/cache/prod/appProdProjectContainer.php on line 340
PHP Stack trace: ...
```
Il faut alors vider le cache :
```sh
$ php app/console cache:clear -env=prod
```