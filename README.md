
# NGenomeSyn
Multi-level visualization of genomic statistical variables on rectangular chromosomes

###  1 Introduction
<b>NGenomeSyn</b> 是于基于多个基因组共线性关系的可视工具，对多个基因组自主排列位置，扩长收缩，旋转角度 等，结合颜色，达到快速一眼看出规律，识别结果。 并且各种可以自己组合 自由修改相关参数。
</br>
</br>亮点：
</br>1  任意多个基因组（目前我限12个，可以取消）
</br>2  各个基因组可以自己调顺序 颜色等等属性
</br>3  各个基因组可以移动 旋转 扩长和收缩等
</br>
</br>其中3  可以调好相关参数 可以出现 三角形  五角形  四边形 等等组合（后面将有空升组调定这些参数）

</br>程序是给一些有基础的生信朋友用的，若是小白看不懂就算了。
</br>
</br><b>NGenomeSyn</b> ,It is a visual tool based on the collinear relationship of multiple genomes, which independently arranges the positions, expansion and contraction, rotation angles, etc. of multiple genomes, combined with colors, to quickly see the rules and identify the results at a glance. And various can be combined by themselves to freely modify the relevant parameters


###  2 Download and Install
------------
The <b>new version</b> will be updated and maintained in <b>[hewm2008/NGenomeSyn](https://github.com/hewm2008/NGenomeSyn)</b>, please click below website to download the latest version
</br><p align="center"><b>[hewm2008/NGenomeSyn](https://github.com/hewm2008/NGenomeSyn)</b></p>

<b> 2.1. linux/MaxOS&nbsp;&nbsp;&nbsp;   [Download](https://github.com/hewm2008/NGenomeSyn/archive/v0.16.tar.gz)</b>
  
  </br> <b>2.2 Pre-install</b>
  </br> NGenomeSyn is for Linux/Unix/macOS only. Before installing,please make sure the following pre-requirements are ready to use.
  </br> 1) [Perl](https://www.perl.org/) with the [SVG.pm](https://metacpan.org/release/SVG) in Perl should be installed. SVG is not necessary,We have provided a built-in SVG module in the package.
  </br> 2) [convert](https://linux.die.net/man/1/convert) command is recommended to be pre-installed, although it is not required

</br> <b>2.3 Install</b>
</br> Users can install it with the following options:
</br> Option 1: 
<pre>
        git clone https://github.com/hewm2008/NGenomeSyn.git
        cd NGenomeSyn;	chmod 755 -R bin/*
        ./bin/NGenomeSyn  -h 
</pre>


###  3 Parameter description
------------
</br><b>3.1 NGenomeSyn</b>
</br><b>3.1.1 Main parameter</b>

```php
        Usage: NGenomeSyn  -InConfi  in.cofi -OutPut OUT

                -InConfi      <s> : InPut Configuration File
                -OutPut       <s> : OutPut svg file result

                -help               See more help *Manual.pdf
                                    [hewm2008 v0.16]

```
</br> brief description for function:
<pre>
	   # 用法和circos相似，主要一个配置文件一样,具体见pdf，简要功能介绍如下
	1  任意多个基因组（目前我限12个，可以取消）
	2  各个基因组可以自己调顺序 颜色等等属性
	3  各个基因组可以移动 旋转 扩长和收缩等
	
	其中3  可以调好相关参数 可以出现 三角形  五角形  四边形 等等组合（后面将有空升组调定这些参数）
	   
</pre>

</br><b>3.1.2 Other parameters</b>
```php
     输入文件基因组格式见  pdf.主要为chr start end 等其它属性 的格式
     输入link件基因组格式见  pdf.主要为chrA  startA enda chrB startB endB   等等其它属性 的格式

```

</br><b>3.2.2 Detail parameters</b>
```php
	#  具体见pdf
##################################### 全局参数 #######################################################
SetParaFor = global
GenomeInfoFile1=RefA.info
###### Format (chr Start End ...其它属性)  chr顺序和这文件一致 若是End Start 则这条chr反向互补
##  其它属性 如fill=red stroke-width=0  stroke=black stroke-opacity=1 fill-opacity=1 等等可以不同行不同属性
GenomeInfoFile2=RefB.info  ##  GenomeInfoFile X  就表示有 X个基因组

LinkFileRef1VsRef2=Link
####### Format (chrA StartA EndA chrB StartB End ...其它属性)
#  可以多次Ref1VsRef2   LinkFileRef2VsRef1 等


##Main = "main_Figure"  ##  the Fig Name  :MainRatioFontSize MainCor ShiftMainX  ShiftMainY 
## font-size 

################################ Figure ############################################################

##############################     画布 和 图片 参数配置 #################################
#body=1200   ##   默认是1200，主画布大小设置  另外：up/down/left/right) = (55,25,100,120); #CanvasHeightRitao=1.0 CanvasWidthRitao=1.0
##RotatePng   = 0  ##  对Figure进行旋转的角度

SetParaFor = Genome1  #  ALL/GenomeX  X第X个基因组

#ZoomChr=1.0          ## chr长度 等大 缩小 or 扩大
#RotateChr=30         ## chr的起点 顺时针 旋转  xx 度
#ShiftX=0
#ShiftY=0             ##对这个基因组移动,也可以直接用MoveToX MoveToY 

#ChrWidth=20          ## 这个基因组chr的在画布的宽度
#LinkWidth=180        ## 这个基因组和下一个link的高度
#ChrSpacing=10        ## 这个基因组chr之间的空隙
#NormalizedScale=0    ## 用自己的标尺  相当该基因组与默认的基因组是否等长

#SpeRegionFile=        ## 文件,表记特别区域[格式chr start End （xx=yy加属性等]

##其它当很少用到的参数 EndCurveRadian=3/ 等等
## GenomeNameRatio GenomeName

SetParaFor = Genome2  #  ALL/GenomeX  X第X个基因组
SetParaFor=Link1  #  靠X� Link X  File 靠靠
#StyleUpDown=           ## UpDown  DownUp  UpUP DownDown  靠靠
#Reverse=1              ## 靠link
#HightRation=1.0        ## links靠靠  靠or靠
####  fill/ stroke/stroke-opacity/fill-opacity/stroke-width  靠

....  #等等


```

</br><b>3.3 Output files</b>
<pre>
out.svg: Output plot in SVG format
out.png: Output plot in png format
</pre>


###  4 Example
------------

</br>See more detailed usage in the&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <b>[Chinese Documentation](https://github.com/hewm2008/NGenomeSyn/blob/main/任意展示多基因组共线性程序NGenomeSyn_manual_chinese.pdf)</b>
</br>See more detailed usage in the&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <b>[English Documentation](https://github.com/hewm2008/NGenomeSyn/blob/main/任意展示多基因组共线性程序NGenomeSyn_manual_chinese.pdf)</b>
</br>See the example directory and  Manual.pdf for more detail.
</br>具体见这儿  Manual.pdf for more detail 里面的实例和配置，后期将在某些网址释放一些教程
</br></br> 
../../bin/NGenomeSyn       -InConfi        in.cofi -OutPut OUT
</br>  目录  Example/example*/　里面有输入和输出和脚本用法。


* Example 1)两个基因组默认
最简易，默认居中。
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example1/OUT.png)

* Example 2) 三个(N个)基因组默认 
两层  即 画text 层和 高亮层两种配合。   其中高亮层的背色条宽度缩小了点.
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example2/OUT1.png)


* Example 3)三个(N个)基因组默认  排列 旋转等
旋转 第三个基因组
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example2/OUT2.png)


* Example 4)  任务排列
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example3/OUT.png)
有数据可以出下图
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example3/test.jpg)




###  5 Advantages

</br>速度快，少内存
</br>可以自我定义组合多层次
</br>有perl即可以运行，免安装


###  6 An example image generated by NGenomeSyn.

------------



###  7 Discussing
------------
- [:email:](https://github.com/hewm2008/NGenomeSyn) hewm2008@gmail.com / hewm2008@qq.com
- join the<b><i> QQ Group : 125293663</b></i>

######################swimming in the sky and flying in the sea #############################

