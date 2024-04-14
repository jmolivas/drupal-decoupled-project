# Drupal Decoupled Integrations: Drupal GraphQL demo site

## Get Started

### Clone site

```bash
git clone git@github.com:octahedroid/drupal-graphql-example.git
```

### Start ddev

```bash
ddev start
```
<!--
### Import Database dump from demo example

```bash
ddev import-db --file=db.sql.gz
``` -->

### Install dependencies using composer

```bash
ddev composer install
```

### Install Drupal site

```bash
ddev drush site:install graphql_example -y
```

### Import content

```
ddev drush content:import profiles/graphql_example/assets/content.zip
```

### Login using drush

```bash
ddev drush uli admin
```

### Configure Simple OAuth Settings

You can reuse the previously generated Consumers currently at the site, or you can created new Consumers if this is the case, make sure you and assign the proper Scope of `Viewer` & `Previewer` depending on the usage you are planing to give to each one.

> Make sure you remember the values used as secret on each one because you will need them for the front-end env variables configuration.

More info about it at this blog post [Implementing Content Previews with Drupal and Remix](https://octahedroid.com/blog/implementing-content-previews-drupal-and-remix)
