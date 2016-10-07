#Lab 2
***
###Description
The distributed operation layer (DOL) is a software development framework to program parallel applications. The DOL allows to specify applications based on the Kahn process network model of computation and features a simulation engine based on SystemC. Moreover, the DOL provides an XML-based specification format to describe the implementation of a parallel application on a multi-processor systems, including binding and mapping.

Reference:
<br>www.tik.ee.ethz.ch/~shapes/dol.html
###How to install
1. 安装VMware，下载乌邦图镜像并创建一个虚拟机。
<br>Vmware教程：`http://jingyan.baidu.com/article/0320e2c1ef9f6c1b87507bf6.html`</br>
<br>ubuntu下载：`http://www.ubuntu.com/download/desktop`</br>
<br><br>
2. 配置必要的环境：
<br>`$	sudo apt-get update`</br>
<br>`$	sudo apt-get install ant`</br>
<br>`$ 	sudo apt-get install openjdk-7-jdk`</br>
<br>`$	sudo apt-get install unzip`</br>
<br><br>
3. 将dol文件和system文件添加到ubuntu中，并解压文件：
  <br>![systemc](https://github.com/CYXXYC/for-graph/blob/master/systemfile.png) 
  </br>
  <br>![dol](https://github.com/CYXXYC/for-graph/blob/master/dolfile.png)
  </br>
  <br> 新建dol的文件夹：
  <br>`$	mkdir dol`
  <br>将dolethz.zip解压到 dol文件夹中
  <br>`$	unzip dol_ethz.zip -d dol`
  <br>解压systemc
  <br>`$	tar -zxvf systemc-2.3.1.tgz`
  <br><br>
4. 编译systemc：
  <br>解压后进入systemc-2.3.1的目录下
  <br>`$	cd systemc-2.3.1`
  <br>新建一个临时文件夹objdir
  <br>`$	mkdir objdir`
  <br>进入该文件夹objdir
  <br>`$	cd objdir`
  <br>运行configure(能根据系统的环境设置一下参数，用于编译)
  <br>`$	../configure CXX=g++ --disable-async-updates`
  <br>
  <br>运行configure结果如下图：
  <br>![configure](https://github.com/CYXXYC/for-graph/blob/master/configure.png)
  <br><br>
  <br>继续编译
  <br>`$	sudo make install`
  <br>记录当前的工作路径
  <br>`$	pwd`


5. 编译dol：
  <br>进入dol的文件夹:
  <br>`$	cd ../dol`
  <br>修改build_zip.xml文件,找到下面这段话:
  <br>`<property name="systemc.inc" value="YYY/include"/>`
  <br>`<property name="systemc.lib" value="YYY/lib-linux/libsystemc.a"/>`
  <br>把YYY改成上页pwd的结果;
  <br>然后编译:
  <br>`$	ant -f build_zip.xml all`

6. 最后的运行结果：
  <br>进入build/bin/mian路径下
  <br>`$	cd build/bin/main`
  <br>运行第一个例子
  <br>`$	ant -f runexample.xml -Dnumber=1`
  <br>运行成功结果如图：
  <br>![success](https://github.com/CYXXYC/for-graph/blob/master/success.png)
  

###Experimental experience
1. 选对镜像很重要，不然换源会很麻烦，如果换了几次源都不行，建议用配置好的同学的镜像；
2. 学会了ubuntu的几个语句，如解压unzip，创建文件夹mkdir；
3. markdown真是非常好用方便的编辑软件。