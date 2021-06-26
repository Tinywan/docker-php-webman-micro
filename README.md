## Inc

Webman Lightweight container with PHP 7.4 based on Alpine Linux.

## build

```
docker build -t tinywan/docker-php-webman-mirco:0.1 .
```

## run

```
docker run -it -p 8080:8080 -name mirco-webman tinywan/docker-php-webman-mirco:latest

-- daemon
docker run -d -p 8080:8080 -name mirco-webman tinywan/docker-php-webman-mirco:latest
```

