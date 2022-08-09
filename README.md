# 柚城后台管理系统

#### 介绍
该项目是基于前后端分离的开发模式，基于Vue技术栈的SPA单页面项目，后端主要操作数据库并向前端暴露一些API接口，前端主要负责绘制页面同时，利用Ajax调用后端提供的接口具体实现功能有：用户管理、权限管理、商品管理、订单管理以及销售数据统计
#### 技术栈
vue+vue-router+element-ui前端组件库+axios发起网络数据请求+echarts绘制相关的图形报表+MySQL+NodeJs


#### 页面展示
登录页面：（默认账户密码：账户：admin 密码：123456）
![登录](https://user-images.githubusercontent.com/74812275/183593513-4628f08f-4a40-4aa3-99e9-381092562d98.png)


欢迎页面：
![欢迎](https://user-images.githubusercontent.com/74812275/183593578-8a77a8b9-2eb7-4abe-b083-fdf1c8c44ae8.png)


用户列表：（包括添加，删除，修改功能，分配角色（默认为超级管理员且不可删除））
![用户列表](https://user-images.githubusercontent.com/74812275/183593619-83989b04-d228-47b7-af98-e538eaf86043.png)


权限管理：（权限列表，角色列表）
![角色列表](https://user-images.githubusercontent.com/74812275/183593662-d8ad8a23-6e5a-4909-8ebd-283220f89ec3.png)

![权限列表](https://user-images.githubusercontent.com/74812275/183593714-b9987757-5708-47e4-bb59-20874b94adc9.png)



商品管理：（商品列表，分类参数，商品分类）
![商品列表](https://user-images.githubusercontent.com/74812275/183593755-1d942aa7-09dd-4a90-a467-e3cedb83dc2e.png)

![分类参数](https://user-images.githubusercontent.com/74812275/183593802-07267add-09b1-4b66-a1fe-7b63f8df7033.png)


![商品分类](https://user-images.githubusercontent.com/74812275/183593833-66f6bddd-e8bf-45f3-a4a7-51222550fef6.png)



订单管理
![订单列表](https://user-images.githubusercontent.com/74812275/183593854-9339a42f-6671-4574-a644-1bb56afffdd6.png)


物流信息（接口暂时请求不到）：
![物流进度](https://user-images.githubusercontent.com/74812275/183593873-bd81f7f2-9b4e-4571-8038-4edae2044efe.png)


数据分析：
![数据报表](https://user-images.githubusercontent.com/74812275/183593917-f428d83c-0706-44c6-a728-d93bf8906a83.png)



#### 使用说明

1. 环境：VScode Nodejs，导入项目后（看是否有node_modules文件夹），若没有在终端运行 npm i
2.  在创建的vue项目目录下运行cmd 输入 vue ui即可打开可视化工具
插件：

![插件](https://user-images.githubusercontent.com/74812275/183593971-384e421a-f0fc-4289-b764-8084178bf8b0.png)

依赖：

![依赖](https://user-images.githubusercontent.com/74812275/183594006-8689a4e7-1f45-49d5-8682-15a74530a8f6.png)


3.  服务器启动(需要mysql数据库，数据库文件在db文件夹下)，进入服务器目录 运行cmd 输入 node ./app.js
成功界面：
![服务器启动成功界面](https://user-images.githubusercontent.com/74812275/183594026-ed6462b0-b3f3-46cd-892c-3c0c7e290be2.png)





