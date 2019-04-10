# docker-redis
Run redis service for docker
使用 docker 快速部署 redis 服务，设置持久化。

# start
clone 这个仓库，在此仓库目录下运行命令
```shell
$ docker run -p 6379:6379 --name redis6379 -v $PWD/conf.d:/usr/local/etc/redis -v $PWD/data:/data -d redis redis-server --appendonly yes
```
