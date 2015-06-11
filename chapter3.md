# Datetime 模块

获取当前时间

```python
>>> import datetime
>>> print datetime.datetime.now()
2015-06-11 17:13:45.427000
```

也可以手动赋值，生成时间

```python
>>> import datetime
>>> print datetime.datetime(2015, 3, 6, 12, 1, 15)
2015-03-06 12:01:15
```

像time模块一样，同样可以使用`strftime()`来将时间转换为字符串

```python
>>> import datetime
print datetime.datetime(2015, 3, 6, 12, 1, 15).strftime('%Y%m%d')
20150306
```

time与datetime之间的互相转换

```python
>>> datetime.datetime.fromtimestamp(time.time())
datetime.datetime(2015, 6, 11, 17, 28, 38, 7000)
```

