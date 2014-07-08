Essayer de vous rendre sur une route qui n'existe pas avec le contrôlleur de production pour voir si cet message par défaut apparait:

> Oops! An Error Occurred
> The server returned a "404 Not Found".

Vous pouvez aussi essayer une route existante lançant une exception, ou une route sécurisé avec un utilisateur n'ayant
pas les droits nécessaires.

La page d'erreur doit être personnalisée pour l'expérience utilisateur et pour éviter d'exposer que votre site est en Symfony2.
