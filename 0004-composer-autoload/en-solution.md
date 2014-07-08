Run the following command after `composer install`:

```sh
$ php composer.phar dump-autoload
```

> You can also use the `install -o` flag

It will convert the PSR-0/4 autoloading to a classmap in `vendor/composer/`.
