# Drupal 8 + Pantheon tips

## Code snippets

### Managing dependencies with Composer Manager

[Composer Manager](https://drupal.org/project/composer_manager) discovers each module’s composer.json file and adds it to the above mentioned merge list.

    cd mysiteroot  
    drush dl composer_manager  
    php modules/composer_manager/scripts/init.php  
    composer drupal-update  

And we’re done. The vendor directory now contains our module’s dependencies.
Once we decide to install another module with Composer dependencies, for example Drupal Commerce, we just need to download that module, then run `composer drupal-update` again.

[Source](https://bojanz.wordpress.com/2015/09/18/d8-composer-definitive-intro/)

### Sample workflow for pushing local code changes to master

    git add .
    git commit -m "Description of the change."
    git push origin master
    
[See more](https://pantheon.io/docs/articles/local/starting-with-git/)

## Articles

* [D8FTW: Storing data in Drupal 8](https://www.palantir.net/blog/d8ftw-storing-data-drupal-8) by Larry Garfield. The different ways to store stuff in Drupal 8.
* [Connect Drupal 8 RESTful Service with Guzzle PHP Web Service Client](eureka.ykyuen.info/2013/09/03/connect-drupal-8-restful-service-with-guzzle-php-web-service-client-1/)
