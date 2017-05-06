# HumHub - Open Source Social Network Kit

### About
[HumHub](https://www.humhub.org) is a free social network software and framework built to give you the tools to make communication and collaboration easy and successful.

It's lightweight, powerful and comes with an user-friendly interface. With HumHub you can create your own customized social network, social intranet or huge social enterprise application that really fits your needs.

Boost your business, support your customers, teach your students or organize your football club. It's on you.

### Usage
 1. Fill in your desired db and storage configuration
 2. Decide weather to use stack scoped storage like "rancher-nfs"

### Develop new humhub module
 * Navigate to index.php?r=gii
 * Click on start at "HumHub Module Generator"
 * Rename "example" to whatever module name you like
 * Click on preview and generate basic module

### Edit/remove current db configuration
     `${HUMHUB_PROTECTED_CONFIG}/dynamic.php`

### Upgrade HumHub to a newer version
   docker-compose -f docker-compose-prod.yml stop
   docker-compose -f docker-compose-prod.yml up --build --force-recreate
   docker exec -it <container_id> bash
   php yii migrate/up --includeModuleMigrations=1
