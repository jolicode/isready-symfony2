If you have Doctrine on your project, you need to make sure some settings are defined in
order to have the best production performance as possible.

All you have to do is running this command:

```sh
$ php app/console doctrine:ensure-production-settings --env=prod --no-debug
```
