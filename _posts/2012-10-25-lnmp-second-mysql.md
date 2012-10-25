---
layout: post  
title: "LNMP环境搭建（二） 编译安装MySQL"  
description: "LNMP环境搭建（二） 编译安装MySQL"  
category: LNMP
tags: [LNMP, MySQL]  
---
**编译安装MySQL**  

1. 创建组和用户
>groupadd mysql  
>useradd -g mysql mysql  

2. 解压源码包并进入  
>tar zxvf mysql-5.5.3-m3.tar.gz  
>cd mysql-5.5.3-m3  

3. cmake配置编译参数  
>cmake -DCMAKE_INSTALL_PREFIX=/usr/local/mysql \  
>-DSYSCONFDIR=/usr/local/mysql/etc   \  
>-DMYSQL_DATADIR=/usr/local/mysql/data \   
>-DMYSQL_TCP_PORT=3306 \   
>-DMYSQL_UNIX_ADDR=/tmp/mysqld.sock \   
>-DMYSQL_USER=mysql \   
>-DEXTRA_CHARSETS=all \   
>-DWITH_READLINE=1 \  
>-DWITH_SSL=system \  
>-DWITH_EMBEDDED_SERVER=1 \  
>-DENABLED_LOCAL_INFILE=1 \  
>-DWITH_INNOBASE_STORAGE_ENGINE=1 \  
>-DWITHOUT_PARTITION_STORAGE_ENGINE=2  

4. 编译安装
>make && make install  

5. 将安装目录极其子目录的所属组和拥有者设置为mysql:mysql  
>chown -R mysql:mysql /usr/local/mysql   
>cd ..  

6. 以mysql用户帐号的身份建立数据表：  
>cd /usr/local/mysql 
>./scripts/mysql_install_db --basedir=/usr/local/mysql --datadir=/usr/local/mysql/data --user=mysql  

 如果执行成功会出来一堆提示信息。  

 现在你已经成功安装了MySQL。你可以用如下命令启动MySQL：   
>./support-files/mysql.server start   

 用下面的命令访问MySQL：   
>./bin/mysql  

 你应该已经发现我们成功登录了Mysql，但是没有提供用户名密码。这样的话任何人都可以登录了，这肯定不是你想要的。 

7. 可以通过一下命令来为root设置密码  
>/usr/local/mysql/bin/mysqladmin -u root password '123123'

 我们的密码是123123。  
 这样再执行`./bin/mysql`的时候就会提示你需要密码了。

8. 好了，这就完事了。
