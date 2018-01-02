# 期中作业——Pygame实践之“Tom and Jerry”

## 摘要：
   Pygame 是一组用来开发游戏软件的 Python 程序模块，基于 SDL 库的基础上开发。本作业就是要用pygame做一个游戏，鉴于水平有限，
   就以一个简单的猫抓老鼠游戏开始吧。
   
## 思路：
   模仿一个简单的炮弹射击游戏，做了一个简单的反相接“炮弹”的游戏。就叫“Tom and Jerry”吧：）
   
   游戏有五轮，游戏者有10血，抓一只老鼠加10分，每100积分进入下一轮，丢老鼠或者碰到一个炸弹都少一血，血量为零时游戏结束。
第一、第二轮只有老鼠，第三轮开始有炸弹，并且鼠的下降速度随轮次增加变快，即游戏难度越来越大。
每局血量剩下不多时猫会改变图片做出提示。没命了就会回到初始界面。

[代码如下](https://github.com/ms-tu/compuational_physics_N2015301020147/blob/master/Tom%20and%20Jerry.py)

## 效果：

![image](https://github.com/ms-tu/compuational_physics_N2015301020147/blob/master/TIM图片20180102162102.png)
![image](https://github.com/ms-tu/compuational_physics_N2015301020147/blob/master/TIM图片20180102162124.png)
![image](https://github.com/ms-tu/compuational_physics_N2015301020147/blob/master/TIM图片20180102162130.png)
![image](https://github.com/ms-tu/compuational_physics_N2015301020147/blob/master/TIM图片20180102162136.png)

## 结论：
   一个简单的打炮弹模拟实验，初步了解了pygame的一些用法。学会了一丢丢使用pygame自己做game的知识~
   
   
## 致谢：
 [Python基础之（三）----PyGame安装步骤](http://blog.csdn.net/qq_33166080/article/details/68928563)  
 [python的相关应用——pygame的一个小例子](http://blog.csdn.net/asware/article/details/4151554)  
 [pygame实例](http://blog.csdn.net/liushaochan123/article/details/8604214)  
 乔敏琛同学的工作
