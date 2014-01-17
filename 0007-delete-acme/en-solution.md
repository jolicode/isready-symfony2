1. Supprimer le dossier du Bundle situé dans `src\Acme`
2. Supprimer son chargement dans `app/AppKernel.php`
```php
if (in_array($this->getEnvironment(), array('dev', 'test'))) {
    $bundles[] = new Acme\DemoBundle\AcmeDemoBundle();
    $bundles[] = ...
}
return $bundles;
```

3. Supprimer les 3 routes dans `app\config\routing_dev.yml`

```yaml
_welcome:
    pattern:  /
    defaults: { _controller: AcmeDemoBundle:Welcome:index }

_demo_secured:
    resource: "@AcmeDemoBundle/Controller/SecuredController.php"
    type:     annotation

_demo:
    resource: "@AcmeDemoBundle/Controller/DemoController.php"
    type:     annotation
    prefix:   /demo
```
