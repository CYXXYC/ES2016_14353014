#Lab5 ROS的安装与Cartographer的体验

##1.ROS配置步骤：
![image](https://cloud.githubusercontent.com/assets/22671956/20245684/60a3b53c-a9e1-11e6-8ab3-e8b0d6e26fd1.png)
![image](https://cloud.githubusercontent.com/assets/22671956/20245687/73f4abbe-a9e1-11e6-85c6-8d45d2eba626.png)
![image](https://cloud.githubusercontent.com/assets/22671956/20245745/7bae915c-a9e2-11e6-9385-d352b4f6cf73.png)
![image](https://cloud.githubusercontent.com/assets/22671956/20245747/7f83ffce-a9e2-11e6-9f9a-8f78cb2c946a.png)

##2.ROS配置截图：
本次实验虽然说按照流程配置即可，但配置你懂的，总会有许多预料之外的困难与阻碍，下面是本次遇到的一些问题，由于配置的年代比较久远了，也就没有截什么图，但有最后一步的截图，因为一直没有配置成功：
![image](https://cloud.githubusercontent.com/assets/22671956/20245785/2dff20c4-a9e3-11e6-9e2a-cd36480e3ec7.png)
尝试了一些方法：
<br>1.![image](https://cloud.githubusercontent.com/assets/22671956/20245797/709825de-a9e3-11e6-8618-4e495927990d.png)
<br>2.换添加到source.list中的镜像，也就是配置的【1.2】
![image](https://cloud.githubusercontent.com/assets/22671956/20245808/bf7facd0-a9e3-11e6-9cb4-ff4e0d729f8e.png)
但尝试了好久还是没有效果，我猜应该是ubuntu的源无法连接到 packages.ros.org的软件包源。最后Ta说可以忽略，决定放弃，好在不是很影响后面的catorgrapher的体验。

##3.Cartographer的配置
![image](https://cloud.githubusercontent.com/assets/22671956/20245885/e2089800-a9e5-11e6-8669-7c96db16ce4d.png)
![image](https://cloud.githubusercontent.com/assets/22671956/20245886/ee7ab9c4-a9e5-11e6-9979-8d6c826622f6.png)
![image](https://cloud.githubusercontent.com/assets/22671956/20245890/f4184982-a9e5-11e6-8a59-ca8da804c0ff.png)
![image](https://cloud.githubusercontent.com/assets/22671956/20245896/02edf2a4-a9e6-11e6-9ab4-cb6b999343bf.png)
讲道理的话按配置走就可以，然后果真在最后一步运行launch文件的时候遇到了问题。。用它推荐的第二种方法没解决，结果用了第一种就可以了。

##4.Cartographer配置截图：
Cartographer是今天配置的，所以截图还是有几张的：
![image](https://cloud.githubusercontent.com/assets/22671956/20245920/b8def50e-a9e6-11e6-89b3-186da24ec826.png)
<br><br>![image](https://cloud.githubusercontent.com/assets/22671956/20245922/bf425f8a-a9e6-11e6-93f0-a237d68a8c2d.png)
<br><br>![image](https://cloud.githubusercontent.com/assets/22671956/20245924/ca6288e0-a9e6-11e6-9a69-9ca4bc8a6565.png)
<br><br>![image](https://cloud.githubusercontent.com/assets/22671956/20245932/e922d532-a9e6-11e6-9a18-c23d275d6bad.png)
<br><br>![image](https://cloud.githubusercontent.com/assets/22671956/20245925/d6de0964-a9e6-11e6-851b-22c3367706f2.png)
<br><br>然后是下载文件，将它添加到ubuntu中运行。
<br>Cartographer2d效果图：
<br>（1）打开时的初始界面：![image](https://cloud.githubusercontent.com/assets/22671956/20245958/74bc037a-a9e7-11e6-9b92-3212dddc17d6.png)
<br><br>（2）貌似是雷达地图：![image](https://cloud.githubusercontent.com/assets/22671956/20245984/06ce43ea-a9e8-11e6-835c-79d44e680482.png)
<br><br>（3）退出时的虚拟机终端：<br>![image](https://cloud.githubusercontent.com/assets/22671956/20245981/f36a02c6-a9e7-11e6-8bde-c72bde758de4.png)

##5.实验感想
讲道理，配置的报告真不知道写些啥，配置的时候忘了截图，重新配一遍的话（呵呵。。），这也是我所能想到的配置报告的形式了，and终于在双十一到来前紧赶忙赶赶到了lab5。