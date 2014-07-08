Follow those steps to remove `AcmeDemoBundle`:

- delete the `src/Acme` directory;
- remove the routing entry referencing `AcmeDemoBundle` in `app/config/routing_dev.yml`;
- remove the `AcmeDemoBundle` from the registered bundles in `app/AppKernel.php`;
- remove the `web/bundles/acmedemo` directory;
- edit the `security.yml` file to remove anything you do not need.
