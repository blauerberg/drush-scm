# Drush scm
Source code management script with drush.
This script updates Drupal using [drush](http://www.drush.org/en/master/) and helps version control of git managed source code.

## Usage

```
$ git clone https://github.com/blauerberg/drush-scm.git
$ cd {your_drupal_site_root}

# show help message
$ /path/to/drush-scm upc -h

# update all modules to lastest version
$ /path/to/drush-scm upc

# update only panels
$ /path/to/drush-scm upc --module panels

# update to views 7.x-3.5
$ /path/to/drush-scm upc --module views --version 7.x-3.5
```

## Configuration

You can configure some options by override drush-scm.ini.
For example, if your Drupal site is in Docker container, you can use this script via `docker-compose`.

```
[common]
# DrushCommand = drush
# example for docker-compose
DrushCommand = docker-compose exec -T php drush
```

## License
This software is released under the MIT License, see LICENSE.
