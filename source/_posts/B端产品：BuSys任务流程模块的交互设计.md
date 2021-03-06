---
title: B端产品：BuSys任务流程模块的交互设计
date: 2017-04-12 13:50:16
tags: 交互
---
# 1.产品目标  
公司旨在以客服系统为中心，建立一个为中小企业信息化办公而打造的平台。BuSys作为一款为企业内各部门打造的任务流转系统，旨通过一套规范的流程，提高企业部门间协作的效率，从而产生长期使用的意愿，积累产品口碑，提高平台的品牌识别度,从而实现利润率的增长。

# 2.业务需求

业务需求是由业务目标和业务目的构成的有机整体,业务需求包括业务业务目标和业务目的两个部分。

<!-- more -->

## 2.1业务目标：企业部门可以通过BuSys系统，实现部门间任务流转。

## 2.2业务目的：通过BuSys降低部门间协作的成本，从而提高企业运作的效率。

{% asset_img 产物呈现.png 产物呈现 %}

# 3.用户目标
用户目标分析过程中，我们可以通过问卷，访谈，现场观察等方法去了解用户的特征,商业项目具体细节就不透露了。

## 3.1角色分析与人物模型

任务流程模块，目标用户是某企业发布任务的A部门，及接受任务的B部门。其中与任务相关的人员：任务发起者、任务审批者、任务执行者、任务验收者。  
根据部门、职能和与场景相关的职能，我们建立了4个典型的人物模型，用于分析和建立情境场景。

{% asset_img 用户模型.png 用户模型 %}

## 3.2用户场景
四个不同的典型人物模型在整个任务流程中会面对不同的使用路径和具体目标。但是整个任务流程中会出现很多的异常情况和支线流程，通过用户场景的梳理，简明地描述四个人物模型使用本模块完成各自任务的过程，并从中关注人物模型的思考和行为方式，对理想的体验进行描述。

{% asset_img 用户场景.png 用户场景 %}  

### 3.2.1核心场景

1.赵刚（任务发布人）   
- 赵刚最近经常收到一些用户关于公司BuSys应用的反馈，赵刚在仔细思索一番后，认为有必要和产品部门提一个需求，改进这个功能点。  

- 赵刚打开电脑，快速进入“发布任务”页面，选择“创建任务”。创建的内容包括：任务类型、接收部门、任务名称、任务描述、任务奖金、任务周期、任务文档、任务留言等关键信息。

- 赵刚在选择任务类型后，系统自动匹配了拥有相应任务接收权限的部门，赵刚选择了自己较为熟悉的产品一部门。  

- 赵刚在看到任务奖金、任务周期时，有点犯难，因为赵刚并不知道这个任务的衡量标准；好在系统根据不同的任务提供了相应的参数范围，赵刚在系统的提示下，完成了相关信息。  

- 赵刚填写完成后，发现需要添加一个任务文档，对该任务进行详细说明。这时赵刚发现可以下载文档的模板，赵刚同时有发现产品一部门的王五也提交了一个相应的任务模板。  

- 赵刚按照王五添加的文档模板填写完整后，上传到了任务中。并在留言板处添加了对任务紧急程度的说明。

- 赵刚点击发布之后，系统提示赵刚任务发布成功，已提交给管理员审核。至此，赵刚的任务已经提交完毕。  

2.张娟（任务审核人）
- 张娟一早正在处理公司报表数据，突然收到一条信息，发现是一条来自BuSys系统发来的任务审核信息。张娟习惯性的打开BuSys系统，进入“任务审核”模块找到赵刚提交审核的任务，张娟仔细查看任务后，发现任务符合平台规范，即点击了通过。

3.赵刚（任务发布人）   
- 赵刚在处理一些技术问题时，收到了BuSys发来的任务审核通过的信息。

4.产品部（任务执行人）  
- 王五手机收到一条来自BuSys系统的信息。王五进入BuSys系统后，发现任务比较合理，即点击了接收。他简单规划后，召集部门成员，开始分配任务的工作。  

- 经过5天的工作，任务已经完成，王五打开任务后，提交了验收申请，并添加了产品说明文档。

5.技术部（任务验收人）  
- 赵刚正在按日常处理用户反馈，突然手机突然收到一条关于任务验收的短信，开发手机后发现是早几天提交给产品部门的任务需要验收。赵刚下载任务文档后，发现产品的设计很符合他内心的预期，便在系统上点击了“确认验收”

6.产品一部（任务执行人）  
- 王五正在和部门成员开会时，收到一条信息，通知王五提交验收的任务已经确认验收，至此，这个任务顺利完成。

### 3.2.2任务审核失败

- 赵刚在发布任务后，提交管理员审核任务。张娟查看相关的任务信息后，发现任务奖金与任务周期之间存在一定的歧义，张娟填写审核信息后，点击驳回了任务。  

- 赵刚正在处理用户反馈时，手机收到一条关于任务审核失败的信息，赵刚打开系统后，仔细查看了审核信息后，重新提交了任务审核。  

- 张娟第二次收到赵刚提交的任务审核，她打开系统后，发现赵刚已经按照规定修改了任务，便点击了“审核通过”。

### 3.2.3拒绝任务

- 王五在收到任务信息后，打开BuSys系统后发现这个任务时间和手上正在执行的任务时间有冲突。在仔细思索后，王五决定暂时先拒绝这个任务，让赵刚在3天后再重新发起这个任务。王五在拒绝理由一栏如实填写了拒绝理由后，提交了请求。    

- 赵刚收到王五拒绝任务的信息后，打开BuSys系统发现王五的拒绝理由比较充分，决定在3天后重新发布任务。

### 3.2.4任务投诉

- 赵刚在收到王五提交的任务拒绝信息后，查看了具体的拒绝理由。发现王五存在故意推脱任务的嫌疑，并且据他所知，王五所说的任务早在三天之前就交付开发了。据此，赵刚决定需要管理员介入。赵刚在投诉理由中，仔细填写投诉理由后，提交了审核。  

- 张娟收到了赵刚提交的投诉信息后，打开系统查看了王五提价的拒绝理由和赵刚提交的投诉理由，并进行了核实。发现赵刚所说情况属实，张娟点击了“通过投诉”。任务被发放到王五的部门，且呈不可拒绝的状态。这时，赵刚和王五都收到了处理结果的信息。

- 张娟在核实后，发现王五反应的情况确实存在，因此张娟填写了处理结果并驳回了赵刚提交的投诉请求。

### 3.2.5任务取消

- 王五在任务执行三天后，因为公司业务需要，需被外派到杭州公出半个月，因此该任务并不能及时完成了。在和赵刚沟通后，王五在BuSys平台提交了任务取消的申请。

- 赵刚收到任务取消的信息后，因为王五已提前和他说明了理由，因此赵刚通过了王五的取消请求。

- 王娟收到任务取消审核的信息后，主动和人事部门的同事进行了联系，发现王五的情况属实，因此通过了该任务取消的请求。

# 4.提炼需求
《About Face 4》中认为需要提炼的设计需求如下：  
（1）数据需求：必须在系统中呈现的对象和信息（账号、用户名、地址、文件、消息、歌曲等）  
（2）功能需求：对系统对象执行的操作或功能  
（3）情境需求：系统中对象之间的关系或依赖、产品的物理环境、人物模型使用产品的技能和能力  
（4）其他需求：企业和技术的现实需求，包括业务需求、品牌和体验需求、技术需求、顾客和合作伙伴需求

为了设计的效率考虑，对本阶段而言，可以将B端产品的需求提炼精简为两个方面：  
（1）信息需求：需要在界面上呈现给用户的数据和信息  
（2）功能需求：需要为用户提供的功能、相应的可操作控件

| 需要设计的页面/推送   | 信息需求    |  功能需求  |
| :--------:            | :-----:     | :----:     |
| 任务发布页面（01）| 任务类型、接受部门、任务名称、任务描述、任务奖金数、任务周期、任务文档、文档模板下载          |   1.选择控件，可以选择拥有相应任务接收权限的部门。2.上传控件，可以上传所需的任务文档。3.点选文档模板后，可以选择和任务类型相匹配的文档模板 
| 任务模板页面（02） | 任务类型名称、任务模板名称、创建者、创建时间 | 1.任务模板下载。2.任务模板类型选择
| 发布成功提示页面（03） | 提示用户成功发布的文案 | 返回任务发布模块首页
| 任务详情页面（04）| 任务类型、任务名称、任务描述、任务奖金数、任务周期、任务文档 | 任务文档下载
| 任务审核页面（05） | 任务发布BU、任务发布时间、任务详情信息 | 1.任务审核按钮。2.返回按钮  
| 任务拒绝页面（06） | 拒绝理由 | 文本输入框、提交按钮
| 拒绝成功提示页面（07） | 提示用户任务拒绝提交成功的文案 | 返回发布处理首页
| 任务验收页面（08） | 验收文档 | 文件上传控件 
| 发布成功提示页面（09） | 提示用户验收提交成功的文案 | 返回任务处理模块首页
| 验收文档下载页面（10） | 验收文档 | 文件下载控件 
| 验收信息提交页面（11） | 验收情况说明 | 文本输入框
| 验收信息提示页面（12） | 提示用户验收信息提交成功的文案 | 返回任务处理模块首页
| 投诉申请页面（13） | 投诉任务、投诉部门、投诉时间、投诉理由 | 文本输入框
| 投诉信息提示页面（14） | 提示用户投诉信息提交成功的文案 | 返回任务发布模块首页
| 投诉处理页面（15） | 处理结果、处理说明 | 1.文本输入框。2.处理结果按钮
| 投诉处理提示页面（16）| 提示用户投诉处理提交成功的文案 | 返回任务投诉模块首页
| 任务取消页面（17） | 取消理由 | 1.文本输入框。2.取消申请提交按钮

# 5.交付物
基于需求提炼以及卡片分类法，将同级页面/元素进行重要性分类，得到了信息结构树状图：

{% asset_img 树状图.png 商业项目已模糊处理 %}

# 6.流程设计篇：接触点，支线和异常
通过需求的提炼，整理得到诸多需要设计中体现的页面、信息和功能后，信息架构设计相当于将这些元素组合成一张地图，而流程设计则是将地图上各个元素沿着不同的任务路径连起来。

{% asset_img 流程图.png 商业项目已模糊处理 %}

==2017年4月19日