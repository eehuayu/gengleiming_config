```
docker run --name mysql -v /data/release/gengleiming_config/share/mysql/my.cnf:/etc/mysql/my.cnf -v /data/store/mysql:/data/store/mysql -v /data/logs/mysql/:/var/log/mysql/ -e MYSQL_ROOT_PASSWORD=123456 -p 3306:3306 -d mysql:5.7
```
```
docker run --name redis -v /data/release/gengleiming_config/share/redis/redis.conf:/usr/local/etc/redis/redis.conf -v /data/logs/redis/redis.log:/var/log/redis/redis.log -p 6379:6379 -d redis:5.0.4
```
```
docker run --name nginx --net host  -v /data/release/gengleiming_config/share/nginx/nginx.conf:/etc/nginx/nginx.conf -v /data/release/gengleiming_config/share/nginx/gengleiming.conf:/etc/nginx/config.d/gengleiming.conf -d nginx 
```
```
docker run -it --name gengleiming --net host -v /data/release:/data/release -v /data/code:/data/code -d kormay/gengleiming
```