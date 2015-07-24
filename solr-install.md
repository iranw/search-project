# solr5.2安装教程(linux)

### 1、安装java(>1.7)
```
$sudo yum install java-1.7.0-openjdk
```

验证安装是否成功
```
[vagrant@localhost ~]$ java -version
java version "1.7.0_85"
OpenJDK Runtime Environment (rhel-2.6.1.3.el6_6-x86_64 u85-b01)
OpenJDK 64-Bit Server VM (build 24.85-b03, mixed mode)
[vagrant@localhost ~]$ 
```

### 2、安装solr
下载solr
```
$ wget -c http://mirrors.cnnic.cn/apache/lucene/solr/5.2.1/solr-5.2.1.tgz
```
`下载地址`:[http://lucene.apache.org/solr/mirrors-solr-latest-redir.html](http://lucene.apache.org/solr/mirrors-solr-latest-redir.html)

解压
```
$ tar -zxvf solr-5.2.1.tgz
$ cd solr-5.2.1
```

常用command
```
$./bin/solr start           #启动   
$./bin/solr -help           #帮助文档
$./bin/solr start -help     #特定命令帮助文档
$./bin/solr start -f        #前端运行
$./bin/solr start -p 8984   #特定端口启动
$./bin/solr stop -p 8984    #关闭特定端口solr服务
$./bin/solr -e techproducts #绑定特殊配置
$./bin/solr status          #查看搜索引擎状态
```


### 3、打开solr web管理页面
`URL`:http://localhost:8983/solr/
