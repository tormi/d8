## KVR with Pantheon

### Set up a new D8 site on Pantheon

1. Create new dev site on https://dashboard.pantheon.io/
2. Visit dev site and install it
3. Commit a settings change using Pantheon dashboard (PD)
4. Switch from SFTP to Git
5. Clone your Git repository locally using the Git address provided by PD.

    git clone ssh ... 

### Download modules locally with drush

    cd modules
    drush dl composer_manager, restui-8.x-1.x, rest_api_doc, csv_serialization, migrate_plus, field_group
