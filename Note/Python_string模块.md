# Python    string模块

- string模块主要包含关于字符串的处理函数

- 大小写、判断函数、以及字符串常规操作（填充、搜索、修改、剪切、添加、分割）

### 大小写

```python
# 大小写
# upper() and lower(), 全部转换为大小写
text = 'Hello World'
print(text.upper())  # HELLO WORLD
print(text.lower())  # hello world
# -------------------------------------------------
# title(), 将给定的字符串中所有单词的首字母大写，其他全部小写
# capitalize(), 将给定的字符串中首字母大写，其他小写
text = 'hello world'
print(text.title())  # Hello World
print(text.capitalize())  # Hello world
# -------------------------------------------------
# 大小写反转 swapcase()
text = 'Hello World'
print(text.swapcase())  # hELLO wORLD
```

### 判断字符串

```python
# 判断字符串
# isdecimal():判断给定字符串是否全为数字
text = '1234'
print(text.isdecimal())  # True
text = '123a'
print(text.isdecimal())  # False
# isalpha():判断给定的字符串是否全为字母
text = 'abcd'
print(text.isalpha())  # True
text = '123a'
print(text.isdecimal())  # False
# isalnum()：判断给定的字符串是否只含有数字与字母
text = 'abcd123'
print(text.isalnum())  # True
text = '123'
print(text.isalnum())  # True
text = 'abcd'
print(text.isalnum())  # True
text = '123asc@'
print(text.isalnum())  # False
# isupper():判断给定的字符串是否全为大写
text = 'ABCD'
print(text.isupper())  # True
text = 'abC'
print(text.isupper())  # False
text = 'ab222'
print(text.isupper())  # False
text = '222'
print(text.isupper())  # False
# islower():判断给定的字符串是否全为小写
text = 'abcd'
print(text.islower())  # True
# istitle():判断给定的字符串是否符合title()
text = 'Hello World'
print(text.istitle())  # True
text = 'Hello world'
print(text.istitle())  # False
# isspace():判断给定的字符串是否为空白符（空格、换行、制表符）
text = ' '
print(text.isspace())  # True
text = 'Hello world'
print(text.isspace())  # False
# isprintable():判断给定的字符串是否为可打印字符（只有空格可以，换行、制表符都不可以）
text = 'he llo'
print(text.isprintable())  # True
text = ' hello\t'
print(text.isprintable())  # False
# isidentifier():判断给定的字符串是否符合命名规则（只能是字母或下划线开头、不能包含除数字、字母和下划线以外的任意字符。）
text = 'ha_123'
print(text.isidentifier())  # True
text = '_123'
print(text.isidentifier())  # True
text = '123abc'
print(text.isidentifier())  # False
```

### 字符串填充

```python
# 字符串填充
# 居中为center(width),这时候原来的字符串将会在中间，扩充物出现在两边。
text = 'abc'
print(text.center(10, '-'))  # ---abc----
# 居左为ljust(width)，l为lef的缩写，源字符串在左边，填充物出现在字符串的右边。
text = 'abc'
print(text.ljust(8, '+'))  # abc+++++
# 居右为rjust(width),  r为right的缩写，源字符串在右边，填充物出现在字符串的左边。
text = 'abc'
print(text.rjust(8, 's'))  # sssssabc
```

### 字符串查找

```python
# 字符串查找操作
"""
count(sub[, start[, end]])
主要对指定字符串搜索是否具有给定的子字符串sub,若具有则返回出现次数。
"""
text = 'abcdabchabjjj'
print(text.count('ab'))  # 3
print(text.count('ab', 2, 10))  # 2
print(text.count('dddd'))  # 0

'''
startswith(prefix[, start[, end]])  |   endswith(suffix[, start[, end]])
判断函数的开始，或者末尾的字符串是否为指定字符串
返回结果为True与False
'''
text = 'abcdefg'
print(text.startswith('ab'))  # True
print(text.startswith('cd', 2, 6))  # True
print(text.endswith('efg'))  # True

'''
find(sub[, start[, end]]) 返回第一个子字符串的位置信息，若无则为-1
rfind(sub[, start[, end]])返回最右边的第一个子字符串的位置信息，若无则为-1
index(sub[, start[, end]]) 返回第一个子字符串的位置信息，若无则为报错
rindex(sub[, start[, end]])返回最右边的第一个子字符串的位置信息，若无则报错
'''
text = 'jflkadjflkasjflsa'
print(text.index('lk'))  # 2
print(text.index('jjj'))  # ValueError: substring not found
print(text.rindex("ls"))  # 14
print(text.find('ad'))  # 4
print(text.find('kk'))  # -1
```

### 字符串替换

```python
# 字符串替换
"""replace(old, new[, count])：将搜索到的字符串改为新字符串
count是可选择输入的参数，代表更改个数。"""
text = 'abckkkfskkmmkk'
print(text.replace('kk', 'gg'))  # abcggkfsggmmgg
print(text.replace('kk', 'gg', 1))  # abcggkfskkmmkk
```

### 字符串分割

```python
# 字符串分割
"""
partition()和rpartition()
partition(sep)对给定字符串进行切割，切割成三部分
返回元组
"""
text = 'java,python,c++,go'
print(text.partition(','))  # ('java', ',', 'python,c++,go')
print(text.partition('c++'))  # ('java,python,', 'c++', ',go')
"""
split()和rsplit()方法分别用来以指定字符为分隔符，
将字符串左端和右端开始将其分割成多个字符串，并返回包含分割结果的列表
如果不指定分隔符，则字符串中的任何空白符号（包括空格、换行符、制表符等等）都将被认为是分隔符
"""
text = 'java,python,c++,go'
print(text.split(','))  # ['java', 'python', 'c++', 'go']
```

### 字符串的连接

```python
# 字符串连接
"""
"连接字符".join(可迭代对象)
将可迭代数据用字符串连接起来(字符串string、列表list、元组tuple、字典dict、集合set)
每个参与迭代的元素必须是字符串类型，不能包含数字或其他类型
"""
text = "abcd"
list1 = ['java', 'python', 'c++']
print("+".join(text))  # a+b+c+d
print(" ".join(list1))  # java python c++
print(''.join("efg"))
# 几个字符串放在一起自动合成一个
print("abc""defg""hijk")  # abcdefghijk
# +号连接
print("abc" + "efg")  # abcefg
# ,号连接成元组
tuple1 = 'abc', 'efg'
print(tuple1)  # ('abc', 'efg')
print(''.join(tuple1))  # abcefg
# 还有其他方法
```

### String模块中的常量

```
string.digits：数字0~9
string.ascii_letters：所有字母（大小写）
string.lowercase：所有小写字母
string.printable：可打印字符的字符串
string.punctuation：所有标点
string.uppercase：所有大写字母
```

**举一个随机生成Email的例子**

```python
def getEmail():
    suffix = ['.com', '.org', '.net', '.cn']  # 后缀名
    characters = string.ascii_letters + string.digits + '_'  # 字母,数字,下划线组成的字符集
    username = ''.join(random.choice(characters) for i in range(random.randint(6, 12)))  # 生成式
    domain = ''.join(random.choice(characters) for i in range(random.randint(3, 6)))
    return username + '@' + domain + random.choice(suffix)


email = getEmail()
print(email)  # yUFK1qQ@BMxhaq.cn
```
