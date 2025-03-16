---
title: Panda、Numpy、Matplotlib演示
date: 2025-03-09
category:
  - 机器学习
tags:
  - 库
sticky: 
thumbnail: 
excerpt: 示例演示
cover: 
mathjax: "true"
---

### 1.matplotlib

```python
import matplotlib
matplotlib.use('TkAgg')       #使用 `TkAgg`后端
from matplotlib import pyplot as plt
x=[1,2,3,4,5]
y=[2,3,4,5,6]
fig1 = plt.figure(figsize = (5,5))
plt.plot(x,y)       #散点 plt.scatter(x, y)
plt.title('y vs x')
plt.xlabel('x')
plt.ylabel('y')
plt.show()

```

### 2.numpy

```python
import numpy as np
a = np.eye(5)       #对角线数组
print(type(a))
print(a)
b = np.ones((5,5))      #全是1的数组
print(type(b))
print(b)
print(b.shape)      #b数组的维度
c = a+b
print(type(c))
print(c.shape)
print(c)

```

### 3.panda
```python
import pandas as pd
data = pd.read_csv('detectedData01.csv')
x = data.loc[:,'编号']        #数据索引
y = data.loc[:,'姓名']
c = data.loc[data['性别'] == 1, '姓名']       #筛选列表中性别==1的下姓名`
#---------------------------------------------------------------------------------------


data_array = np.array(data)       #调用numpy中arry()方法转换数组

data_new = data + 10       #所有数据＋10
data_new.head()       #展示部分数据
data_new.to_csv('data_new.csv')       #新文件保存
```
```