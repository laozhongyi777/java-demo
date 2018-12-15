# java-demo

#### ci/cd 架构图
https://github.com/laozhongyi777/java-demo/blob/master/picture/1.png





#### java 发布流水线

https://github.com/laozhongyi777/java-demo/blob/master/picture/2.png
#### devops各个环节：

##### 1.环境概述

1.包括使用到主要组件组件：

​	gitlab，Jenkins，harbor，k8s，nfs

2.服务器配置推荐2和4G

3.服务器规划

IP                                                                 角色

10.206.240.111                                     Node01

10.206.240.112                                    Node02

10.206.240.188                                   Master01，Harbor

10.206.240.189                                   Master02，Git，NFS

10.206.176.19                    Internal Loadbalancer

27.115.124.xxx                   External Loadbalancer





##### 2.基本环境配置

1.包括jdk和maven

2.配置注意软件版本限制，apache-maven-3.5.3-bin.tar.gz  apache-tomcat-8.5.31.tar.gz  jdk-8u45-linux-x64.tar.gz





##### 3.git

1.安装git 即可

2.如需工作使用建议gitlab，构建自动化ci/cd

3.代码仓库一定是自动定时备份和网络多主机存储文件





##### 4.harbor部署

1.可配置双主保证高可用

2.尽量简化在开发环境的使用难度

3.安全采用域名加证书访问



##### 5.Jenkins配置

1.添加k8s、gitlab、docker、认证相关插件安装

2.所有相关文件使用git管理

3.构建并发量大使用Jenkins slave 

4.版本管理使用git tag来管理









