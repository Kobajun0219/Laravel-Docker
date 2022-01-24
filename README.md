# Laravel-Docker
  Docker、Laravel7系、nginx、mysql8系を利用した環境が構築できます。
  
 #手順
 
 クローンする
 git clone https://github.com/Kobajun0219/Laravel-Docker.git
 
 docker-compose.ymlのある階層で
 
 ```
 docker-compose up -d --build
 ```
 
 コンテナが立ち上がっているか確認

```
docker ps
```

こんな感じで4つコンテナが立ち上がっていればOK
```
CONTAINER ID        IMAGE                       COMMAND                  CREATED             STATUS              PORTS                               NAMES
985bf4968d56        nginx                       "/bin/sh -c 'nginx -…"   3 hours ago         Up 2 minutes        0.0.0.0:80->80/tcp                  app_nginx
ce3884c56d5e        phpmyadmin/phpmyadmin       "/docker-entrypoint.…"   3 hours ago         Up 2 minutes        0.0.0.0:8080->80/tcp                app_pma
b074c9aa9a1f        laravel-nginx-mysql80_web   "docker-php-entrypoi…"   3 hours ago         Up 2 minutes        9000/tcp                            app_php
1456a01d168c        mysql:8.0                   "docker-entrypoint.s…"   3 hours ago         Up 9 seconds        0.0.0.0:3306->3306/tcp, 33060/tcp   app_db
```

下記にアクセスできてLaravelが出ればOK
http://localhost/

