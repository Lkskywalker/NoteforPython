#### 拼接,合并(+ 操作)

```py
# 合并_字符串
str1 = '人生苦短'
str2 = '我用python'
print(str1+str2)
```

```
人生苦短我用python
```

-----

```py
# 合并_列表
list1 = [1,'love',1.2]
list2 = [8,9,'k2']
print(list1+list2)
```

```
[1, 'love', 1.2, 8, 9, 'k2']
```

----

```py
# 合并_元组
tuple1 = (1,2,'abc')
tuple2 = (3,4,'def')
print(tuple1+tuple2)
```

```
(1, 2, 'abc', 3, 4, 'def')
```

#### 复制(* 操作)

```py
# 复制
str1 = '人生苦短'
print(str1*3)
list1 = [1,'love',1.2]
print(list1*3)
```

```
人生苦短人生苦短人生苦短
[1, 'love', 1.2, 1, 'love', 1.2, 1, 'love', 1.2]
```

#### 判断是否存在(in 操作)

```py
#存在判断
#序列(字符串,列表,元组)
str1 = '人生苦短'
print('生' in str1)
list1 = [1,'love',1.2]
print(888 in list1)
#字典(判断键key)
dict1 = {'name':'Tom','age':'21','shcool':'CUIT'}
print('name' in dict1)
```

```
True
False
True
```
