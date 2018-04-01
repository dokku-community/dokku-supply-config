# dokku-supply-config [![Build Status](https://img.shields.io/travis/dokku-community/dokku-supply-config.svg?branch=master "Build Status")](https://travis-ci.org/dokku-community/dokku-supply-config)

Supply dokku configuration files within your app repository.

## requirements

- dokku 0.4.0+
- docker 1.8.x

## installation

```shell
# on 0.4.x
dokku plugin:install https://github.com/josegonzalez/dokku-supply-config.git supply-config
```

## hooks

This plugin provides hooks:

* `post-extract`: copy configuration files into app directory

## usage
This plugin allows you to store configuration files which reside in the dokku app directory, such as ENV, inside the app's git repository.

For example, say you want to include a file called DOCKER_OPTIONS for the [Docker options plugin](https://github.com/dyson/dokku-docker-options). In the root directory of your app repository, create a directory called `.dokku` and put the files in there. This plugin will copy those files into `$DOKKU_ROOT/$APP/` before building the app.
