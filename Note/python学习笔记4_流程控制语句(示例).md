### 流程控制语句(示例)

#### if else流程

```python
num = int(input("输入成绩:"))
if num>=60 and num<90:
    print('及格')
    pass
elif num>=90 and num<100:
    print("优秀")
    pass
else:
    print('不及格')
    pass
```

注意条件后打冒号

Python pass 是空语句，是为了保持程序结构的完整性。

**pass** 不做任何事情，一般用做占位语句。

##### 石头剪刀布

```python
import random
person = int(input('请出拳:[0:石头,1:剪刀,2:布]'))
pc = random.randint(0,2)
if pc==0 and person==1:
    print('pc win')
    pass
elif pc==0 and person==2:
    print('player win')
    pass
elif pc==1 and person==2:
    print('pc win')
    pass
elif pc==1 and person==0:
    print('player win')
    pass
elif pc==2 and person==0:
    print('pc win')
    pass
else:
    print('player win')
    pass
```

##### 嵌套

```python
num = int(input("输入成绩:"))
if num>=60:
    if num > 60 and num <80:
        print('yiban')
        pass
    else:
        print('优秀')
        pass
    pass

else:
    print('不及格')
    pass
```

用缩进代表C语言的大括号

##### 
