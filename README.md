###DOL Application Programming Interface: 
The DOL defines a set of computation and communication routines that enable the programming of distributed, parallel applications for the SHAPES platform. Using these routines, application programmers can write programs without having detailed knowledge about the underlying architecture. In fact, these routines are subject to further refinement in the hardware dependent software (HdS) layer.
###DOL Functional Simulation: 
To provide programmers a possibility to test their applications, a functional simulation framework has been developed. Besides functional verification of applications, this framework is used to obtain performance parameters at the application level.
###DOL Mapping Optimization: 
The goal of the DOL mapping optimization is to compute a set of optimal mappings of an application onto the SHAPES architecture platform. In a first step, XML based specification formats have been defined that allow to describe the application and the architecture at an abstract level. Still, all the information necessary to obtain accurate performance estimates is contained.

##step:
1.安装一些必要的环境

$	sudo apt-get update  
$	sudo apt-get install ant  
$ 	sudo apt-get install openjdk-7-jdk  
$	sudo apt-get install unzip

2.从主机中下载所需文件拷贝到虚拟机内

3.解压文件


4.编译systemc
![](http://oes14yokp.bkt.clouddn.com/%E5%9B%BE%E7%89%870.jpg)
解压后进入systemc-2.3.1的目录下  
$	cd systemc-2.3.1  
新建一个临时文件夹objdir  
$	mkdir objdir  
进入该文件夹objdir  
$	cd objdir  
运行configure(能根据系统的环境设置一下参数，用于编译)  
$	../configure CXX=g++ --disable-async-updates  
编译
$	sudo make install
编译完后文件目录如下  
$ cd ..        $ ls
![](http://oes14yokp.bkt.clouddn.com/%E5%9B%BE%E7%89%872.jpg)

记录当前的工作路径
$	pwd

![](http://oes14yokp.bkt.clouddn.com/%E5%9B%BE%E7%89%873.jpg)

5.编译dol  

$	ant -f build_zip.xml all  

![](http://oes14yokp.bkt.clouddn.com/%E5%9B%BE%E7%89%874.jpg)

进入build/bin/mian路径下  
$	cd build/bin/main  
然后运行第一个例子  
$ sudo	ant -f runexample.xml -Dnumber=1

![](http://oes14yokp.bkt.clouddn.com/%E5%9B%BE%E7%89%875.jpg)



