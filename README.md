## Inc

Webman Lightweight container with PHP 7.4 based on Alpine Linux.

## build

```
docker build -t tinywan/docker-php-webman-micro:0.1 .
```

## run

### debug
```
docker run --rm -it -p 8080:8080 --name micro-webman tinywan/docker-php-webman-micro:latest
```

output
```
2021-06-26 09:20:45,672 INFO Set uid to user 0 succeeded
2021-06-26 09:20:45,676 INFO supervisord started with pid 1
2021-06-26 09:20:46,679 INFO spawned: 'webman' with pid 9
Workerman[/app/start.php] start in DEBUG mode
----------------------------------------- WORKERMAN -----------------------------------------
Workerman version:4.0.19          PHP version:7.4.20
------------------------------------------ WORKERS ------------------------------------------
proto   user            worker          listen                 processes    status
tcp     root            webman          http://0.0.0.0:8080    8             [OK]
tcp     root            monitor         none                   1             [OK]
tcp     root            rpc             text://0.0.0.0:8081    8             [OK]
---------------------------------------------------------------------------------------------
Press Ctrl+C to stop. Start success.
2021-06-26 09:20:47,737 INFO success: webman entered RUNNING state, process has stayed up for > than 1 seconds (startsecs)
^C2021-06-26 09:23:26,937 WARN received SIGINT indicating exit request
2021-06-26 09:23:26,937 INFO waiting for webman to die
Workerman[start.php] stopping ...
Workerman[start.php] has been stopped
2021-06-26 09:23:27,977 INFO stopped: webman (exit status 0)
```

### daemon
```
docker run -d -p 8080:8080 -name micro-webman tinywan/docker-php-webman-micro:latest
```

