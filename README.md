# Docker WordPress
Wordpress, PHP-FPM 7.4, MySQL 8, Nginx Setup

# About the repo
It was a mix of things.  I wanted to brush up on my WordPress, as well as learn about Docker.  Hopefully you find this helpful.

# Getting Started
## Prerequisites
- Docker
- Git

## Installation
1. Clone the repo
```bash
git clone https://github.com/danfoust/docker-wordpress.git
```
2. Run docker-compose
```bash
docker-compose up -d
```

## Personalizing
You can personalize this setup by installing git and then updating the WordPress Dockerfile to pull in your theme repository (using git clone).

## Other helpful additions
Copy and paste these commands into your Wordpress Dockerfile to be able to use these packages

### Include WP CLI
```bash
RUN curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar \
    && chmod +x wp-cli.phar \
    && mv wp-cli.phar /usr/local/bin/wp
```

## Resources
```
https://sidshome.wordpress.com/2020/06/05/how-to-change-the-maximum-file-size-you-can-upload-to-wordpress-on-nginx-w-php-fpm/
https://www.hostinger.com/tutorials/how-to-install-wordpress-with-nginx-on-ubuntu/
```
