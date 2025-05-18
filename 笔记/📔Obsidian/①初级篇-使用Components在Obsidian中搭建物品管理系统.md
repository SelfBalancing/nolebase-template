---
comment: true
tags:
  - obsidian/components
link: https://mp.weixin.qq.com/s/9o7IFytcw1uk6peW0e9r4g
finished: 2024-09-19
---


# 前言


每次出差，在收拾整理必带的物品时，翻箱倒柜地找各种东西，然后再装进自己的行李箱、手提包和背包中


> [!Todo] 找一件物品通常经历以下过程：
> 1. 想这个东西大概在什么位置
> 2. 然后去第一个地方去找，找到了就跳到步骤4，没找到就跳转到步骤3
> 3. 到下一个地方继续寻找，找到了就跳到步骤4，没找到继续本步骤
> 4. 太好了，终于找到了😂


一件物品通常要找很久，找到后就放到自己要带走的箱包中，一会儿又再想，某件物品到底放进去没啊，放进去的话自己又放到哪个包里了，又得找一遍😂


> [!DANGER] 在出差的路上，我就开始思考这个问题。
怎么才能**简单方便**地管理好自己的物品呢？


我也找了不少的手机软件，但是**自由度不高**，且大多需要**付费**。

我想着使用Obsidian搭建一个，但是里面涉及大量的**Dataview代码**又把我劝退。

这时适逢**@vran**更新了**Components**的1.8.0版本，里面一个更新的功能一下子打开了我的思路。
通过这个功能，将笔记拖拽到别的分组，相应的属性就能变为该分组。
联想到物品管理方面，如果把物品当成一个笔记，那么这就是一种结构比内容更重要的笔记，配置好相应的储存位置属性，物品的转移只需通过简单、直观的拖拽即可实现。


> [!DANGER] 基于Components插件，我搭建了一个物品管理系统。
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E5%AE%8C%E6%95%B4%E7%89%88.png)

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E5%B0%81%E9%9D%A2%E5%A4%A7%E5%9B%BE.png)


现在将此系统的搭建教程分享于此，同时相应的组件已打包成示例库，下载后放入自己激活后的**Components**插件即可使用


> [!DANGER] 更多内容
> 1. 公众号后台回复**物品管理系统**，即可获得完整示例库
> 2. 文章较长，预计会分为三个篇章进行分享，敬请关注
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240918114235.png)
> 后续更新
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240918114536.png)


# 搭建基础的物品管理系统

## 1.1 创建物品笔记的模板
在这里，我们**每一个物品**用**一个笔记**来表示，笔记的属性就对应物品的各种性质，比如说位置、价格、数量等

我们新建一个模板文件，然后在属性区添加文档属性

注意选择好对应的属性类别，比如说**入库日期**，就应该选择日期类型




> [!Tip] 接下来演示一个最最基础的物品管理系统
> 属性中只包含位置
> 且限定物品只有一件，只在一个位置


创建一个文件夹，文件夹名为物品，然后将刚刚创建的模板文件复制粘贴一份到该文件夹，之后修改文件名并填写文件的位置属性：


> [!NOTE] 这样，一个名为雨伞的物品文件就创建好了
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240905225408.png)

## 1.2 创建看板组件
接下来使用**Components**插件创建一个**数据视图**组件
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240905224242.png)

在数据视图中选择看板
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240905224417.png)


接下来点进视图配置，设置为小卡片、封面暂时设为**无**
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240905224802.png)

接下来配置筛选的部分，填写条件为：文件路径包含物品
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240905225622.png)


点击**分组**，设置分组条件为刚刚设置的属性**位置**
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240907232210.png)


![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240905225919.png)


接着在当前界面，勾选彩色分组，同时将**行李箱**分组进行展示。
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240907232657.png)


> [!success] 这时你就能获得这样的看板视图
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240907232824.png)

`推荐使用看板视图，因为此视图有一种抽屉的感觉，方便折叠和滑动`



现在我们完成了一个最基本的物品管理系统，接下来我们提高**增加物品的速度**。

## 1.3 快速新建物品模板
点击组件的设置按钮，打开配置面板
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240907233828.png)

首先点击**模板**，然后添加模板，选择刚刚设置好的**新物品模板**
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240907234001.png)
然后在点击模板的右侧三个小点---，将其设置为默认模板
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240907234130.png)
> [!HELP] 模板的作用：一键添加新物品
> 此操作是为了使你能够在以后点击组件右上角的**新建**按钮时，都能自动调用这个模板，不用自己再反复的复制副本了。




然后我们再点击配置面板的**新建笔记位置**的**无**紫色区域（下方）



![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240907233828.png)



在配置界面中，选择物品的文件夹
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240907234723.png)


> [!HELP] 设置新建笔记位置
> 这样以后需要添加新的物品进来时，只需点击**新建**按钮，然后就会自动在**物品**文件夹中创建一个模板文件，然后再自行填写内容和修改物品名即可
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240907234926.png)

当前的位置属性只有**行李箱**，如果你增加新的位置属性，比如说**书包**，记得重复之前的步骤，将**书包**的分组属性进行展示

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240908090358.png)


再添加几个物品进去，这时**物品管理系统**已经有了大致的形状
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240908090613.png)

> [!danger] 新建物品的小技巧
> 此时在**看板**界面，也能快速新建物品，只需点击各个分组下的**新建**按钮即可
而且你在**手提包**分组下新建，那么此文件的**位置**属性会自动填写成**手提包**，更加方便快捷
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240908090941.png)


---
再分享一个快速创建分组属性的方法
> [!danger] 快速创建新分组
> 滑到组件的右侧，点击添加分组，即可快速添加新的分组属性
应用场景如下，比如说你发现有一个新的存放物品的位置——储物箱，你就可以直接在此处新建一个**储物箱**的分组属性，然后再接着快速新建**储物箱**中的物品
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240908112951.png)



## 1.4 物品管理系统的基本功能
一个**物品管理系统**需要具备基本的**增删查改**功能，刚刚的1.3已经实现了增加的功能，要想删除掉物品只需在组件的界面点击物品右侧的三个小圆点···，选择删除即可

> [!tip] 删
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240908113936.png)

---



> [!tip] 查
> 需要进行🔍时，直接在组件的左上角的放大镜即可进行，同时此查询附带**临时筛选**功能，可以**限制**查询物品的条件，可以更加**快速**地查找到相应物品
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240908114709.png)
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240908115129.png)

---

> [!tip] 改
> 如果是要对展示的**分组属性**进行修改，比如说，你要将牛仔外套从行李箱转移手提包中，你可以点进笔记中修改**位置**属性，将行李箱修改为手提包
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240908125453.png)

但是这里有更加简单直观的方法

> [!danger] 通过拖拽实现修改
> 直接拖拽物品，然后移动至相应位置即可修改展示的分组属性
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E6%8B%96%E6%8B%BD%E4%BF%AE%E6%94%B9%E5%B1%9E%E6%80%A71.gif)

---



# 下篇预告
初级篇的内容如上，通过本篇教程，你已经搭建出自己的物品管理系统，并且实现了利用看板进行展示

> [!note] 一个基础的物品管理系统
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E9%80%9A%E8%BF%87%E4%BD%8D%E7%BD%AE%E6%9D%A5%E5%B1%95%E7%A4%BA.png)

同时能够实现基本的**增删查改**



> [!danger] ②提升篇内容
> 1.展示更多属性，多角度了解物品
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240918130345.png)
> 2.选择其他分组展示，展示更多一个维度
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240917225358.png)
> 3.日历化展示，掌握入库时间
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E6%97%A5%E5%8E%86%E5%8C%96%E5%B1%95%E7%A4%BA.gif)




> [!danger] ③进阶篇内容
> 1.展示物品图片
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E5%AE%8C%E6%95%B4%E7%89%88.png)
> 2.利用公式属性计算物品还有多久过期
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240918093248.png)
> 3.利用JS脚本快速增减数量
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E5%A2%9E%E5%8A%A0%E5%87%8F%E5%B0%91%E6%B5%8B%E8%AF%95.gif)



