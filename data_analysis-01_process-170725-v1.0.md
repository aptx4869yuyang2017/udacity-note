Title:  data_analysis-01_process-170725-v1.0
Author: yuyang  
Date:   July 25, 2017  

> 数据分析入门<https://classroom.udacity.com/courses/ud170>

## problems solved
How Bill James applied data analysis to baseball
<https://en.wikipedia.org/wiki/Bill_James>

## process

1. question
2. wrangle
3. explore
4. draw conclusions
5. communication

## read csv
```python
import unicodecsv

def read_csv(filename):
    with open(filename, 'rb') as f:
        reader = unicodecsv.DictReader(f)
        return list(reader)
   
```

## fixing type of data 修复数据类型

* 时间
```python
from datetime import datetime as dt

# Takes a date as a string, and returns a Python datetime object. 
# If there is no date given, returns None
def parse_date(date):
    if date == '':
        return None
    else:
        return dt.strptime(date, '%Y-%m-%d')
```
* 整形字符串
```python
# Takes a string which is either an empty string or represents an integer,
# and returns an int or None.
def parse_maybe_int(i):
    if i == '':
        return None
    else:
        return int(i)
```
* 布尔型
 ```python
 enrollment['keyname'] = enrollment['keyname'] == 'True'
```

## investigating the data
* 根据某个特征值 找到不重复的数据
```python
bs_num = len(bs)

unique_bs = set()   #集合对象的特点
for b in bs:
    unique_bs.add(b['account_key'])
len(unique_bs)
```

