# 字符编码

```python
>>> s = "中文"
>>> type(s)
<type 'str'>
>>> u = u"中文"
>>> type(u)
<type 'unicode'>
```

如上可知，我们定义的变量s是字符串类型的，在前面加上一个u限定，那么变量u就是unicode类型的

Unicode 编码成 UTF-8, GB2312

```python
>>> u = u"中文"
>>> type(u)
<type 'unicode'>
>>> utf8 = u.encode("utf-8")
>>> type(utf8)
<type 'str'>
>>> print utf8
中文
>>> utf8
'\xe4\xb8\xad\xe6\x96\x87'
>>> 
>>> gb2312 = u.encode("gb2312")
>>> gb2312
'\xd6\xd0\xce\xc4'
```

我们之前的s, 打印出来看看它的编码

```python
>>> s = "中文"
>>> type(s)
<type 'str'>
>>> s
'\xe4\xb8\xad\xe6\x96\x87'

```

跟上面对比可知，Python的默认的字符编码就是UTF-8的

---


# 未完，待更新。。。

