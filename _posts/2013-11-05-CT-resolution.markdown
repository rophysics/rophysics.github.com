---
layout: post
title: CT的密度分辨力和空间分辨力
category: radiation
tags: radiation-physics
---
最近参加CT考试，经常看到图像处理方面常用的两个参数，即空间分辨力（spatial resolution）和密度分辨力(contrast resolution)，有些书里又叫空间分辨率和密度分辨率，这两个概念容易混淆，且在这里区别总结一下：  

### 空间分辨力  

这是我们平常最常用的概念，我们说“像素很高”，就是指的空间分辨力很高，因此，空间分辨力是分辨最小物体（CT中叫组织）的能力，它代表了能显示的最小信息点的大小，因此像素越小，图像就越能让人“看得清晰”  。  

在CT中，它跟什么因素有关呢？主要有以下几方面：  

-  设备本身 探测器的数目（即采集矩阵）越多，那么采集的点相对越小，那么空间分辨力越高，X线的焦点尺寸越小，那么产生的X线越窄，空间分辨力越高  
-  扫描层厚 通过准直器我们可以调节扫描的层厚，层厚越小，那么采集点的尺寸越小，同时由于容积效应的减小，最小组织细节不容易被掩盖  
-  重建算法 一般CT提供了好几种重建算法，用于不同组织的诊断，高分辨力的算法，可以提高显示细小结构的能力，如内耳道、肺部一些小结节的显示  

那么，实际操作中如何来测量一个图像的空间分辨力？一般都是用模体测量，有两种方法，一种原理：  

-  线对法 这是最常用的方法，模体使用很细小的针排成几排，放在由塑料或者有机玻璃制作的模体中，扫描后就形成了黑白相间的线对，辨别出最小针距的线对数（LP/cm）就是这幅图像的空间分辨力了。  
![线对法][1]  

-  圆孔法 这次模体里面填充的是几排高密度物质排列的圆孔，两个圆孔中心距离是直径的两倍，测量能分辨出的最小一排圆孔，找到对应的分辨力数值就得到了。  
![圆孔法][2]  

### 密度分辨力

它表示是对比度相近的两种组织能不能分辨出来的能力，相比空间分辨力“有多能看清组织”，它的能力就是“有多能分清组织”，它在CT中的影响因素主要有：  

-  噪声 就是信噪比的大小，如果探测器得到的X线很少，那么信息量就很少，如果噪声很大，那么图像会变得模糊，所以想提高密度分辨力可以提高X线的强度，或者降噪，对于体型很胖的病人，一般就要增加X强度  
-  扫描层厚 同样，如果扫描层厚很小（虽然空间分辨力高了），但是X线的量减少了，密度分辨力就降低了，增加层厚能增加密度分辨力  
- 后期处理 重建算法中的平滑算法可以增加密度分辨力，但同时降低了空间分辨力，通过显示的窗口技术，我们可以调节到两种组织密度分辨力尽可能大的程度  

密度分辨力的测量办法是圆孔法，这种模体中有很多圆柱形的大小不一的孔，他们的CT值有所差别，当你能找到最小分辨的两个孔时，你计算一下两个孔的密度差百分率（%），就得到了密度分辨力值。  

![圆孔法][3]  

从Wikipedia上拿来一张图，可以清晰的显示密度分辨力不同的变化：分别为5.1%、3.7%、 2.2%、1%  

![示例][4]

最后要说一下CT上岗证的参考书，简直错误百出，逻辑也很混乱，很多地方讲得不清楚，复习时要注意，我的复习笔记[在这里][5]，以供后用，里面把我记得今年考试的条目都更新了记号。  

[1]: http://farm4.staticflickr.com/3748/10684519304_fd2cd12727_n.jpg
[2]: http://farm3.staticflickr.com/2844/10684461195_480361ecf2_n.jpg
[3]: http://farm3.staticflickr.com/2871/10684517016_dcd765e4d5_n.jpg
[4]: http://farm4.staticflickr.com/3686/10684509434_d63e95856c.jpg
[5]: http://www.evernote.com/shard/s74/sh/e39b95f8-94d3-402e-9889-1e75ab857022/122ff4cd5cc830923477fc7c9fbb6d09


