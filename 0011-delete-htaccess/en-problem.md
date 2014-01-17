Les fichiers `.htaccess` permettent de modifier la configuration de serveur Apache, en définissant des règles et directives dans un répertoire. On peut les utiliser pour protéger un répertoire par mot de passe, ou gérer l’accès à certains fichiers.

Le fichier `.htaccess` s’applique au répertoire dans lequel il se trouve ainsi qu’à tous les sous-répertoires ; par contre si un de ces derniers a lui aussi un `.htaccess` alors il est prioritaire sur son compère du niveau supérieur, et ainsi de suite.

À chaque requête sur le serveur l’ensemble des fichiers .htaccess sont parcourus ; cela s’avère donc assez gourmand en terme de ressources.

Il faut donc limiter l’utilisation de ces fichiers.