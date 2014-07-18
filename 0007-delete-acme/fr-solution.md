Suivre ces étapes pour supprimer `AcmeDemoBundle` :

- supprimer le répertoire `src/Acme` ;
- supprimer les références à `AcmeDemoBundle` dans le fichier de routing `app/config/routing_dev.yml` ;
- supprimer le bundle dans `app/AppKernel.php` ;
- supprimer le répertoire `web/bundles/acmedemo` ;
- éditer le fichier  `security.yml` pour l'adapter a vos besoin.
