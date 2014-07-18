Si un des **Mandatory requirements** n'est pas **OK**, vous devez impérativement corriger votre configuration ou votre serveur.

Pour trouver vos fichiers `php.ini`, executez les snippets suivants:

Depuis la ligne de commande :

```sh
$ php --ini
```

Depuis un fichier PHP dans votre navigateur :

```php
<?php phpinfo(); ?>
```

Les **Optional recommendations** doivent aussi être corrigées avant de passer en production, même si elles sont
optionnels, si vous voulez obtenir le meilleur de votre projet.
