# 基础镜像 WEB Nginx PHP 5.6

- L: Linux alpine
- N: Nginx
- P: PHP 5.6
- PHP MySQL Ext
    + mysql
    + mysqli

## Example

[challenge_pwnhub_2017_web_open_weekday](https://github.com/ctfhub-team/challenge_pwnhub_2017_web_open_weekday)

## Usage

### ENV

- FLAG=ctfhub{nginx_php_56}

You should rewrite flag.sh when you use this image.
The `$FLAG` is not mandatory, but i hope you use it!

### Files

- src 网站源码
    + index.php
    + ...etc
- Dockerfile
- docker-compose.yml

### Dockerfile

```
FROM ctfhub/base_web_nginx_php_56

COPY src /var/www/html
COPY _files/flag.sh /flag.sh
```

