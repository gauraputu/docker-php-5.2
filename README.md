# Docker image for php 5.2 legacy projects

[![Image size](https://img.shields.io/docker/image-size/prncd/php-5.2)](https://hub.docker.com/r/prncd/php-5.2/)

This docker image is intended to work as a replacement for old legacy projects, running on old server.

Features:
* Features included from the [original repository](https://github.com/kuborgh/docker-php-5.2):
    * Based on Ubuntu 12.04
    * Apache MPM Prefork
    * PHP 5.2.17 as apache mod
    * Zend Optimizer
* Features added by [Demin](https://github.com/deminy/docker-php-5.2)
    * Enable PHP on the default site.
    * Allow [short open tag](http://php.net/manual/en/ini.core.php#ini.short-open-tag).
    * Various updates and fixes.
* Features added by princed
    * XSLT support
    * Zend Optimizer and memcache pinned to working versions

# Sample Docker compose file

```yaml
version: '3'

services:
  app:
    image: prncd/php-5.2
    ports:
      - "80:80"
    volumes:
      - ~/projects/example.com:/project
```
