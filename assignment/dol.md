#Lab3
##1.实验结果截图
1. 将example2中的三个平方模块修改为两个
<br />重新编译运行后的.dot图：
<br /> ![](https://github.com/CYXXYC/for-graph/blob/master/dot.png)

2. example1运行结果：
<br />![](https://github.com/CYXXYC/for-graph/blob/master/example1.png)

3. example2运行结果:
<br />![](https://github.com/CYXXYC/for-graph/blob/master/example2.png)

##2.实验关键步骤以及主要代码
1. example1：
修改squre.c中的squre_fire函数，将输入端读进来的数原来的平方运算修改为立方运算，再读入到输出端即可，然后重新编译运行，修改代码如下：
<br />![](https://github.com/CYXXYC/for-graph/blob/master/example1代码.png)

2. example2：将example.xml文件中N的值修改为2，即让它的迭代次数变为2，修改代码如下：
<br />![](https://github.com/CYXXYC/for-graph/blob/master/example2代码.png)

##3. 实验感想：
1. 修改完代码后要将原来的文件夹删掉，重新编译再运行，才会跑出修改后的效果。大概是因为原来的文件夹是没修改前编译出来的，所以即使在example文件夹中修改了也不会跑出修改后的结果，相当于压缩包里的东西改变了，但我跑的是之前解压的文件运行的也是之前的效果。
2. 熟悉了.dot框架图，初步了解如何从代码中知道哪个框对应什么进程，如何连线，以及与端口之间的联系。
3. 上次实验是配置dol环境，虽然配置成功了但却不知道example1和example2在终端的输出是什么意思；通过这次实验，通过看example中的文件，初步了解为何终端为何会输出那些数据。