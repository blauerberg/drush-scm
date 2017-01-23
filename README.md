# Drush scm
Source code management script with drush.

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

## License
This software is released under the MIT License, see LICENSE.
