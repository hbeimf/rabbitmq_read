

wget http://www.rabbitmq.com/releases/rabbitmq-server/v3.6.10/rabbitmq-server-generic-unix-3.6.10.tar.xz


xz -d ./rabbitmq-server-generic-unix-3.6.10.tar.xz

tar xvf ./rabbitmq-server-generic-unix-3.6.10.tar


```
$ cd ./rabbitmq_server-3.6.10/sbin

启动web插件
$ ./rabbitmq-plugins enable rabbitmq_management

启动mq
$ ./rabbitmq-server

以守护进程启动mq
$ sudo ./rabbitmq-server -detached

停止节点

$ sudo ./rabbitmqctl stop

```

web管理页面

http://127.0.0.1:15672/

账号密码：
guest guest


可以创建管理员用户，负责整个MQ的运维，例如：

$ ./rabbitmqctl add_user  admin  123456

赋予其administrator角色：

$ ./rabbitmqctl set_user_tags admin administrator


查看users

```
maomao@maomao-ThinkCentre-E73:/web/rabbitmq_read/rabbitmq_server-3.6.10/sbin$ ./rabbitmqctl list_users
Listing users
guest   [administrator]

```

各种版本的客户端demo

https://github.com/rabbitmq/rabbitmq-tutorials


