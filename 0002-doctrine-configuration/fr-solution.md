En cas d'erreur, assurez-vous que ces paramétres sont définis dans vos fichiers `config.yml` :

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

Le driver de Cache est `array` par défaut, mais il existe de [nombreuses alternatives plus rapide](https://github.com/doctrine/cache/tree/master/lib/Doctrine/Common/Cache).
