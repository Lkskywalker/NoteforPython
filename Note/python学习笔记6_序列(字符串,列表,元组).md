## 序列(字符串,列表,元组)

**支持索引和切片操作**

###### 索引(下标):第一个索引为0;第一个索引为负数时,指向右端

#### 字符串

###### 切片

切片:截取字符串中的一段内容,**基本语法[起始下标:结束下标:步长]**

```py
# 切片
print('--------切片----------')
s = 'I love you'
print(s[2:6])#取2~5个字符

print(s[2:])#取2到最后

print(s[:6])#0~5

print(s[::-1])#倒叙输出
```

```py
--------切片----------
love
love you
I love
uoy evol I
```

###### 字符串函数

![](https://s1.ax1x.com/2022/10/04/xlPm8I.jpg)

#### 列表

##### 列表的常用函数

![](https://s1.ax1x.com/2022/10/04/xlE9BV.jpg)

###### 增加

```py
# append    在列表末尾增加元素
list2 = list(range(0,10))
print('list2:',list2)
list2.append(8888)
print('list2:',list2)
list2.append([1,2,3,4])
print('list2:',list2)
```

```py
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 8888]
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 8888, [1, 2, 3, 4]]
```

----

```py
# insert    在列表中指定位置插入元素
list2 = list(range(0,10))
print('list2:',list2)
list2.insert(2,888)
print('list2:',list2)
list2.insert(2,[1,2,3])
print('list2:',list2)
```

```py
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
list2: [0, 1, 888, 2, 3, 4, 5, 6, 7, 8, 9]
list2: [0, 1, [1, 2, 3], 888, 2, 3, 4, 5, 6, 7, 8, 9]
```

-----

```py
# extend    扩展,批量添加
list2 = list(range(0,10))
print('list2:',list2)
list2.extend([10,11,12,13])
print('list2:',list2)
```

```py
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13]
```

###### 删除

```py
# del    删除指定元素,批量删除(利用切片)
list2 = list(range(0,20))
print('list2:',list2)
del list2[0]
print('list2:',list2)
del list2[0:5]
print('list2:',list2)
```

```py
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
list2: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
list2: [6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
```

-----

```py
# remove    移除指定的元素
list2.remove(18)
print('list2:',list2))
```

```py
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 19]
```

------

```python
# pop   移除指定下标的元素
list2.pop(0)
print('list2:',list2)
```

```py
list2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
list2: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
```

###### 查找

```py
list1 = ['abc',123,1.1,'hello',True]
print(list1)
print(list1.index('hello'))
print(list1.index)
```

```
['abc', 123, 1.1, 'hello', True]
3
```

##### 列表的切片

```py
# 列表
list1 = ['abc',123,1.1,'hello',True]
print(list1)
# 索引
print(list1[1])
# 切片
print(list1[1:3])
print(list1[2:])
print(list1[:3])
print(list1[::-1])
```

#### 元组

元组是一种不可变的序列,创建后不能做任何修改

当元组中只有一个元素时要加逗号,不然当作其他类型处理

###### 元组的查询

元组因为不可变,所以只能进行查询操作

```py
tupleA = ('abc',3,1.22,6,9,[1,2,3,4])
print(tupleA)
#元组的查询
#下标查询
print(tupleA[1])
#切片
print(tupleA[1:3])
print(tupleA[::-1])
print(tupleA[::-2]) # 反转每隔两个取一次
print(tupleA[::2])# 每隔两个取一次
print(tupleA[-3:-1:]) # 倒着取-1 ~ -3的元素,不包含-1,步长为1
```

```py
('abc', 3, 1.22, 6, 9, [1, 2, 3, 4])
3
(3, 1.22)
([1, 2, 3, 4], 9, 6, 1.22, 3, 'abc')
([1, 2, 3, 4], 6, 3)
('abc', 1.22, 9)
(6, 9)
```

###### 元组中列表的修改

```py
#元组中的列表可以修改
print(type(tupleA[5])) # 查看元组中列表的类型
tupleA[5][0] = 888
print(tupleA) #可以修改元组中列表中的值
```

```py
<class 'list'>
('abc', 3, 1.22, 6, 9, [888, 2, 3, 4])
```

###### 打逗号

```py
#元组中只有一个元素时,需要打逗号,不然会识别为其他类型
tupleB = (1)
print(type(tupleB))
tupleB = ('abc')
print(type(tupleB))
tupleB = (1,)
print(type(tupleB))eB))
```

```py
<class 'int'>
<class 'str'>
<class 'tuple'>
```

#### 列表生成式 (列表表达式)

![](https://s1.ax1x.com/2022/10/07/x3NaZV.png)

上图 i*i 指是要输出值的表达式, 后面是对输出值的条件限定和取值范围,下面看几个例子

**简单来说:从要生成的序列中取值, 后面的for用来控制取值的次数**

```py
#列表生成式
#生成1~10的列表
list1 = [i for i in range(1,10)]
print(list1)
#生成A1,A2,A3,...,C1,...的列表
list1 = [i+j for i in 'ABC' for j in '123']
print(list1)
#实现嵌套列表的平铺
vec = [[1,2,3], [4,5,6], [7,8,9]]
list1 = [num for elem in vec for num in elem]
print(list1)
#过滤不符合条件的元素
aList = [-1,-4,6,7.5,-2.3,9,-11]
#过滤掉负数
aList = [i for i in aList if i>=0]
print(aList)
```

```py
[1, 2, 3, 4, 5, 6, 7, 8, 9]
['A1', 'A2', 'A3', 'B1', 'B2', 'B3', 'C1', 'C2', 'C3']
[1, 2, 3, 4, 5, 6, 7, 8, 9]
[6, 7.5, 9]
```

```python
s = ['java', 'python', 'c++', 's', 'kk', 'dfhsdj']
list1 = [random.choice(s) for i in range(3)]
print(list1)#['java', 's', 'dfhsdj']
```



#### 生成器推导式

生成器推导式（generator expression）的用法与列表推导式非常相似，在形式上生成器推导式使用<mark>圆括号</mark>（parentheses）作为定界符

---

- 生成器推导式的结果是一个<mark>生成器对象</mark>,类似于迭代器对象。具有<mark>惰性求值</mark>的特点，只在需要时生成新元素，比列表推导式具有更高的效率，空间占用非常少，尤其适合大数据处理的场合。

- 使用生成器对象的元素时，可以根据需要将其转化为列表或元组，也可以使用生成器对象的______next_______() (前后两根下划线)方法或者内置函数next()进行遍历，或者直接使用for循环来遍历其中的元素。

- 只能从前往后正向访问每个元素，没有任何方法可以再次访问已访问过的元素，也不支持使用下标访问其中的元素。如果需要重新访问其中的元素，必须重新创建该生成器对象

```py
#生成器推导式
g = (i**2 for i in range(1,10))
print(type(g))#<class 'generator'>
#遍历
print(g.__next__())#1
print(g.__next__())#4
print(next(g))#9
for i in g:
    print(i,end=" ")#16 25 36 49 64 81
    pass
print()
tupleA = tuple(g)
print(tupleA)#()
#不能重新访问,输出空
g1 = (i**2 for i in range(1,5))
tupleA = tuple(g1)
print(tupleA)#(1, 4, 9, 16)
```
