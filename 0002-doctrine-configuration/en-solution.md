In case of error, make sure those settings are defined in your `config.yml` files:

```yml
doctrine:
    orm:
        auto_generate_proxy_classes: %kernel.debug% # Should be FALSE on production
        entity_managers:
            default: # Prototype
                query_cache_driver:
                    type:                 array
                metadata_cache_driver:
                    type:                 array

```

Cache driver is `array` by default, but there is a [lot of available and faster alternatives](https://github.com/doctrine/cache/tree/master/lib/Doctrine/Common/Cache).
