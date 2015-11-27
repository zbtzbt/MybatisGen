# Mybatis Generator demo

Mybatis受到很多java开发者的青睐，本工程为自动生成Mybatis代码的小demo。

## 使用说明

1.生成本demo中的persion表映射：在sqlserver2008 R2中，执行doc/sql目录下sql脚本，生成数据库表。</br>
  生成你远程数据库或者本机localhost数据库的表映射：请直接配置config.properties。

2.配置config.properties:  
jdbc.driverLocation  jdbc驱动本地地址，本demo 用的sqlserver2008 R2数据库，数据库驱动为sqljdbc4-3.0.jar,其他数据库请自行本地download对应数据库的驱动。  
jdbc.driverClass 数据库驱动类  
jdbc.connectionURL 数据库连接url  
jdbc.userId 数据库用户名  
jdbc.password 密码

4.配置generatorConfig.xml中需要映射的表名tableName:
<xmp><table tableName="" enableCountByExample="false" enableDeleteByExample="false" enableSelectByExample="false" enableUpdateByExample="false"/></xmp>

3.在工程目录下执行:mvn mybatis-generator:generate -e  
  即在target目录下Generator code