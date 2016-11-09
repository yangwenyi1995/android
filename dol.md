#DOL修改
##Example1：使其输出三次方数
原本的是输出二次方数，所以我们只需要找到实现模块，并加以修改即可。实现在square.c中，所以找到其中的实现部分，将i= i*i修改即可。

i = i * i * i;

![](http://oes14yokp.bkt.clouddn.com/dol_1.jpg)

##Example2：让三个square模块变为两个

模块的连接是在xml中实现的，我们找到对应的xml文件。原来的iterator是3，即square模块被使用了三次，我们只需要改为2即可。

![](http://oes14yokp.bkt.clouddn.com/dol_2.jpg)