# 需求规格说明书

<br/>

## 修订历史记录

<br/>

 日期 | 版本 | 说明 | 作者
:---:|:---:|:----:|:---:
2017.11.5  | V1.0  | 第一个版本，根据项目形成基本构架 | Java演绎法
2017.11.12 | V1.1  | 添加选车和选音乐界面，完善开始界面，加入数据结构相关内容 | Java演绎法

<br/>

## 0. 目录

* [需求规格说明书](#需求规格说明书)
* [修订历史记录](#修订历史记录)
    * [0. 目录](#0-目录)
    * [1. 引言](#1-引言)
        * [1.1 目的](#11-目的)
        * [1.2 背景](#12-背景)
        * [1.3 定义](#13-定义)
        * [1.4 参考文献](#14-参考文献)
    * [2. 项目概述](#2-项目概述)
        * [2.1 产品描述](#21-产品描述)
        * [2.2 产品功能](#22-产品功能)
        * [2.3 用户特点](#23-用户特点)
            * [2.3.1 用户示例场景](#231-用户示例场景)
            * [2.3.2 用户需求分析](#232-用户需求分析)
        * [2.4 假定和约束](#24-假定和约束)
            * [2.4.1 假定](#241-假定)
            * [2.4.2 约束](#242-约束)
    * [3. 具体需求](#3-具体需求)
        * [3.1 功能需求](#31-功能需求)
            * [3.1.1 界面设计](#311-界面设计)
                * [开始界面](#开始界面)
                * [选车界面](#选车界面)
                * [游戏界面](#游戏界面)
                * [通关界面](#通关界面)
                * [结束界面](#结束界面)
        * [3.2 外部接口需求](#32-外部接口需求)
            * [3.2.1 用户接口](#321-用户接口)
            * [3.2.2 硬件接口](#322-硬件接口)
            * [3.2.3 软件接口](#323-软件接口)
            * [3.2.4 通信接口](#324-通信接口)
        * [3.3 性能需求](#33-性能需求)
            * [3.3.1 精度需求](#331-精度需求)
        * [3.4 属性](#34-属性)
            * [3.4.1 可用性](#341-可用性)
            * [3.4.2 可维护性](#342-可维护性)
    * [4. 验证验收标准及相关要求](#4-验证验收标准及相关要求)
        * [4.1 验收标准](#41-验收标准)
            * [4.1.1 文档验收标准](#411-文档验收标准)
            * [4.1.2 软件验收标准](#412-软件验收标准)
            * [4.1.3 界面验收标准](#413-界面验收标准)
            * [4.1.4 功能验收标准](#414-功能验收标准)
            * [4.1.5 游戏验收标准](#415-游戏验收标准)
        * [4.2 灵活性](#42-灵活性)
        * [4.3 时间特性需求](#43-时间特性需求)
        * [4.4 其它要求](#44-其它要求)

<br/>

## 1. 引言

<br/>

### 1.1 目的

<br/>

- 经过一个半学期的java学习与Android Studio的自学过程，我们迫切地需要清楚地了解自身知识的掌握程度与运用能力，于是我们在老师的引导下开始了此次做游戏的实践任务。

- 本游戏app的定义为休闲游戏，基于Android平台。编写本功能需求说明书的目的是为了详尽呈现出该游戏的用户需求、设计理念与游戏特性分析；明确包含游戏性质、软件运行界面、功能需求、代码编写特点的描述，便于用户、开发人员的协调工作，并在此基础上进一步提出概要设计说明书，建立可确认、可验证的一个基本依据，以完成后续的设计与开发工作。

- 本文档面向的预期读者范围与阅读建议：
1. 项目经理：项目经理根据该文档了解预期产品的功能，并据此进行系统设计、项目管理。
2. 程序员：了解需求的程序特点与系统功能。
3. 测试员：根据本文档作出测试用例，对软件进行功能性测试与非功能测试。
4. 用户：清晰了解软件使用方式，

<br/>

### 1.2 背景

<br/>

- 项目开发单位：北京电子科技学院2016级23班一组学生

- 本次待开发的软件为休闲游戏类软件。
本游戏软件将被投放至应用市场供群众下载，用户使用该软件进行娱乐，放松身心，锻炼手脑协调能力与反应能力。

<br/>

### 1.3 定义

<br/>

 序号 | 缩写 | 定义
---|--- |----- 
1 | app      | 应用程序，Application的缩写，一般指手机软件
2 | Android   | Android是一种基于Linux的自由及开放源代码的操作系统，主要是使用移动设备，如智能手机和平板电脑，由Google公司和开放手机联盟领导及开发。

<br/>

### 1.4 参考文献

<br/>

- 《报课系统软件需求规格说明书》

- 《报课系统需求规格说明书》

- 《一起买APP需求规格说明书》

<br/>

## 2. 项目概述

<br/>

### 2.1 产品描述

<br/>

- 该游戏是基于Android平台开发的app。该2D赛车躲避障碍物游戏可用于锻炼手指灵活度，提高反应速度与敏捷度。

<br/>

### 2.2 产品功能

<br/>

- 功能介绍图（WBS）：

- ![image](http://ww2.sinaimg.cn/large/0060lm7Tly1flldbdohp3j30ut0iimy6.jpg)


该产品为平面2D赛车游戏，用户可通过手指移动自己的车辆躲避出现的车辆和障碍物，也可以通过发射子弹来消除它们，游戏目标是得到更高的分数。

<br/>

### 2.3 用户特点

<br/>

本产品使用于一切能独立使用Android手机的用户。适用于想要放松，喜欢尝试锻炼敏捷性游戏的用户。

<br/>

#### 2.3.1 用户示例场景

<br/>

- 用户场景A：小明是一名高中生，周末放假回家闲来无事，和朋友用各自的手机玩游戏，想要比比谁的分数高。

- 用户场景B：小王是一个公司职员，上午上了半天班有点累，中午休息的时候不知道干什么，于是拿出了手机玩了几分钟小游戏来放松一下。

<br/>

#### 2.3.2 用户需求分析

<br/>

- 场景A：小游戏有趣，游戏结束后能显示成绩，能比较玩家得分。

- 场景B：小游戏操作简单，不需要费神去学习和使用，能用于闲暇时的放松和打发时间。

<br/>

### 2.4 假定和约束

<br/>

#### 2.4.1 假定

<br/>

1.可操作性：假定本游戏用户在试玩后能很快灵活操作游戏。
   
2.用户支持：假定在本游戏开发的各个环节中得到用户的有效支持和配合。
   
3.技术支持：假定开发初期，小组成员成分认识游戏的需求，认真学习相关知识。假定在开发过程中遇到问题，可以及时得到老师的指导与帮助。

4.人员配合：假定小组成员不会出现变动，并且在项目开发过程中不会有突发情况的发生而导致项目成员无法正常参与开发工作。

5.时间限定：假定项目的截止时间不会提前。

6.需求限定：假定项目需求基本确定之后，不会有太大改变。

<br/>

#### 2.4.2 约束

<br/>

- 人员约束：
团队成员均为大二学生，共6人。

- 管理约束：
1.本次开发，实行以一人担任小组组长，各组员分工合作的模式进行。每个人负责切实具体的流程板块，并且按照进度表进行，开发过程中遇到的问题通过小组会议得到一致的解决。
2.小组成员首次合作，需要明确责任，互相配合，迅速度过磨合期。在遇到问题时需要小组组长能进行有效的协调，才能快速，有效地完成开发过程。

- 技术约束：
1、小组成员在相关技术水平方面存在一定欠缺，缺乏相关项目经验，在文档编制能力方面也有待提升。
2、小组成员在美工方面，能力有限。

- 时间约束：
本系统开发周期较短，时间相对紧张。

- 其他约束：
由于在开发期间，小组成员还有其他科目的学习任务，将对项目进度造成一定的影响。

<br/>

## 3. 具体需求

<br/>

- ![image](http://ww2.sinaimg.cn/large/0060lm7Tly1fllea5161rj310m0lg3za.jpg)

### 3.1 功能需求

<br/>

#### 3.1.1 界面设计

<br/>

#### 开始界面

<br/>

- 用户选择开始游戏亦或是结束游戏：

![输入图片说明](https://gitee.com/uploads/images/2017/1112/100009_38f719a5_1107099.png "屏幕截图.png")
 
<br/>

#### 选车界面
 
<br/>

- 在用户点击选车界面之后，会有四辆不同型号的赛车来让用户选择。并且每辆赛车下面都有赛车的名字，可以通过搜索框来对赛车进行搜索的方式来选择。

![输入图片说明](https://gitee.com/uploads/images/2017/1116/085717_9f4b4657_1107011.jpeg "111.jpg")

<br/>

#### 游戏界面

<br/>

- 在游戏界面中，用户可以同过指尖在屏幕上滑动来移动自己的车辆，来躲避随机出现的车辆和障碍。用户同时也可以同过子弹来消灭挡路的车辆。

![输入图片说明](https://gitee.com/uploads/images/2017/1112/100411_722d4501_1107099.png "屏幕截图.png")
 
- 用户点击右上角的M键可以进入背景音乐选择界面，在提供好的音乐列表中选择自己感兴趣的、喜欢的背景音乐。界面中已存在音乐，用户点击后自动更换，按后退键取消音乐选择。在未选择下，游戏背景音乐默认只有一首。

![输入图片说明](https://gitee.com/uploads/images/2017/1112/100456_d403fca0_1107099.png "屏幕截图.png")

- 用户点击右上角的暂停键的时候会出现选项让用户选择继续游戏亦或是退出当前游戏返回主界面。

![输入图片说明](https://gitee.com/uploads/images/2017/1112/100521_06ec7ca0_1107099.png "屏幕截图.png")

<br/>

#### 通关界面

<br/>

- 在用户顺利同过所有关卡后，会出现这样一个弹窗。用户可以在界面看到自己的分数。点击“确认后会回到开始界面”：

![输入图片说明](https://gitee.com/uploads/images/2017/1112/100557_f9a14895_1107099.png "屏幕截图.png")

<br/>

#### 结束界面

<br/>

- 若用户中途被击中，会出现结束界面。用户按“确认”可回到主界面。

![输入图片说明](https://gitee.com/uploads/images/2017/1112/100618_a4783e20_1107099.png "屏幕截图.png")
 
<br/>

### 3.2 外部接口需求

<br/>

#### 3.2.1 用户接口

<br/>

无特殊需求。

#### 3.2.2 硬件接口
	
<br/>

无特殊需求。

#### 3.2.3 软件接口

<br/>

无特殊需求。

#### 3.2.4 通信接口

<br/>

无特殊需求。

### 3.3 性能需求

<br/>

#### 3.3.1 精度需求

<br/>

|      项目  | 精度| 
| --------   | :----------------:|
| 躲避一个障碍物        |10
| 躲避一辆车辆或击破一辆车辆      |20   
| 关卡数      |20   
|关卡1-->关卡2      | 10          |
| 关卡2-->关卡3      | 250          |
| 关卡3-->关卡4      | 375          |
| 关卡4-->关卡5      | 525          |
| 关卡5-->关卡6      | 700          |
| 关卡6-->关卡7      | 900          |
| 关卡7-->关卡8      | 1125          |
| 关卡8-->关卡9      | 1375         |
| 关卡9-->关卡10      | 1650          |

- 每过一个关卡，分数不会清零，会一直累积

1.	用户控制的车辆不能移到道路外。
2.	障碍物或障碍车辆碰撞用户车辆的判断要精确。
3.	子弹与障碍车辆接触判断要精确。
4.	障碍物和障碍车辆要出现在道路内。
5.	子弹的发射位置要在用户车的中见
6.	子弹发射的频率和速度要合理。

<br/>

### 3.4 属性

<br/>

#### 3.4.1 可用性

<br/>

1.	易操作，易理解。界面设计简洁易用。
2.	操作完成时有统一规范的提示信息。

#### 3.4.2 可维护性

<br/>

1.	保留系统的源代码
2.	代码注释详细，包括方法实现过程以及变量的含义。
3.	清晰的系统结构和命名规范，界面规范。
4.	每次调试都会记入日志。
5.	不断从各方面操作进行测试。

<br/>

## 4. 验证验收标准及相关要求

<br/>

### 4.1 验收标准

<br/>

#### 4.1.1 文档验收标准

<br/>

（1）app项目开发计划

（2）软件需求说明书

（3）团队项目及时记录和总结报告（团队博客）

<br/>

#### 4.1.2 软件验收标准

<br/>

APP安装包

<br/>

#### 4.1.3 界面验收标准

<br/>

| 序号 | 界面名称 | 界面描述 | 备注 |
| --- | --- | --- | --- |
| 1 | 开始界面 | 页面上半部分标题栏显示游戏名称&quot;&quot;，中间部分从上至下依次有按钮&quot;闯关模式&quot;和按钮&quot;结束游戏&quot;。 |   |
| 2 | 选车界面 | 页面分为左上，右上，左下，右下四个板块，每个板块是用户需要选择的车辆按钮 |   |
| 3 | 游戏边框界面（两边） | 页面左边框是动画效果处于移动中的路旁的画面，左边框上部有提示栏&quot;关卡：XXX&quot;与&quot;分数：XXX&quot;,页面右边框同是动画效果处于移动中的路旁的画面，右边框上部有按钮暂停框&quot; ‖&quot;和&quot;♬&quot; |   |
| 4 | 游戏主界面（中部） | 中部界面有方形的人工移动光标&quot;车&quot;，界面上方有系统随机产生自上而下规律移动的光标&quot;汽车&quot;和&quot;障碍&quot;，主界面背景为动画效果样式处于移动中的道路（分4条主道）。 | &quot;汽车&quot;和&quot;障碍&quot;属于不同类型，详见功能说明部分 |
| 5 | 暂停界面 | 该界面大小约为主界面的三分之一，上部有状态提示语&quot;暂停&quot;，下部左右依次有按钮键&quot;继续&quot;和&quot;退出&quot; |   |
| 6 | 音乐界面 | 该界面含有多首音乐的按钮 |   |
| 7 | 返回界面 | 该界面与暂停界面相同位置及大小，上部有提示语&quot;是否返回&quot;，下部分左右依次有按钮键&quot;是&quot;与&quot;否&quot;。 | 由暂停界面&quot;退出&quot;键进入返回界面 |
| 8 | 结束界面 | 界面为弹出框，框上部有提示语&quot;游戏结束&quot;和&quot;你的最终分数是：XXXX分&quot;，框下部有按钮键&quot;确认&quot; |   |
| 9 | 通关界面 | 界面为弹出框，有结语&quot;恭喜你！你已通关！&quot;和&quot;你的最终分数是：XXXX分&quot;，框下部是按钮键&quot;确认&quot;。 |   |

<br/>

#### 4.1.4 功能验收标准

<br/>

| 序号 | 功能名称 | 操作界面 | 详细操作 | 备注 |
| --- | --- | --- | --- | --- |
| 1 | 进入游戏 | 开始界面 | 点击&quot;闯关模式&quot;转入游戏界面 |   |
| 2 | 结束游戏 | 开始界面 | 点击&quot;结束游戏&quot;退出游戏回到手机上一级主界面 |   |
| 3 | 游戏 | 开始界面、选车界面、游戏界面 | 通过点击&quot;闯关模式&quot;进入选车界面，点击想要使用的车辆进入游戏界面，手机通过屏幕感应移动光标躲避从上到下迎来的障碍物和车辆，避免碰撞 |   |
| 4 | 计分 | 游戏边框界面、结束界面、通过界面 | 每躲避一个障碍物加10分，躲避或消灭一个车辆加20分，达到一定的分数标准则进入下一关，左边框上部实时记录游戏关卡以及得分，若碰撞障碍物则即时停止计分。在游戏左边框界面上部、通关界面和结束界面会显示游戏得分 | 若碰撞障碍物则即时停止计分，转入结束界面 |
| 5 | 选歌 | 游戏界面、音乐界面 | 点击游戏界面右上角的&quot;♬&quot;符号进入音乐界面，点击界面内任何一首歌曲则背景音乐切换到该歌曲，用户点手机的返回键回到上一界面 | 初始背景音乐默认为第一首歌曲的单曲循环 |
| 6 | 暂停 | 暂停界面、游戏边框界面、开始界面、返回界面 | 点击游戏右边框界面上部&quot;‖&quot;按钮进入暂停界面弹出框，点击&quot;继续&quot;返回游戏界面继续游戏，点击&quot;退出&quot;则弹出返回界面框 |   |
| 7 | 返回 | 暂停界面、返回界面、开始界面 | 在暂停界面点击&quot;退出&quot;按钮进入返回界面，点击&quot;是&quot;则回到开始界面，点击&quot;否&quot;则返回暂停界面 |   |
| 8 | 通关 | 游戏界面、通关界面 | 在游戏界面通过所有关卡后进入通关界面，点击&quot;确认&quot;返回开始界面 |   |
| 9 | 结束 | 游戏界面、结束界面、开始界面 | 在游戏中碰撞到障碍物及车辆会进入结束界面，点击&quot;确认&quot;则返回开始界面 |   |

<br/>

#### 4.1.5 游戏验收标准

<br/>

| 序号 | 功能名称 | 操作界面 | 详细操作 | 备注 |
| --- | --- | --- | --- | --- |
| 1 | 光标移动 | 游戏界面 | 用户通过按住屏幕&quot;车&quot;通过滑动改变其位置 |   |
| 2 | 环境 | 游戏界面、游戏边框界面 | 进入游戏后游戏界面背景&quot;公路&quot;实现移动状态，游戏边框界面的路旁景象实现移动状态，二者要求同步移动速率 |   |
| 3 | 车辆障碍 | 游戏界面 | 实现&quot;车辆&quot;和&quot;障碍&quot;两种不同类型的&quot;敌人&quot;，使二者随机出现，以不同速率从游戏界面上部进入，垂直向下移动，直至移出界面 |   |
| 4 | 射击 | 游戏界面 | 用户操纵的车辆可以发射垂直向上&quot;导弹&quot;，击中车辆会使消失并产生爆炸效果 |   |
| 5 | 音乐 | 后台 | 开始界面设置音乐&quot;Alone&quot;，游戏界面设置音乐&quot;Open Window&quot;(音乐界面的第一首歌),当有其他界面弹出框出现则暂停播放 |   |

<br/>

### 4.2 灵活性

<br/>

本软件最终完成后，短期内需求不会发生太大变化。相应地，即当需求发生某些变化时，该软件具备对这些变化的适应能力：操作方式上的变化。本系统的操作方式相对简单，用户可以很容易掌握。 在系统前期的需求分析和交互设计方面已经做了充分的考虑和设计，一般不会发生太大的变化。不过我们可以根据用户需求的变化，做一些更改和扩充，具有比较好的扩展性。

<br/>

### 4.3 时间特性需求

<br/>

此APP对时间特性的要求不高，只需在合理时间内响应用户的请求即可。例如点击按钮反应时间不得超过1s等。

<br/>

### 4.4 其它要求

<br/>

#### 安全要求：

不会向用户索要个人信息，尽量提示APP本身的安全性

<br/>

#### 可靠性：

系统具有较强的稳定性，不存在太多的不稳定因素。

<br/>

#### 使用方便要求：

（1）该系统的所有界面要简洁且易用。

（2）操作完成时有统一规范的提示信息。

<br/>

#### 可维护性：

（1）保留系统的源代码

（2）代码注释详细，包括方法实现过程以及变量的含义。

（3）清晰的系统结构和命名规范，界面规范。

（4）每次调试都会记入日志。

（5）：全面考虑系统，加强后期的维护，不断从各方面操作进行测试。

<br/>

#### 性能需求：

（1）用户控制的车辆不能移到道路外。

（2）障碍物或障碍车辆碰撞用户车辆的判断要精确。

（3）子弹与障碍车辆接触判断要精确。

（4）障碍物和障碍车辆要出现在道路内。

（5）子弹的发射位置要在用户车的中见

（6）子弹发射的频率和速度要合理。
