---
layout: post
title: 剂量验证中的γ分析
category: radiation
---
在放射治疗中，我们必须保证TPS中计算的剂量分布与实际在人体中沉积的一致，所以需要进行剂量验证分析，现在普遍使用的是γ分析（gamma analysis），为解释这个概念，有必要先说一下先前的两种剂量分析方法，即DD法（Dose-difference）和DTA法（Distance-to-agreement），这两种方法非常容易理解：  

首先，我们需要先拿到要比较的数据，一个是计算机算出来的Dc， 一个是我们测到的（现在常用的有矩阵和EPID测量）Dm，当然两种分布的分辨率是不一致的，比如从计算机导出的数据是512\*512的，矩阵达到的可能只有29\*29个。测完两组数据，就可以比较了。  
DD比的是剂量差别，用测到的点的剂量与其位置相对应的计算点的剂量相比较，如果两者差异在计算点的3%以内（在这里计算点为参考剂量，剂量容忍误差为3%），那么可以认为这一个点是准确的，即通过检验；DTA也是要找到与位置的相对应的点，如果在这一点以3mm为半径（在这里位置容许误差为3mm，对二维验证来说）的圆内找到与测量点相等剂量的点，那么也通过检验。  

但是这两种方法都有其不足之处，DD法在剂量梯度很大的位置不太准确——因为一旦存在误差，那么剂量的差异会很大，这个点不能通过检验，所以DD法常用在剂量平缓区；同理，DTA法在剂量平缓区不准确——剂量平坦的话，会出现即便位置误差较大，那么仍然可以在一定的距离内找到所需要的对应点，所以会高估剂量分布的通过率，同样的道理，DTA对剂量梯度大的范围有更好的准确性。  

γ分析弥补了两者不足，对任意测量点，寻找计算点中的值都结合这两个因素考虑，γ分析的公式在最后参考论文中有论述，为了说明这种方法的准确性，通过对参考剂量分布进行位置/剂量的偏移，然后通过剂量验证方法进行验证，参考论文中也举了足够的例子。

这种思想可以用在其他QA上，比如测量加速器输出稳定性时，有一个时间γ分析，这里将距离的概念替换成时间，因此γ的定义就变为： 

<span class="imgcenter">![tima gama analysis][2]</span>

Update, 在分析软件中（如 Mapcheck），Gamma分析有Global 和 Local 之分，这是由于在计算剂量误差时（例如3%），有两种计算方法，一种是两个对应点的剂量差比这一点的计算值（local point）得到一个百分数，一种则是比这个层面的最大剂量值（计算点）（Global）显然，我们知道用Global方法计算出的值小于等于Local方法算出的偏差，因此通过率会比Local方法高出很多，可以看以下图[^1]：

![Global VS Local](..\images\pr.jpg)

以及PTW软件得到的误差值：

![PTW](..\images\ptw.jpg)

参考论文：[A technique for the quantitative evaluation of dose distributions] [1]   


 [1]: http://personal.us.es/alberto/ffisim/material/gamma_index.pdf "Reference"

 [2]: https://farm8.staticflickr.com/7479/15191234054_b34b24198b_o.jpg

[^ 1 ]: 来自：Moving beyond 3%/3mm gamma criterion for IMRT/VMAT patient specific QA 作者：J. Hindmarsh等.