#### while循环(未知循环次数)

```python
#----------while循环---------------
count=1
while count<=10:
    print('{}'.format(count))
    count+=1
    pass

# 打印九九乘法表
row=9
while row>=1:
    col=1
    while col<=row:
        print('%d+%d=%d'%(row,col,row*col),end=" ")
        col+=1
        pass
    print()
    row -= 1
    pass
```

#### for循环(已知循环次数)

```python
#------------for循环--------------------
# for 临时变量 in 容器
#     执行代码块

tags = 'Hello'
for item in tags:
    print(item)
    pass

#range函数  range(起始:结束:步长)   生成一个数据集合列表(左闭右开)
#输出1~9
for i in range(1,10):
    print('{} '.format(i),end="")
```

#### break 和 continue

break:推出当前的循环体

continue:推出本次循环

```python
#break 和 continue
for i in range(1,10):
    #输出1~5
    if i>5:
        break
    print('{} '.format(i),end="")
    pass

print()#换行

for i in range(1,10):
    #输出奇数
    if i%2==0:
        continue
    print('{} '.format(i),end="")
    pass
```

#### 嵌套

```py
#用for打印九九乘法表
for i in range(1,10):
    for j in range(1,i+1):
        print("{}*{}={} ".format(i,j,i*j),end="")
        pass
    print()
```
