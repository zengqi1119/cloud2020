# cloud2020
尚硅谷 springcloud2020 teacher:周阳 视频学习
## 目前进度 openFeign完结 第58节 明天开始学习Hystrix
### 数据库8.0驱动 mysql
1. 集群服务 7001 7002 采用eureka
2. 支付集群服务 8001 8002 采用eureka
3. eureka消费者 80 
4. zookeeper消费者 80
5. zookeeper 服务 8004
6. cloud-api-commons 为公共jar
#### yml 
        7001 单机版 集群版已注释 已经禁用自我保护模式  2s剔除服务
        7002 集群版 
        8001 单机版 注册地址为7001  心跳间隔、等待上限已做修改。为1s、2s
        8002 集群版
        8004单机版
        
#### 2020-03-24
         今日新增 使用zookeeper作为注册中心 服务端口8004
         消费zk端口80  
         zookeeper 3.6.0版本

#### 2020-03-25
        新增 consul作为注册中心 服务端口8006
             消费consul端口80
#### 2020-03-26
      新增 ribbon负载均衡
          端口7001 和8001 均改为集群版模式
          80端口创建myrule包为负载均衡策略配置
          80端口lb包为手写自定义轮询负载均衡算法
#### 2020-03-28
      新增 openfeign 消费端口80 8001作为测试
           超时控制 8001端口项目 controller新增超时控制测试方法
           日志配置输出
           脑图上传
#### 2020-03-29
       新增 hystrix 消费端口80
            服务端口8001
            服务降级 @HystrixCommand全局配置
            局部配置、
            @FeignClient(value,fallback)三种方式
