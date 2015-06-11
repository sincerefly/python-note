#Time 模块

time模块表示时间有两种形式，分别为`时间戳`和`数组（struct_time）`。

```python
>>> import time
>>> print time.time()
1434010963.16
>>> print time.localtime()
time.struct_time(tm_year=2015, tm_mon=6, tm_mday=11, tm_hour=16, tm_min=23, tm_sec=5, tm_wday=3, tm_yday=162, tm_isdst=0)
```

两种表示法可以通过`gmtime()`和`mktime()`相互转换。

```python
>>> import time
>>> print time.gmtime(time.time())
time.struct_time(tm_year=2015, tm_mon=6, tm_mday=11, tm_hour=8, tm_min=35, tm_sec=39, tm_wday=3, tm_yday=162, tm_isdst=0)
>>> print time.mktime(time.localtime())
1434011755.0
>>> 
```

使用strptime可以将字符串转换为数组时间格式。

```python
>>> import time
>>> time.strptime('20150306', '%Y%m%d')
time.struct_time(tm_year=2015, tm_mon=3, tm_mday=6, tm_hour=0, tm_min=0, tm_sec=0, tm_wday=4, tm_yday=65, tm_isdst=-1)
```

使用strftime可以将数组时间格式转换为字符串。

```python
>>> import time
>>> print time.strftime('%Y-%m-%d', time.localtime())
2015-06-11
>>> print time.strftime('%Y-%m-%d %H:%M:%S', time.localtime())
2015-06-11 16:47:32
```







