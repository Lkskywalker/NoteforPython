### 输入和输出

##### 输出

```python
#--------输入------------
#百分号输出
name = 'xiaoming'
age = 15
print('姓名:%s,年龄:%d'%(name,age))

# .format(name)输出
name = 'xiaogang'
age = 18
print('姓名:{},年龄:{}'
.format(name,age))
```

##### 输入

```python
#input()输入
name = input('Input your name:')
age = input('Input your age:')
print('姓名:{},年龄:{}'.format(name,age))
```

**input()输入的数据默认是str,字符型**

**强制类型转换**

```python
age = int(input('Input your age:)
```
