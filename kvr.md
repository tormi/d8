## KVR with Pantheon

### Set up a new D8 site on Pantheon

1. Create new dev site `kvr` on https://dashboard.pantheon.io/ ([Pantheon Upstream for Drupal 8 sites](https://github.com/pantheon-systems/drops-8))
2. Visit [dev site](http://dev-kvr.pantheon.io/) and install it
3. Commit a settings change using Pantheon dashboard (PD)
4. Switch from SFTP to Git

### Clone your Git repository locally using the Git address provided by PD

    git clone ssh ...

### Download required modules locally with drush

    drush dl composer_manager, restui-8.x-1.x, rest_api_doc, csv_serialization, migrate_plus, field_group

