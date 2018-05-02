## 分销管理系统

###  引用技术

  guns 权限管理系统

### 适用企业

1、已有项目，需要增加分销功能。

2、项目需要暂时使用分销功能来增加粉丝量，后面可能下线。

3、对接多个系统，需要对多个账户进行控制的系统

### 项目说明

distribution_management  用来运行分销管理系统

plug用来调试接口，调试完成后，可以直接使用

### 安装方法

下载此项目后，将sql中的 两个数据库初始化到本地数据库，然后根据实际情况更新数据库账户和密码。

运行项目即可。

账号 ： admin /111111

​          dist/123

###  项目背景

在互联网项目兴起的大环境下，定制化分销软件的各种样式层出不穷，但是不管何种分销软件都离不开用户等级、代理、分润的形式，我通过自己的总结，意图将所有分销模式抽象画，在后台可配置化，将微服务的模式融入进来，实现系统的可拔插等。

###  经典分销模式
如下图中的分销模式，就可以很好的与本系统对接
![输入图片说明](https://gitee.com/uploads/images/2018/0414/200816_423e5359_1497609.png "未命名文件.png")

### 项目特色

#### 系统可拔插

​      系统以微服务的形式运行，即独立于其他的软件，提供接口进行交互，不会对其他的系统产生新的冗余数据。

​      假设**李老板** 前期需要推广自己的软件，自己的软件又没有设计这个功能，加功能又需要很多钱，这个时候，使用这个软件就可以减少资金的投入（写很少的代码就可以实现自己的需求）。

  系统稳定了，**李老板** 不需要这个分销软件了， 那么可以直接将原来的几行代码关了，或者在自己的系统中增加开关，直接就可以关掉。并且不影响原来的系统的运行。

####  分销配置化

  假设**李老板**  原来只设置一级又分润，后面需要给二级或者三级分润，这个时候只需要在后台进行配置就可以。**李老板** 如果设置原来的配置每笔交易按照百分比收取，后来改为每笔交易按照固定金额收取，就可以直接在后台进行配置。

#### 会员关系可视化

  会员的发展理论上可以无限制的发展下去，并且可以通过树状图表现出来。

#### 分销关系权限化

每个分销商只能看到自己名下的会员。并且可以看到自己的交易明细，这个就减少原有的系统的开发。

会员管理用于查看分销的会员，并且支持图形化查看其关系

![输入图片说明](https://gitee.com/uploads/images/2018/0414/155612_90c66fff_1497609.jpeg "1.jpg")

![输入图片说明](https://gitee.com/uploads/images/2018/0414/155641_9d426b81_1497609.jpeg "2.jpg")

如图很明白的看到了 中国朝代的关系

![输入图片说明](https://gitee.com/uploads/images/2018/0502/205806_11435b20_1497609.jpeg "QQ截图20180502205455.jpg")

接口管理用于提供对接的接口文档

![输入图片说明](https://gitee.com/uploads/images/2018/0414/155749_cff31c2c_1497609.jpeg "3.jpg")
分润设置用于设置分销商的分润 
![输入图片说明](https://gitee.com/uploads/images/2018/0414/160010_69264fa1_1497609.jpeg "5.jpg")

交易查询 ，用于查询相关交易分润

![输入图片说明](https://gitee.com/uploads/images/2018/0414/155829_4f4d13ad_1497609.jpeg "4.jpg")

维护相关分销字典
![输入图片说明](https://gitee.com/uploads/images/2018/0425/222344_946c3f4a_1497609.jpeg "QQ截图20180425222254.jpg")


产品后续规划：
   账户管理（mongodb）
   提现管理(mysql)
   图形界面统计(echarts)
