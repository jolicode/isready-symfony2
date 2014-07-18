Il existe deux façons de personnaliser les pages d'erreur.

## La plus simple en écrasant le template par défaut

Pour écraser le template d'erreur par défaut, créer un nouveau template `app/Resources/TwigBundle/views/Exception/error.html.twig`.
Il sera utilisé pour toutes les erreurs, mais vous pouvez aussi ajouter des pages par status et par format :

- `app/Resources/TwigBundle/views/Exception/error404.html.twig`
- `app/Resources/TwigBundle/views/Exception/error404.json.twig`
- `app/Resources/TwigBundle/views/Exception/error403.html.twig`
- `app/Resources/TwigBundle/views/Exception/error500.html.twig`

## Écrire votre propre contrôlleur d'erreur

Le contrôlleur par défaut est `Symfony\Bundle\TwigBundle\Controller\ExceptionController`,
vous pouvez l'étendre et le configurer dans votre fichier `app/config/config.yml` :

```yml
twig:
    exception_controller: 'FOS\RestBundle\Controller\ExceptionController::showAction'
```
