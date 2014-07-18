There is two way to customize the error pages.

## Easiest way by overriding the default template

To override the default error template, create a new template in `app/Resources/TwigBundle/views/Exception/error.html.twig`.
It will be used for all the errors, but you can also add template by status code and format:

- `app/Resources/TwigBundle/views/Exception/error404.html.twig`
- `app/Resources/TwigBundle/views/Exception/error404.json.twig`
- `app/Resources/TwigBundle/views/Exception/error403.html.twig`
- `app/Resources/TwigBundle/views/Exception/error500.html.twig`

## Writing your own error controller

The default exception controller is `Symfony\Bundle\TwigBundle\Controller\ExceptionController`,
you can extend it and specify your own in the `app/config/config.yml` file:

```yml
twig:
    exception_controller: 'FOS\RestBundle\Controller\ExceptionController::showAction'
```
