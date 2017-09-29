# Problem 1.6: Population growth problem

## 摘要
  这是一个比较简单的人口增长问题，对题目所述的人口增长模型用Python建立程序模型，使用欧拉方法求出数值解，并与解析解进行比较分析得到一定结论。
  
## 背景介绍
在这里采用的模型为：人口增长速率为与人口总数量成正比的出生人口减去与人口总数量二次成正比的死亡人口。
  其函数模型为：
    ![](http://latex.codecogs.com/gif.latex?\frac{dN}{dt}=aN-bN{^{2}})
    其中N为人口总数，aN对应人口增长，![](http://latex.codecogs.com/gif.latex?bN{^{2}})对应人口死亡。当人口数量多到一定程度时，由于食物的缺乏导致人口存在上限，所以人口死亡数量与![](http://latex.codecogs.com/gif.latex?bN{^{2}})成正比，当b=0时，则人口将呈指数增长。
    当a和b取不同的竖直时，将得到很多有趣的结果，并且结果很大程度上依赖于N的初始值大小。
  
## 正文
#### 分析
首先，我们对其做进一步分析，人口增长模型对应的常微分方程可写成：
```math
N(t+dt)=N(t)+[aN(t)-bN^2(t)]dt
```
如果我们取![](http://latex.codecogs.com/gif.latex?dt)为一个足够小的值，并且已知N的初值N(t0)后经过多次迭代，便可得到之后所有的数值近似解。
然后，就参数而言，我们需要设置（a、b、N(t0)、dt、end_t）

- 对于a、b、N(t0)容易看出参数a为人口增长系数，建议的值在0.01-100之间；参数b为人口消减系数，建议的值在0-10之间。参数a、b和人口初值N(t0)均可通过用户输入方式得到，且数值类型为浮点数，因为人口初值可以科学计数法方式设定。
- 对于end_t，通过考察方程可发现，当N=a/b时，dN=0，即人口数N将无限趋于a/b，为了显示适当比例的人口增长曲线图，end_t需要根据输入的a、b、N(t0)来决定。又当处于b=0的极端情况时，人口数将指数增长，这将可能超出matplotlib能接受的最大数值，故需要对此情况做特殊处理。
- 对于dt，由于end_t的范围变动很大，故设置一个固定的计算次数而让dt的值由计算次数决定。
#### 程序实现
对于该问题，在借鉴了学长的成果后，我使用了matplotlib库作为作图工具。

[代码在此](https://github.com/ms-tu/compuational_physics_N2015301020147/blob/master/problem1-6%EF%BC%9Apopulation%20growth.py)
#### 结果分析
- 当a=0.1,b=0.001,N(t_0)=2时，人口增长曲线如图，可以推出，当N=a/b时，人口增长趋于稳定
![image](https://github.com/ms-tu/compuational_physics_N2015301020147/blob/ms-tu-patch-1/population_model_1.png)
- 当a=10,b=3,N(t0)=1000时，人口迅速下降后趋于一稳定值
![image](https://github.com/ms-tu/compuational_physics_N2015301020147/blob/ms-tu-patch-1/population_model_2.png)

## 结论
从上面的分析可知：当a=0.1,b=0.001,N(t_0)=2时，最终人口稳定于100，当a=10,b=3,N(t0)=1000时，人口迅速下降后趋于一稳定值。

由此可推知：
- a/b比较大时，出生率起主要作用，因此人口增长较快， 但会趋近于一个定值a/b.
- 当不是很大时，N(t)会下降得很快，这是由于死亡率起较大作用，但不会趋近于0，最终仍会趋于一个定值。
- 当b=0时（未作图验证），但易知人口将呈指数一直增长。
## 致谢
感谢—— 臧之昊    刘文焘 前辈们的工作
