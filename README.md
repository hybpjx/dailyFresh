# dailyFresh

>天天生鲜项目，很早以前做的一个Django的小项目 依赖于 1.8版本 
并且 此项目有些东西BUG居多 比如

- fastdfs 的 配置（配置地狱 解决完一个BUG就出另一个BUG 好不容易你搞出来 了，部署时候又会出现一大堆问题。）
- 在用户创建的时候 Django 提供的create_user 在1.8的时候会有各种小问题蹦出来，哦？ 你不用1.x 不好意思 本项目依赖于1.8 如果你强行要用2.2以上版本 ，那不好意思 很多东西都要重写 可能 除了前端 后端的所有东西 都需要人眼过一遍。我们可以用 django的models自带的object.get.create()来创建


> 本项目 pip安装东西包括但不局限于
> 
> celery jieba django django-redis Pillow pymysql uwsgi tinymce

> 环境配置的内容有
>
> fastdfs mysql redis nginx 


# 项目架构

## 页面说明：

1. index.html 网站首页，顶部“注册|登录”和用户信息是切换显示的，商品分类菜单点击直接链接滚动到本页面商品模块。首页已加入幻灯片效果。此效果在课程中已讲述如何制作。
2. list.html 商品列表页，商品分类菜单鼠标悬停时切换显示和隐藏，点击菜单后链接到对应商品的列表
3. detail.html  商品详情页，某一件商品的详细信息。
4. cart.html 我的购物车页，列出已放入购物车上的商品
5. place_order.html 提交订单页
6. login.html 登录页面
7. register.html 注册页面，已加入了初步的表单验证效果，此效果在课程中已讲述如何制作。
8. user_center_info.html 用户中心-用户信息页 用户中心功能一，查看用户的基本信息
9. user_center_order.html 用户中心-用户订单页 用户中心功能二，查看用户的全部订单
10. user_center_site.html 用户中心-用户收货地址页 用户中心功能三，查看和设置用户的收货地址

**前端**

用户相关 商品相关 购物车相关 订单相关 后台管理

**后端**

用户模块 商品模块 购物车模块 订单模块 后台管理模块

**其他**

数据库 mysql

session 缓存服务器  django-redis redis

异步任务处理  celery

分布式文件存储系统  fastdfs
