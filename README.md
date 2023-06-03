# WP Docker Dev For Apple Silicon

A beefed up version of [php - Official Image](https://hub.docker.com/_/php) build for debugging WordPress core with Docker  on Apple Silicon.

Pull from Docker Hub ([devunstuck / wp-docker-dev-apple-si](https://hub.docker.com/repository/docker/devunstuck/wp-docker-dev-apple-si)):
```
docker pull devunstuck/wp-docker-dev-apple-si:latest
```

Includes:
- [WP-CLI](https://wp-cli.org/) 
    - The official [wordpressdevelop/cli](https://registry.hub.docker.com/r/wordpressdevelop/cli#!) image doesn't have a ARM compatible version.
    Rather than using a seperate container, wpcli is installed to avoid setup struggles on devices like Apple Silicon powered M1, M2.
- [Xdebug](https://xdebug.org/).

## WPCLI
To run `wp` commands, use the `wp_php` user.

E.g. 
To run `wp help` on a container named `du-wordpress-develop-php-1` that was built using this image([devunstuck / wp-docker-dev-apple-si](https://hub.docker.com/repository/docker/devunstuck/wp-docker-dev-apple-si)) :
```
docker exec -u wp_php du-wordpress-develop-php-1 wp help
```

## Xdebug
Xdebug is enabled by default.