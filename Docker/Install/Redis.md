# Docker Redis安装

- 创建实例
````
docker run -p 6380:6379 --name 容器名 -v /user/redis.config:/etc/redis/redis.conf -tid 镜像id redis-server /etc/redis/redis.conf --appendonly yes
````
-v 挂载是因为要设置密码，没有找到直接使用docker run中添加密码的方式
或者在redis里面创建密码，可以在笔记[数据库redis模块](/DataBase/Redis/Root.md)中查看

appendonly yes是持久化设置