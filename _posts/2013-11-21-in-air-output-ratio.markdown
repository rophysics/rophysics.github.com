---
layout: post
title: 空气输出因子及测量
category: radiation
tags: radiation
---
#### 射野输出因子

射野输出因子是放射物理中的重要概念，主要是用于机器跳数——MU值（Machine Unit）的计算，为什么呢？因为处方剂量是肿瘤组织的吸收剂量（Absorbed Dose），但这是考虑各种衰减因素（距离平方反比、指数衰减）和散射因素（准直器、铅门、模体）后得到的最终值，那么机器在出束时应该有多少的量，才能在去除各个因素的影响后，靶区（CTV，PTV）得到预订的处方量？这里用机器跳数表示这个机器量，Gy是吸收剂量的单位，用在机器中不适合，所以称作重新设计一个机器单位，一般在校准时，会将1MU在数值上校准为1cGy（例如在标准野刻度机器时，给机器200MU，静电计测得的值应在200cGy），计算时需要考虑的就是两部分——原射线和散射线，散射线的产生主要来自：准直器（包括初级准直器、二级准直器），上下的铅门、电离室、均整器、楔形板、模体等。射野输出因子就是描述这些散射的影响程度的，其中包括了两种因素，一个是模体外的因子![equation][1]（in-air output ratio）和模体散射因子![equation][2]（phantom scatter factor），现在要说的是前者——空气中的输出因子。    

#### 空气输出因子的定义和测量  

空气输出因子定义为测量野和参考野的自由空间中释放的比释动能比值，又称作准直器散射因子（Collimator scatter factor），但是根据TG74的报告，还是建议使用空气输出因子（in-air output factor），历史上，![equation][1]主要是在用TMR计算MU值时，使用建成套在最大剂量点深度测量得到的，而TG74的报告建议使用小模体（Miniphantom）在一定深度（没有电子污染）上测量，因为建成套不能完全阻挡电子污染的影响。另外，测量前要考虑的还有模体的材料，因为在测量小野时，模体需要完全被照射野覆盖，同时又要满足防止电子污染的要求，就必须选用高原子序数的材料，但是有研究证明，用不同的材料可能造成射线能谱的改变，需要引入一个校正因子。TG74报告建议在射野大于5cm时使用水等效的模体就行，当射野小于5cm时，建议使用高原子序数的材料。  

测量时的射野设置可见下图，图例的电离室在模体下10cm，模体高20cm，直径4cm。参考射野大小为10cm：   

![measurement][4]  

因为测量只跟射野大小相关，所以![equation][3]的影响可以省略，使用以下的公式即可算出![equation][1]:  

![equation][8]

#### 影响因素  

根据TG74的报告，影响![equation][1]的主要因素有以下几个：  

-  来自均整器和主准直器的散射（Flattening filter and primary collimator）  
-  楔形板和补偿器（Wedge and compensator）  
-  治疗准直器的散射和漏射  
-  电离室的背向散射（Monitor）  
-  源湮灭效应（Source obscuring effect）：这个效应一般在非常小的野和低能时出现  

这些部件的位置可以在下图找到：  

![position][5]  

有很多文章试图定量的分析不同散射部分所占的比重，这一般需要使用蒙卡技术模拟和分析，文章结果显示主准直器的散射贡献要比均整器的多，而上下铅门都会对电离室的背向散射有所贡献，关于蒙卡技术的模拟以后再有机会看看。  

文章主要参考了一下两篇：  

1: [quantitative analysis of in-air output ratio][6]    

2: [Report of AAPM Therapy Physics Commitee Task Group 74][7]   

[1]: http://latex.codecogs.com/gif.latex?\inline&space;S_{c}
[2]: http://latex.codecogs.com/gif.latex?\inline&space;S_{p}
[3]: http://latex.codecogs.com/gif.latex?\inline&space;K_{Q}
[4]: http://farm3.staticflickr.com/2866/11047643343_a21caca98f_n.jpg
[5]: http://farm8.staticflickr.com/7443/10963403803_f0ae7e47eb.jpg
[6]: http://jrr.oxfordjournals.org/content/early/2013/01/03/jrr.rrs118.full.pdf
[7]: http://www.aapm.org/pubs/reports/RPT_97.pdf
[8]: http://latex.codecogs.com/gif.latex?\inline&space;S_{c}(A)=\frac{M(A)}{M(A_{_{ref}})}
