# dokku-supply-config

Supply Dokku configuration files within your app repository.

## Installation

```bash
cd /var/lib/dokku/plugins
sudo git clone git@github.com:heichblatt/dokku-supply-config.git supply-config
sudo dokku plugins-install
```

## Usage

Say you want to include a file called DOCKER_OPTIONS for the [Docker options plugin](https://github.com/dyson/dokku-docker-options). In the root directory of your app repository, create a directory called `.dokku` and put the files in there. This plugin will copy those files into `~dokku/$APP/` before building the app.

## Hooks

This plugin provides hooks:

* pre-build: copy configuration files into app directory
