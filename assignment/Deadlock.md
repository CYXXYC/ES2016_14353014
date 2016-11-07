#Lab4 Deadlock

##1.实验截图
实验中通过设置bat文件中的参数c，来设定运行不同次数的死锁程序。
</br>c = 500:
</br>![](https://github.com/CYXXYC/for-graph/blob/master/lab4_c%3D500.png)
![](https://github.com/CYXXYC/for-graph/blob/master/lab4_500time.png)

</br>c = 1000：
</br>![](https://github.com/CYXXYC/for-graph/blob/master/lab4_c%3D1000.png)
![](https://github.com/CYXXYC/for-graph/blob/master/lab4_1000times.png)
</br>

##2.产生死锁的四个必要条件
死锁的产生主要是因为系统资源不足，进程的执行顺序不当，资源分配不均等原因造成的，如果系统资源充足，进程的执行的顺序使得每个进程的资源都能得到满足等，那么产生死锁的可能性就很小。虽然我们的资源总是不充足的，但我们的操作系统或者进程之间并不总是产生死锁，因为死锁产生有四个必要条件：
</br>
1. 一个资源每次只能被一个进程占有。</br>
2. 当进程请求资源被阻塞时，对已有的资源不释放。</br>
3. 每个进程对获得的资源，未使用完前不对资源进行释放。</br>
4. 若干进程之间形成首尾循环等待资源的关系。</br>

##3.实验中的死锁
main函数中新建执行一个Deadlock（）函数，由于Deadlock类是继承自Runanable的，调度执行它时也会运行run（）中的语句。
</br>我们来看看两个函数中的语句：Deadlock（）函数中先实例化了A和B两个类，当线程t开始，此时run（）中的语句执行，它是b中一个被synchronized修饰的函数methodA（），传入一个A的对象，执行last（）函数；另一方面Dealock（）函数等到c变为0后，a也执行类似的方法methodB（）；a和b都需要对方作为自己的参数来执行函数，但自己在运行完自己的函数之前不会释放自己的资源，因此均被阻塞，同时由于函数是被synchronized修饰的，无法重开一个线程来执行这一函数，所以双方都在同一个线程内请求对方资源而又不释放自己的资源，产生死锁。

##4.实验感想
1. 重新温习了死锁产生的必要条件。
2. 初步了解了bat文件在cmd中的执行以及相关语句，例如`：start`是开始标签，`echo`是显示在cmd上，`%var%`是取变量var的值，`if %var% leq 1000`是当var到达1000时等。
3. 嵌入式实验PPT真有趣，嗯。