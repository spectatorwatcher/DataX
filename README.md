![Datax-logo](https://github.com/alibaba/DataX/blob/master/images/DataX-logo.jpg)



# DataX

DataX 是阿里巴巴集团内被广泛使用的离线数据同步工具/平台，实现包括 MySQL、Oracle、SqlServer、Postgre、HDFS、Hive、ADS、HBase、OTS、ODPS 等各种异构数据源之间高效的数据同步功能。



# Features

DataX本身作为数据同步框架，将不同数据源的同步抽象为从源头数据源读取数据的Reader插件，以及向目标端写入数据的Writer插件，理论上DataX框架可以支持任意数据源类型的数据同步工作。同时DataX插件体系作为一套生态系统, 每接入一套新数据源该新加入的数据源即可实现和现有的数据源互通。



# DataX详细介绍

##### 请参考：[DataX-Introduction](https://github.com/alibaba/DataX/wiki/DataX-Introduction)



# Quick Start

##### Download [DataX下载地址](http://datax-opensource.oss-cn-hangzhou.aliyuncs.com/datax.tar.gz)

##### 请点击：[Quick Start](https://github.com/alibaba/DataX/wiki/Quick-Start)
* [配置示例：从MySQL读取数据 写入ODPS](https://github.com/alibaba/DataX/wiki/Quick-Start)
* [配置定时任务](https://github.com/alibaba/DataX/wiki/%E9%85%8D%E7%BD%AE%E5%AE%9A%E6%97%B6%E4%BB%BB%E5%8A%A1%EF%BC%88Linux%E7%8E%AF%E5%A2%83%EF%BC%89)
* [动态传入参数](https://github.com/alibaba/DataX/wiki/%E5%8A%A8%E6%80%81%E4%BC%A0%E5%85%A5%E5%8F%82%E6%95%B0)



# Support Data Channels

DataX目前已经有了比较全面的插件体系，主流的RDBMS数据库、NOSQL、大数据计算系统都已经接入，目前支持数据如下图，详情请点击：[DataX数据源参考指南](https://github.com/alibaba/DataX/wiki/DataX-all-data-channels)

| 类型           | 数据源        | Reader(读) | Writer(写) |
| ------------ | ---------- | :-------: | :-------: |
| RDBMS 关系型数据库 | Mysql      |     √     |     √     |
|              | Oracle     |     √     |     √     |
|              | SqlServer  |     √     |     √     |
|              | Postgresql |     √     |     √     |
|              | 达梦         |     √     |     √     |
| 阿里云数仓数据存储    | ODPS       |     √     |     √     |
|              | ADS        |           |     √     |
|              | OSS        |     √     |     √     |
|              | OCS        |     √     |     √     |
| NoSQL数据存储    | OTS        |     √     |     √     |
|              | Hbase0.94  |     √     |     √     |
|              | Hbase1.1   |     √     |     √     |
|              | MongoDB    |     √     |     √     |
| 无结构化数据存储     | TxtFile    |     √     |     √     |
|              | FTP        |     √     |     √     |
|              | HDFS       |     √     |     √     |


# 我要开发新的插件
请点击：[DataX插件开发宝典](https://github.com/alibaba/DataX/wiki/DataX%E6%8F%92%E4%BB%B6%E5%BC%80%E5%8F%91%E5%AE%9D%E5%85%B8)

# 其他

本工程只为简述一个模块化工程构架实现过程，因此删除除stream和mysql之外所有的reader和writer，以保证代码阅读体验

# 代码原始版本

本工程源于之前托管在taocode上的datax工程，当时只支持有限的hbase/hdfs/mysql/oracle/stream等几个主流数据存储格式，其代码路径：
http://code.taobao.org/svn/datax