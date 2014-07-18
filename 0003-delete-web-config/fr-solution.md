Le répertoire `/web` doit uniquement contenir des fichiers de production,
y laisser le fichier `app_dev.php` avec la seule protection par IP n'est que peu sécurisé et le fichier `web/config.php`
expose votre configuration PHP.

## Avec Capistrano

```ruby
desc "Remove dangerous files"
    task :remove_web_files , :roles => :web do
      sudo %{rm -f #{current_path}/web/config.php}
      sudo %{rm -f #{current_path}/web/app_dev.php}
    end

after 'deploy:remove_web_files'
```
