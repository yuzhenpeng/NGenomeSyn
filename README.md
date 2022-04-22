
# NGenomeSyn
Multi-level visualization of genomic statistical variables on rectangular chromosomes

###  1 Introduction
<b>NGenomeSyn</b> ���ڻ��ڶ�������鹲���Թ�ϵ�Ŀ��ӹ��ߣ��Զ����������������λ�ã�������������ת�Ƕ� �ȣ������ɫ���ﵽ����һ�ۿ������ɣ�ʶ������ ���Ҹ��ֿ����Լ���� �����޸���ز�����
</br>
</br>���㣺
</br>1  �����������飨Ŀǰ����12��������ȡ����
</br>2  ��������������Լ���˳�� ��ɫ�ȵ�����
</br>3  ��������������ƶ� ��ת ������������
</br>
</br>����3  ���Ե�����ز��� ���Գ��� ������  �����  �ı��� �ȵ���ϣ����潫�п����������Щ������

</br>�����Ǹ�һЩ�л��������������õģ�����С�׿����������ˡ�
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
	   # �÷���circos���ƣ���Ҫһ�������ļ�һ��,�����pdf����Ҫ���ܽ�������
	1  �����������飨Ŀǰ����12��������ȡ����
	2  ��������������Լ���˳�� ��ɫ�ȵ�����
	3  ��������������ƶ� ��ת ������������
	
	����3  ���Ե�����ز��� ���Գ��� ������  �����  �ı��� �ȵ���ϣ����潫�п����������Щ������
	   
</pre>

</br><b>3.1.2 Other parameters</b>
```php
     �����ļ��������ʽ��  pdf.��ҪΪchr start end ���������� �ĸ�ʽ
     ����link���������ʽ��  pdf.��ҪΪchrA  startA enda chrB startB endB   �ȵ��������� �ĸ�ʽ

```

</br><b>3.2.2 Detail parameters</b>
```php
	#  �����pdf
##################################### ȫ�ֲ��� #######################################################
SetParaFor = global
GenomeInfoFile1=RefA.info
###### Format (chr Start End ...��������)  chr˳������ļ�һ�� ����End Start ������chr���򻥲�
##  �������� ��fill=red stroke-width=0  stroke=black stroke-opacity=1 fill-opacity=1 �ȵȿ��Բ�ͬ�в�ͬ����
GenomeInfoFile2=RefB.info  ##  GenomeInfoFile X  �ͱ�ʾ�� X��������

LinkFileRef1VsRef2=Link
####### Format (chrA StartA EndA chrB StartB End ...��������)
#  ���Զ��Ref1VsRef2   LinkFileRef2VsRef1 ��


##Main = "main_Figure"  ##  the Fig Name  :MainRatioFontSize MainCor ShiftMainX  ShiftMainY 
## font-size 

################################ Figure ############################################################

##############################     ���� �� ͼƬ �������� #################################
#body=1200   ##   Ĭ����1200����������С����  ���⣺up/down/left/right) = (55,25,100,120); #CanvasHeightRitao=1.0 CanvasWidthRitao=1.0
##RotatePng   = 0  ##  ��Figure������ת�ĽǶ�

SetParaFor = Genome1  #  ALL/GenomeX  X��X��������

#ZoomChr=1.0          ## chr���� �ȴ� ��С or ����
#RotateChr=30         ## chr����� ˳ʱ�� ��ת  xx ��
#ShiftX=0
#ShiftY=0             ##������������ƶ�,Ҳ����ֱ����MoveToX MoveToY 

#ChrWidth=20          ## ���������chr���ڻ����Ŀ��
#LinkWidth=180        ## ������������һ��link�ĸ߶�
#ChrSpacing=10        ## ���������chr֮��Ŀ�϶
#NormalizedScale=0    ## ���Լ��ı��  �൱�û�������Ĭ�ϵĻ������Ƿ�ȳ�

#SpeRegionFile=        ## �ļ�,����ر�����[��ʽchr start End ��xx=yy�����Ե�]

##�����������õ��Ĳ��� EndCurveRadian=3/ �ȵ�
## GenomeNameRatio GenomeName

SetParaFor = Genome2  #  ALL/GenomeX  X��X��������
SetParaFor=Link1  #  ��X� Link X  File ����
#StyleUpDown=           ## UpDown  DownUp  UpUP DownDown  ����
#Reverse=1              ## ��link
#HightRation=1.0        ## links����  ��or��
####  fill/ stroke/stroke-opacity/fill-opacity/stroke-width  ��

....  #�ȵ�


```

</br><b>3.3 Output files</b>
<pre>
out.svg: Output plot in SVG format
out.png: Output plot in png format
</pre>


###  4 Example
------------

</br>See more detailed usage in the&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <b>[Chinese Documentation](https://github.com/hewm2008/NGenomeSyn/blob/main/����չʾ������鹲���Գ���NGenomeSyn_manual_chinese.pdf)</b>
</br>See more detailed usage in the&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <b>[English Documentation](https://github.com/hewm2008/NGenomeSyn/blob/main/����չʾ������鹲���Գ���NGenomeSyn_manual_chinese.pdf)</b>
</br>See the example directory and  Manual.pdf for more detail.
</br>��������  Manual.pdf for more detail �����ʵ�������ã����ڽ���ĳЩ��ַ�ͷ�һЩ�̳�
</br></br> 
../../bin/NGenomeSyn       -InConfi        in.cofi -OutPut OUT
</br>  Ŀ¼  Example/example*/�����������������ͽű��÷���


* Example 1)����������Ĭ��
����ף�Ĭ�Ͼ��С�
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example1/OUT.png)

* Example 2) ����(N��)������Ĭ�� 
����  �� ��text ��� ������������ϡ�   ���и�����ı�ɫ�������С�˵�.
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example2/OUT1.png)


* Example 3)����(N��)������Ĭ��  ���� ��ת��
��ת ������������
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example2/OUT2.png)


* Example 4)  ��������
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example3/OUT.png)
�����ݿ��Գ���ͼ
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example3/test.jpg)




###  5 Advantages

</br>�ٶȿ죬���ڴ�
</br>�������Ҷ�����϶���
</br>��perl���������У��ⰲװ


###  6 An example image generated by NGenomeSyn.

------------



###  7 Discussing
------------
- [:email:](https://github.com/hewm2008/NGenomeSyn) hewm2008@gmail.com / hewm2008@qq.com
- join the<b><i> QQ Group : 125293663</b></i>

######################swimming in the sky and flying in the sea #############################

