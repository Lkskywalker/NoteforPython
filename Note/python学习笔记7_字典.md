## 字典

- 字典以键值对{key:value}组成的集合,可以存储任何对象.

- 通常以键来访问数据,支持增删改

- 字典没有下标的概念,是无序的键值集合

- 键是唯一的

### 字典的操作

#### 字典的定义,添加

```py
# 字典的定义,添加
dictA = {'name':'Tom','age':'21','shcool':'CUIT'}# 直接在定义的时候添加
dictA['pro'] = 'Internet'#定义后添加
print(dictA)
```

```py
{'name': 'Tom', 'age': '21', 'shcool': 'CUIT', 'pro': 'Internet'}
```

#### 字典的获取,查找

```py
#获取
# 获取所有的键
print(dictA.keys())
# 获取所有的值
print(dictA.values())
# 获取所有的键值对
print(dictA.items())
# 用for循环遍历
for key,value in dictA.items():
    print('%s=%s'%(key,value),end=" ")
    pass
```

```py
dict_keys(['name', 'age', 'shcool', 'pro'])
dict_values(['Tom', '21', 'CUIT', 'Internet'])
dict_items([('name', 'Tom'), ('age', '21'), ('shcool', 'CUIT'), ('pro', 'Internet')])
name=Tom age=21 shcool=CUIT pro=Internet
```

#### 字典的更新(修改)

```py
print(dictA)
dictA.update({'age':'100'})#用update通过键值对修改
dictA['name'] = 'Make'  #通过键查找后修改
print(dictA)
```

```py
{'name': 'Tom', 'age': '21', 'shcool': 'CUIT', 'pro': 'Internet'}
{'name': 'Make', 'age': '100', 'shcool': 'CUIT', 'pro': 'Internet'}
```

#### 字典的删除

```py
# 删除
print(dictA)
del dictA['name']
dictA.pop('age')
print(dictA)
```

```py
{'name': 'Tom', 'age': '21', 'shcool': 'CUIT', 'pro': 'Internet'}
{'shcool': 'CUIT', 'pro': 'Internet'}
```

![](https://s1.ax1x.com/2022/10/05/x1COTe.jpg)

## 集合

没有value的字典, 集合属于可变的序列,存储的数据的顺序与添加的顺序不一定相同(Hash), 集合中的元素不重复

#### 集合的操作

```py
#创建
setA = set(range(1,10))
print(setA)
setB = {1,2,3,4,5,99}
print(setB)
#添加
setB.add(6)
setB.update({11,23,34})
print(setB)
#删除
setB.remove(99)
print(setB)
#setB.remove(888)    #KeyError: 888
#remove删除指定元素不存在时,会报异常
setB.discard(888)
#discard功能同remove一样,但不会抛异常
setB.pop()  #任意删除一个元素
#清空
setB.clear()
print(setB)
```

```
{1, 2, 3, 4, 5, 6, 7, 8, 9}
{1, 2, 3, 4, 5, 99}
{1, 2, 3, 4, 5, 99, 6, 34, 11, 23}
{1, 2, 3, 4, 5, 6, 34, 11, 23}
set()
```

#### 集合的关系判断

```py
#集合的关系判断
set1 = {1,2,3,4}
set2 = {1,2,3,4}
set3 = {1,2,3,4,5}
#判定是否相等
print(set1==set2)#True
print(set1==set3)#False
#判断是否 没有 交集,没有是True
print(set1.isdisjoint(set3))#False 有交集
set4 = {8,9,10}
print(set1.isdisjoint(set3))#True 没有交集
#判断是否是子集
print(set1.issubset(set3))#True
#判断是否是超集
print(set3.issuperset(set1))#True
```

```py
#真子集的判断
print(set3>set1)#True
print(set2>set1)#False
```

#### 集合的运算

```py
set1 = {1,2,3,4}
set2 = {5, 6, 7, 8}
set3 = {3,4,5,6}
#并集
print(set1|set2)    #{1, 2, 3, 4, 5, 6, 7, 8}
#交集
print(set2&set3)    #{5, 6}
#差集(set2-set3 = set2-(set2 & set3))
print(set2-set3)    #{8, 7}
```
