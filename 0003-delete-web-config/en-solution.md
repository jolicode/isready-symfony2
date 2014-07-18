The `/web` directory must only contains production files,
leaving `app_dev.php` only protected by IP checking is not secure and the `web/config.php` file expose your PHP configuration.

## With Capistrano

```ruby
desc "Remove dangerous files"
    task :remove_web_files , :roles => :web do
      sudo %{rm -f #{current_path}/web/config.php}
      sudo %{rm -f #{current_path}/web/app_dev.php}
    end

after 'deploy:remove_web_files'
```
