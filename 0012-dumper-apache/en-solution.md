> Warning: this feature is deprecated in Symfony 2.5

Run this command and put the resulting output in your VirtualHost configuration:

```sh
$ php app/console router:dump-apache --env=prod --no-debug
```

Then add to your `app/config/config_prod.yml` configuration file the following lines:

```yml
parameters:
    router.options.matcher.cache_class: ~ # disable router cache
    router.options.matcher_class: Symfony\Component\Routing\Matcher\ApacheUrlMatcher
```

Optionally you can change the `web/app.php` file to replace `Request` by `ApacheRequest`:

```php
<?php
use Symfony\Component\HttpFoundation\ApacheRequest;

// [...]

$kernel->handle(ApacheRequest::createFromGlobals())->send();
```
