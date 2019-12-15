# strings_bot
**一个基于 [酷Q](https://cqp.cc/) 及其插件 [cqhttp](https://github.com/richardchien/coolq-http-api) 和 [nonebot](https://github.com/richardchien/nonebot) 的QQ机器人**



- [功能](https://github.com/jinserrr/strings/blob/master/README.md#目前实现的功能有:)
  - [新番](https://github.com/jinserrr/strings/blob/master/README.md#新番)
  - [随机](https://github.com/jinserrr/strings/blob/master/README.md#随机)
  - [翻译](https://github.com/jinserrr/strings/blob/master/README.md#翻译)
  - [签到](https://github.com/jinserrr/strings/blob/master/README.md#签到)
  - [报时](https://github.com/jinserrr/strings/blob/master/README.md#报时)
  - [send](https://github.com/jinserrr/strings/blob/master/README.md#send)
  - [日历](https://github.com/jinserrr/strings/blob/master/README.md#日历)
  - [回应](https://github.com/jinserrr/strings/blob/master/README.md#回应)
  - [搜索](https://github.com/jinserrr/strings/blob/master/README.md#搜索)
  - [scp](https://github.com/jinserrr/strings/blob/master/README.md#scp)
  - [信息](https://github.com/jinserrr/strings/blob/master/README.md#信息)
- [Thanks](https://github.com/jinserrr/strings/blob/master/README.md#Thanks)
  - [以下是在开发过程中给予帮助的~~群友~~朋友们](https://github.com/jinserrr/strings/blob/master/README.md#以下是在开发过程中给予帮助的~~群友~~朋友们)
  - [捐赠列表（按时间先后顺序）](https://github.com/jinserrr/strings/blob/master/README.md#捐赠列表（按时间先后顺序）)
- [捐赠入口](https://github.com/jinserrr/strings/blob/master/README.md#捐赠入口)



### 目前实现的功能有：

#### 新番

  - ##### 新番

    - 指令: **新番** / **新番时间表**
    - 参数：无
    - 例子：**新番**
    - 会话：否
    - 说明：返回 bilibili 的新番时间表

#### 随机

  - ##### 随机数

    - 指令：**随机数**
    - 参数（可选）：【开始数字】 和 【结束数字】, 起始范围为**（-10000, 10000）**，若无参数则为 **（1, 100）**
    - 例子：**随机数 10 999**
    - 会话：否
    - 说明：返回一个随机数字

  - ##### 打乱

    - 指令：**打乱**
    - 参数：想要打乱的字符串（注意需要空格），若加入 **-r** 参数则随机打乱后跟的数字
    - 例子：**打乱 有 一 说 一 ， 确 实** / **打乱 -r 10 999**
    - 会话：否
    - 说明：返回打乱后的字符串

  - ##### 抽签

    - 指令: **抽签**
    - 参数: 想要抽签的内容（需要空格）
    - 例子：**抽签 斯 卡 雷 特 姐 妹 真 可 爱** / **抽签 打游戏 写作业 睡觉**
    - 会话：否
    - 说明：返回随机一个字符串

  - ##### 乐子

    - 指令：**找点乐子** / **找点事做** / **没事找事**
    - 参数：无
    - 例子：**找点乐子**
    - 会话：否
    - 说明：返回一个关于现在可以做什么的建议

#### 翻译

  - ##### 有道翻译

    - 指令：**翻译** / **有道翻译** / **fanyi** / **translate**
    - 参数：要翻译的内容
    - 例子：翻译
    - 会话：是
    - 说明：返回翻译后的内容

#### 签到

  - ##### 注册

    - 指令：**注册**
    - 参数：无
    - 例子：**注册**
    - 会话：否
    - 说明：用于初始化持久化保存数据
    
  - ##### 签到
  
    - 指令：**签到**
    - 参数：无
    - 例子：**签到**
    - 会话：否
    - 说明：返回签到图片，累加数值

#### 报时

- ##### 零点报时

  - 指令：无
  - 参数：无
  - 例子：无
  - 会话：无
  - 说明：零点整报时

#### send

- ##### 发送私聊消息

  - 暂时未开放

- ##### 发送群聊消息

  - 暂时未开放

#### 日历

- ##### 今日历

  - 指令：**今日历**
  - 参数：无
  - 例子：**今日历**
  - 会话：否
  - 说明：返回今天的日历

- ##### 日历

  - 指令：**日历**
  - 参数：日期， 可以是 **明天** 或 **后天**
  - 例子；**日历 明天**
  - 会话：是
  - 说明：返回指定的日历

#### 回应

- ##### 应激反应，包括但不仅限于（其中大部分概率响应）

  - **嘤一下** / **嘤一个** / **来嘤**
  - **喵一下** / **喵一个** / **来喵**
  - **草**
  - **机屑人**
  - **五十弦**
  - **mua**

#### 搜索

- ##### 百度搜索

  - 指令：**百度** / **百度一下**
  - 参数：要百度的内容
  - 例子：**百度 土能吃吗** / **百度一下 失恋了怎么办**
  - 会话：是
  - 说明：返回 百度 的短链接， 调用了微博的短链接服务

- ##### bing搜索

  - 指令：**bing** / **必应**
  - 参数：要必应的内容
  - 例子：**bing ajax** / **bing nonebot**
  - 会话：是
  - 说明：返回 bing 的短链接， 调用了微博的短链接服务

- ##### 不会百度么

  - 指令：**不会百度吗** / **不会百度么**
  - 参数：要搜索的内容
  - 例子：**不会百度吗 bios怎么开啊** / **不会百度么 可以给我发一份吗**
  - 会话：是
  - 说明：返回 不会百度么 的短链接， 调用了微博的短链接服务

#### scp

- ##### scp

  - 指令：**scp** / **Scp** / **SCP**
  - 参数：**最近翻译** / **最近原创** / **随机**
  - 例子：**scp 最近翻译** / **SCP 随机**
  - 会话：是
  - 说明：返回相应的条目

#### 信息

- ##### 历史上的今天

  - 指令：**历史上的今天**
  - 参数：无
  - 例子：**历史上的今天**
  - 会话：否
  - 说明：返回随机一条 历史上今天发生过的某事

- ##### 每日一句

  - 指令：**每日一句**
  - 参数：无
  - 例子：**每日一句**
  - 会话：否
  - 说明：返回 扇贝单词 的 每日一句（中英文）

- ##### five语录

  - 指令：**five语录** / **废物语录** / **二次元语录**
  - 参数：无
  - 例子：**five语录**
  - 会话：否
  - 说明：返回一条语录

- ##### 垃圾分类

  - 指令：**垃圾分类** / **分类**
  - 参数：要分类的垃圾
  - 例子：**分类 垃圾袋** / **~~垃圾分类 我~~**
  - 会话：是
  - 说明：返回垃圾的分类

- ##### 段子

  - 指令：**joke** / **段子** / **笑话**
  - 参数：无
  - 例子：**段子**
  - 会话：否
  - 说明：返回一条~~无聊的~~笑话

- ##### 新闻

  - 指令：**news** / **新闻** / **近闻**
  - 参数：无
  - 例子：**新闻**
  - 会话：否
  - 说明：返回一条新闻

- ##### 天气查询

  - 指令：**天气** / **查天气** / **最近什么天气** / **最近天气怎么样**
  - 参数：【城市】和【日期】
  - 例子：**天气 福州 明天** / **查天气 湖州**
  - 会话：是
  - 说明：返回指定的天气信息

- ##### 知乎日报

  - 指令：**daily_zhihu** / **daily** / **知乎日报**
  - 参数：无
  - 例子：**知乎日报**
  - 会话：否
  - 说明：随机返回一条知乎日报

- ##### 干货

  - 指令：**gank** / **干货** / **整活**
  - 参数：无
  - 例子：**整活**
  - 会话：否
  - 说明：随机返回一条干货

- ##### steam sale

  - 指令：**steam sale** / **steam促销** / **steam优惠**

  - 参数：无

  - 例子：**steam优惠**

  - 会话：否

  - 说明：随机返回一条steam优惠信息

    

***解释***：**会话** 即 **交互式对话**，可以将 **指令** 和 **参数** 分开输入。形式如下：

> user：天气
>
> bot：你想查哪个城市?
>
> user：厦门
>
> bot：你想查哪一天?
>
> user：今天
>
> bot：厦门  晴  15日星期天
> 		 当前温度 17℃
> 		 东风  3-4级
> 		 最高温度23℃
> 		 最低温度15℃
> 		 各项气象条件适宜，无明显降温过程，发生感冒机率较低。

------



### Thanks

#### 以下是在开发过程中给予帮助的~~群友~~朋友们

​	由于人数过多不能全部列出，排名不分先后

- 服务器提供 + 技术支持：[柚子君](https://github.com/zhufree)
- ~~水群~~给予我帮助的群友们
- 投以热心的同学们



#### 捐赠列表（按时间先后顺序）

|  捐赠人  | 捐赠金额（￥） | 捐赠渠道 |
| :------: | :------------: | :------: |
| 川泽黎丶 |      5.20      |   微信   |
|  R4VEN   |      5.00      |   微信   |
| sym1018  |     12.00      |   微信   |



### 捐赠入口

![微信赞赏码](https://github.com/jinserrr/strings/blob/master/appreciated.png)


