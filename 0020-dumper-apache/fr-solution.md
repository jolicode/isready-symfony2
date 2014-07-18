> Attention : cette feature est dépréciée en Symfony 2.5

Executer cette command et en copier la sortie dans votre fichier de configuration Apache :

```sh
$ php app/console router:dump-apache --env=prod --no-debug
```

Ajoutez ensuite les lignes suivante a votre fichier de configuration `app/config/config_prod.yml` :

```yml
parameters:
    router.options.matcher.cache_class: ~ # disable router cache
    router.options.matcher_class: Symfony\Component\Routing\Matcher\ApacheUrlMatcher
```

Vous pouvez aussi changer votre fichier `web/app.php` pour remplacer `Request` par `ApacheRequest`:

```php
<?php
use Symfony\Component\HttpFoundation\ApacheRequest;

// [...]

$kernel->handle(ApacheRequest::createFromGlobals())->send();
```
