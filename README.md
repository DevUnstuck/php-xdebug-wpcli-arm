# PHP Xdebug WPCLI ARM

This recipe builds a WordPress debugging ready flavor of PHP - ([devunstuck / php-xdebug-wpcli-arm](https://hub.docker.com/repository/docker/devunstuck/php-xdebug-wpcli-arm)).

It is based on [php - Official Image](https://hub.docker.com/_/php), and can be used in similar fashion.

Tools included:
- [WP-CLI](https://wp-cli.org/) 
    - The official [wordpressdevelop/cli](https://registry.hub.docker.com/r/wordpressdevelop/cli#!) image doesn't have a ARM compatible version.
    Rather than using a seperate container, wpcli is installed to avoid setup struggles on devices like Apple Silicon powered M1, M2.
- [Xdebug](https://xdebug.org/).

## WPCLI
To run `wp` commands, use the `wp_php` user.
E.g. if the container is named `du-wordpress-develop-php-1`, do:
`docker exec -u wp_php du-wordpress-develop-php-1 wp help`

## Xdebug
Xdebug is enabled by default.