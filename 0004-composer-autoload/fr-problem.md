Le fichier `autoload.php` permet de charger automatiquement chaque classe se trouvant dans le dossier vendor. Afin d’optimiser ce procédé il faut utiliser la commande :
```sh
$ php composer.phar dump-autoload --optimize
```
Ce qui va créé dans le projet, une map de l’ensemble des classes de celui-ci.