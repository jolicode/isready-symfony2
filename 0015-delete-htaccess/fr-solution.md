Copier les directives du fichier `web/.htaccess` dans votre fichier de VirtualHost (`apache2.conf` ou `httpd.conf`, ou encore un fichier dans `apache2/conf.d`).

Vous pouvez ensuite remplacer les occurences de `AllowOverride All` par `AllowOverride None` et bénéficier d'un gain de performance.
