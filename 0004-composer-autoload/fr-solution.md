Executer la commande suivante après `composer install` :

```sh
$ php composer.phar dump-autoload
```

> Vous pouvez aussi utiliser le flag `install -o`

Cela va convertir l'auto-loading PSR-0/4 en classmap et le stocker dans `vendor/composer/`.
