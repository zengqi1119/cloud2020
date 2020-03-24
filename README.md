# cloud2020
尚硅谷 springcloud2020 teacher:周阳 视频学习
## 目前进度 zookeeper完结 第31节 


###数据库8.0驱动 mysql
1.集群服务 7001 7002 采用eureka
2.支付集群服务 8001 8002 采用eureka
3.eureka消费者 80 
4.zookeeper消费者 80
5.zookeeper 服务 8004
6.cloud-api-commons 为公共jar

 ####yml 
        7001 单机版 集群版已注释 已经禁用自我保护模式  2s剔除服务
        7002 集群版 
        8001 单机版 注册地址为7001  心跳间隔、等待上限已做修改。为1s、2s
        8002 集群版
        8004单机版
        
####最新更新
         今日新增 使用zookeeper作为注册中心 服务端口8004
         消费zk端口80  
         zookeeper 3.6.0版本
