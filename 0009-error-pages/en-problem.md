Try going on a non existing route with the production controller to see if the default error page appear:

> Oops! An Error Occurred
> The server returned a "404 Not Found".

You should also try an existing route throwing an exception, or going to a secured route with
an not authorized user.

The error page must be customized for user experience and to avoid exposing you use Symfony2.
