---
comment: true
---
## ②提升篇-使用Components在Obsidian中搭建物品管理系统

> [!info] 前情提要
通过初级篇的教程，大家能够搭建出基础的物品管理系统，实现利用看板对不同位置的物品进行展示
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E5%B0%81%E9%9D%A21.png)
同时能够达到基本的==增删查改==功能

> [!note] 搭建一个基础的物品管理系统
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E9%80%9A%E8%BF%87%E4%BD%8D%E7%BD%AE%E6%9D%A5%E5%B1%95%E7%A4%BA.png)


>本篇教程将会进一步提升，重点关注==属性的使用==，展示Components是如何通过==属性==实现物品的更进一步管理的

---

## 1 展示更多属性

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240908090613.png)
> 现在的==物品管理系统==是根据不同的**位置属性**进行分组展示的，我们可以在此基础上，展示==更多想要关注的属性==，比如说购入这些物品的开销、购入的时间、数量等

1. 首先点击属性的配置界面
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240911161828.png)


2. 点击添加属性，添加我们已经在物品文档的属性栏中填写好的，我们想要展示的属性，这里用==金额==这个属性来演示。
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240911161909.png)

3. 另外对于添加的属性，Components还可以编辑后缀，比如==金额==是个数字属性，我们可以添加一个==元==的后缀，就能显示为==XX元==
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240911162222.png)

---


## 2 选择其他分组展示

>上一步骤实现了展示**更多属性**，现在利用填写的属性切换到另一个分组进行展示，比如说刚刚使用的属性是不同的**位置**，现在可以实现使用另一个属性——不同的**品牌**来展示

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240917225207.png)

上图为==基于位置==的分组，此图为==基于品牌==的分组
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240917225358.png)
**修改分组的步骤如下**：

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E7%82%B9%E5%87%BB%E5%88%86%E7%BB%84.png)


1. 点击配置界面的分组，修改原来的==分组条件==为品牌属性
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240917225938.png)

2. 接着勾选我们要展示出的品牌的属性，就能得到基于品牌展示的物品
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240917225358.png)

---

## 3 日历化展示

>本篇的第一个教程实现了物品的更多属性的展示，对于添加的日期属性，还可以配合==数据视图==的==日历==视图实现对物品的**日历化展示**


---

1. 点击数据视图的配置按钮，切换为日历显示

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240917223426.png)

2. 回到主界面，然后点击==选择属性==

> [!help] 此处“选择属性”的作用
> ==日历视图==需要指定一个日期类型的属性来筛选文件
> 因此选择你想要限定的属性即可
> 比如我现在想看这些物品都是哪天入库的，稍后我选择==入库时间==即可






3. 这时我们选择==入库时间==



![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240917223933.png)


就能够以日历的形式显示具体哪天入库的物品



![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E6%97%A5%E5%8E%86%E5%8C%96%E5%B1%95%E7%A4%BA.gif)


> [!bug] 推荐在移动端呈现：
> 这个视图推荐在手机端或者电脑的侧边使用（如上图），全宽的显示效果如下，其实不太好😁
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240917224354.png)

---
## 进阶篇预告




> [!danger] ③进阶篇内容
> 1.展示物品图片，物品管理更加直观
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E5%AE%8C%E6%95%B4%E7%89%88.png)
> 2.利用公式属性计算物品还有多久过期
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240918093248.png)
> 3.利用JS脚本快速增减物品数量
> ![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E5%A2%9E%E5%8A%A0%E5%87%8F%E5%B0%91%E6%B5%8B%E8%AF%95.gif)





