Si vous utilisez Doctrine dans votre projet, vous devez vous assurer que certains paramètres de configurations
sont définis afin de bénéficier des meilleures performances possibles en production.

Vous devez lancer cette commande pour vérifier la configuration:

```sh
$ php app/console doctrine:ensure-production-settings --env=prod --no-debug
```
