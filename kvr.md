## KVR with Pantheon

### Set up a new D8 site on Pantheon

1. Create new dev site `kvr` on https://dashboard.pantheon.io/ ([Pantheon Upstream for Drupal 8 sites](https://github.com/pantheon-systems/drops-8))
2. Visit [dev site](http://dev-kvr.pantheon.io/) and install it
3. Commit a settings change using Pantheon dashboard (PD)
4. Switch from SFTP to Git

### Clone your Git repository locally using the Git address provided by PD

    git clone ssh ...

### Download required modules locally with drush

    cd mysiteroot
    drush dl restui-8.x-1.x, rest_api_doc, csv_serialization, migrate_plus, field_group

### Manage dependencies with Composer Manager

[Composer Manager](https://drupal.org/project/composer_manager) discovers each module’s composer.json file and adds it to the above mentioned merge list.

    drush dl composer_manager  
    php modules/composer_manager/scripts/init.php  
    composer drupal-update 

### Push local code changes to master

    git add .
    git commit -m "Description of the change."
    git push origin master

### Enable pushed modules

1. Switch from Git to SFTP in PD
2. Enable modules on http://dev-kvr.pantheon.io/admin/modules
