# my-dianping
## 一、项目介绍
本项目为redis练习项目，仿大众点评。

![image](https://github.com/ldzhang1/my-hm-dianping/assets/104254485/7efe3334-f39f-46fb-8d5c-2085b4f7ac9f)

使用了前后端分离进行开发

![image](https://github.com/ldzhang1/my-hm-dianping/assets/104254485/b888ff73-1c16-4257-b54f-f1f0375ea3be)

#### 项目使用技术：springMVC、springboot、redis、mysql、mybatisplus
### 主要包括以下功能

### * 短信登录
这一块使用redis共享session来实现
### * 商户查询缓存
理解缓存击穿，缓存穿透，缓存雪崩等问题
### * 优惠卷秒杀
通过本章节，我们可以学会Redis的计数器功能， 结合Lua完成高性能的redis操作，同时包含Redis分布式锁的原理，包括Redis的三种消息队列
### * 附近的商户
我们利用Redis的GEOHash来完成对于地理坐标的操作
### * UV统计
主要是使用Redis来完成统计功能
### * 用户签到
使用Redis的BitMap数据统计功能
### * 好友关注
基于Set集合的关注、取消关注，共同关注等等功能
### * 打人探店
基于List来完成点赞列表的操作，同时基于SortedSet来完成点赞的排行榜功能

## 二、项目启动：
### 1.配置数据库
·使用mysql运行 src/main/resources/db/hmdp.sql 下的sql文件，建立表和导入数据
·修改配置文件 src/main/resources/application.yaml 中的mysql数据库和redis配置

![image](https://github.com/ldzhang1/my-hm-dianping/assets/104254485/44057718-d14d-4516-a320-186d141769c3)

### 2.启动后端
·启动项目后，访问localhost:8081/shop-type/list, 如果能够看到数据就表示没问题

### 3.启动前端
·打开src/main/resources/nginx-hmd文件夹，运行nginx.exe文件，然后访问127.0.0.1:8080，即可看到页面
