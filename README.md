# Drush scm
Source code management script with drush.
This script updates Drupal using [drush](http://www.drush.org/en/master/) and helps version control of git managed source code.

## Usage

```bash
$ git clone https://github.com/blauerberg/drush-scm.git
$ cd {your_drupal_site_root}

# show help message
$ /path/to/drush-scm -h
$ /path/to/drush-scm ups -h
$ /path/to/drush-scm upc -h

# show unapplied security updates
$ /path/to/drush-scm ups

# update core and all modules to latest version with security fixes
$ /path/to/drush-scm upc

# update all modules other than views and panels
$ /path/to/drush-scm upc --exclude-module views,panels

# update only Drupal core
$ /path/to/drush-scm upc --module drupal

# update only panels
$ /path/to/drush-scm upc --module panels

# update to views 7.x-3.8
$ /path/to/drush-scm upc --module views --version 7.x-3.8

# update ctools to lastest stable version
$ /path/to/drush-scm upc --module ctools --apply-no-security-update
```

## Configuration

You can configure some options by override drush-scm.ini.

```bash
$ mkdir ~/.drush-scm
$ cp /path/to/drush-scm/drush-scm.ini ~/.drush-scm/drush-scm.ini
```

For example, if your Drupal site is in Docker container, you can use this script via `docker-compose` from host machine.

```
[common]
# DrushCommand = drush
# example for docker-compose
DrushCommand = docker-compose exec -T php drush
```

## License
This software is released under the MIT License, see LICENSE.
