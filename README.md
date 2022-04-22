
# NGenomeSyn
Multi-level visualization of genomic statistical variables on rectangular chromosomes

###  1 Introduction
<b>NGenomeSyn</b> ÊÇÓÚ»ùÓÚ¶à¸ö»ùÒò×é¹²ÏßĞÔ¹ØÏµµÄ¿ÉÊÓ¹¤¾ß£¬¶Ô¶à¸ö»ùÒò×é×ÔÖ÷ÅÅÁĞÎ»ÖÃ£¬À©³¤ÊÕËõ£¬Ğı×ª½Ç¶È µÈ£¬½áºÏÑÕÉ«£¬´ïµ½¿ìËÙÒ»ÑÛ¿´³ö¹æÂÉ£¬Ê¶±ğ½á¹û¡£ ²¢ÇÒ¸÷ÖÖ¿ÉÒÔ×Ô¼º×éºÏ ×ÔÓÉĞŞ¸ÄÏà¹Ø²ÎÊı¡£
</br>
</br>ÁÁµã£º
</br>1  ÈÎÒâ¶à¸ö»ùÒò×é£¨Ä¿Ç°ÎÒÏŞ12¸ö£¬¿ÉÒÔÈ¡Ïû£©
</br>2  ¸÷¸ö»ùÒò×é¿ÉÒÔ×Ô¼ºµ÷Ë³Ğò ÑÕÉ«µÈµÈÊôĞÔ
</br>3  ¸÷¸ö»ùÒò×é¿ÉÒÔÒÆ¶¯ Ğı×ª À©³¤ºÍÊÕËõµÈ
</br>
</br>ÆäÖĞ3  ¿ÉÒÔµ÷ºÃÏà¹Ø²ÎÊı ¿ÉÒÔ³öÏÖ Èı½ÇĞÎ  Îå½ÇĞÎ  ËÄ±ßĞÎ µÈµÈ×éºÏ£¨ºóÃæ½«ÓĞ¿ÕÉı×éµ÷¶¨ÕâĞ©²ÎÊı£©

</br>³ÌĞòÊÇ¸øÒ»Ğ©ÓĞ»ù´¡µÄÉúĞÅÅóÓÑÓÃµÄ£¬ÈôÊÇĞ¡°×¿´²»¶®¾ÍËãÁË¡£
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
	   # ÓÃ·¨ºÍcircosÏàËÆ£¬Ö÷ÒªÒ»¸öÅäÖÃÎÄ¼şÒ»Ñù,¾ßÌå¼ûpdf£¬¼òÒª¹¦ÄÜ½éÉÜÈçÏÂ
	1  ÈÎÒâ¶à¸ö»ùÒò×é£¨Ä¿Ç°ÎÒÏŞ12¸ö£¬¿ÉÒÔÈ¡Ïû£©
	2  ¸÷¸ö»ùÒò×é¿ÉÒÔ×Ô¼ºµ÷Ë³Ğò ÑÕÉ«µÈµÈÊôĞÔ
	3  ¸÷¸ö»ùÒò×é¿ÉÒÔÒÆ¶¯ Ğı×ª À©³¤ºÍÊÕËõµÈ
	
	ÆäÖĞ3  ¿ÉÒÔµ÷ºÃÏà¹Ø²ÎÊı ¿ÉÒÔ³öÏÖ Èı½ÇĞÎ  Îå½ÇĞÎ  ËÄ±ßĞÎ µÈµÈ×éºÏ£¨ºóÃæ½«ÓĞ¿ÕÉı×éµ÷¶¨ÕâĞ©²ÎÊı£©
	   
</pre>

</br><b>3.1.2 Other parameters</b>
```php
     ÊäÈëÎÄ¼ş»ùÒò×é¸ñÊ½¼û  pdf.Ö÷ÒªÎªchr start end µÈÆäËüÊôĞÔ µÄ¸ñÊ½
     ÊäÈëlink¼ş»ùÒò×é¸ñÊ½¼û  pdf.Ö÷ÒªÎªchrA  startA enda chrB startB endB   µÈµÈÆäËüÊôĞÔ µÄ¸ñÊ½

```

</br><b>3.2.2 Detail parameters</b>
```php
	#  ¾ßÌå¼ûpdf
##################################### È«¾Ö²ÎÊı #######################################################
SetParaFor = global
GenomeInfoFile1=RefA.info
###### Format (chr Start End ...ÆäËüÊôĞÔ)  chrË³ĞòºÍÕâÎÄ¼şÒ»ÖÂ ÈôÊÇEnd Start ÔòÕâÌõchr·´Ïò»¥²¹
##  ÆäËüÊôĞÔ Èçfill=red stroke-width=0  stroke=black stroke-opacity=1 fill-opacity=1 µÈµÈ¿ÉÒÔ²»Í¬ĞĞ²»Í¬ÊôĞÔ
GenomeInfoFile2=RefB.info  ##  GenomeInfoFile X  ¾Í±íÊ¾ÓĞ X¸ö»ùÒò×é

LinkFileRef1VsRef2=Link
####### Format (chrA StartA EndA chrB StartB End ...ÆäËüÊôĞÔ)
#  ¿ÉÒÔ¶à´ÎRef1VsRef2   LinkFileRef2VsRef1 µÈ


##Main = "main_Figure"  ##  the Fig Name  :MainRatioFontSize MainCor ShiftMainX  ShiftMainY 
## font-size 

################################ Figure ############################################################

##############################     »­²¼ ºÍ Í¼Æ¬ ²ÎÊıÅäÖÃ #################################
#body=1200   ##   Ä¬ÈÏÊÇ1200£¬Ö÷»­²¼´óĞ¡ÉèÖÃ  ÁíÍâ£ºup/down/left/right) = (55,25,100,120); #CanvasHeightRitao=1.0 CanvasWidthRitao=1.0
##RotatePng   = 0  ##  ¶ÔFigure½øĞĞĞı×ªµÄ½Ç¶È

SetParaFor = Genome1  #  ALL/GenomeX  XµÚX¸ö»ùÒò×é

#ZoomChr=1.0          ## chr³¤¶È µÈ´ó ËõĞ¡ or À©´ó
#RotateChr=30         ## chrµÄÆğµã Ë³Ê±Õë Ğı×ª  xx ¶È
#ShiftX=0
#ShiftY=0             ##¶ÔÕâ¸ö»ùÒò×éÒÆ¶¯,Ò²¿ÉÒÔÖ±½ÓÓÃMoveToX MoveToY 

#ChrWidth=20          ## Õâ¸ö»ùÒò×échrµÄÔÚ»­²¼µÄ¿í¶È
#LinkWidth=180        ## Õâ¸ö»ùÒò×éºÍÏÂÒ»¸ölinkµÄ¸ß¶È
#ChrSpacing=10        ## Õâ¸ö»ùÒò×échrÖ®¼äµÄ¿ÕÏ¶
#NormalizedScale=0    ## ÓÃ×Ô¼ºµÄ±ê³ß  Ïàµ±¸Ã»ùÒò×éÓëÄ¬ÈÏµÄ»ùÒò×éÊÇ·ñµÈ³¤

#SpeRegionFile=        ## ÎÄ¼ş,±í¼ÇÌØ±ğÇøÓò[¸ñÊ½chr start End £¨xx=yy¼ÓÊôĞÔµÈ]

##ÆäËüµ±ºÜÉÙÓÃµ½µÄ²ÎÊı EndCurveRadian=3/ µÈµÈ
## GenomeNameRatio GenomeName

SetParaFor = Genome2  #  ALL/GenomeX  XµÚX¸ö»ùÒò×é
SetParaFor=Link1  #  ¿¿X¿ Link X  File ¿¿¿¿
#StyleUpDown=           ## UpDown  DownUp  UpUP DownDown  ¿¿¿¿
#Reverse=1              ## ¿¿link
#HightRation=1.0        ## links¿¿¿¿  ¿¿or¿¿
####  fill/ stroke/stroke-opacity/fill-opacity/stroke-width  ¿¿

....  #µÈµÈ


```

</br><b>3.3 Output files</b>
<pre>
out.svg: Output plot in SVG format
out.png: Output plot in png format
</pre>


###  4 Example
------------

</br>See more detailed usage in the&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <b>[Chinese Documentation](https://github.com/hewm2008/NGenomeSyn/blob/main/ÈÎÒâÕ¹Ê¾¶à»ùÒò×é¹²ÏßĞÔ³ÌĞòNGenomeSyn_manual_chinese.pdf)</b>
</br>See more detailed usage in the&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <b>[English Documentation](https://github.com/hewm2008/NGenomeSyn/blob/main/ÈÎÒâÕ¹Ê¾¶à»ùÒò×é¹²ÏßĞÔ³ÌĞòNGenomeSyn_manual_chinese.pdf)</b>
</br>See the example directory and  Manual.pdf for more detail.
</br>¾ßÌå¼ûÕâ¶ù  Manual.pdf for more detail ÀïÃæµÄÊµÀıºÍÅäÖÃ£¬ºóÆÚ½«ÔÚÄ³Ğ©ÍøÖ·ÊÍ·ÅÒ»Ğ©½Ì³Ì
</br></br> 
../../bin/NGenomeSyn       -InConfi        in.cofi -OutPut OUT
</br>  Ä¿Â¼  Example/example*/¡¡ÀïÃæÓĞÊäÈëºÍÊä³öºÍ½Å±¾ÓÃ·¨¡£


* Example 1)Á½¸ö»ùÒò×éÄ¬ÈÏ
×î¼òÒ×£¬Ä¬ÈÏ¾ÓÖĞ¡£
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example1/OUT.png)

* Example 2) Èı¸ö(N¸ö)»ùÒò×éÄ¬ÈÏ 
Á½²ã  ¼´ »­text ²ãºÍ ¸ßÁÁ²ãÁ½ÖÖÅäºÏ¡£   ÆäÖĞ¸ßÁÁ²ãµÄ±³É«Ìõ¿í¶ÈËõĞ¡ÁËµã.
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example2/OUT1.png)


* Example 3)Èı¸ö(N¸ö)»ùÒò×éÄ¬ÈÏ  ÅÅÁĞ Ğı×ªµÈ
Ğı×ª µÚÈı¸ö»ùÒò×é
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example2/OUT2.png)


* Example 4)  ÈÎÎñÅÅÁĞ
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example3/OUT.png)
ÓĞÊı¾İ¿ÉÒÔ³öÏÂÍ¼
![out.png](https://github.com/hewm2008/NGenomeSyn/blob/main/Example/example3/test.jpg)




###  5 Advantages

</br>ËÙ¶È¿ì£¬ÉÙÄÚ´æ
</br>¿ÉÒÔ×ÔÎÒ¶¨Òå×éºÏ¶à²ã´Î
</br>ÓĞperl¼´¿ÉÒÔÔËĞĞ£¬Ãâ°²×°


###  6 An example image generated by NGenomeSyn.

------------



###  7 Discussing
------------
- [:email:](https://github.com/hewm2008/NGenomeSyn) hewm2008@gmail.com / hewm2008@qq.com
- join the<b><i> QQ Group : 125293663</b></i>

######################swimming in the sky and flying in the sea #############################

