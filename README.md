# 带配置文件使用 docker 启动 redis 服务
使用 docker 快速部署带配置文件的 redis 服务，设置持久化。

# Usage
conf.d: redis 配置文件目录，目录下放置了 Redis 4.0 版本的配置文件 

data: 持久化数据目录

1、clone 这个仓库，在此仓库目录下运行命令

```shell
$ docker run -p 6379:6379 --name redis6379 -v $PWD/conf.d:/usr/local/etc/redis -v $PWD/data:/data -d redis redis-server --appendonly yes
```



