# ChatServer

工作在nginx配置tcp负载均衡环境中的集群聊天服务器和客户端源码，基于muduo网络库，redis缓存服务器，mysql数据库编程开发

# 编译方式

cd build

rm -rf *

cmake ..

make

或者添加自动化运行脚本

./autobuild.sh


# 项目技术

基于cmake构建自动化编译环境

基于Json第三方库进行数据的序列化和反序列化，简化了程序设计，增加了程序的可读性

基于muduo网络库编程开发，实现服务器的网络IO模块、业务模块、数据模块的分层设计

基于nginx配置tcp负载均衡器实现了服务器的集群

基于redis缓存服务器中间件的发布-订阅消息队列实现了跨服务器通信，实现松耦合

基于mysql数据库编程实现信息存储和增删改查


# 目录介绍

bin目录存放可执行文件（ChatServer/ChatClient）

buid目录存放cmake构建的文件

src目录存放项目的源文件

include目录存放项目的头文件

thirdparty目录存放第三方库

