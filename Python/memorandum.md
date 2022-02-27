# Python Memorandum

## NumPy

如果我们有一个类似 enum 类型的 list, 比如说:

```python
countries = np.array(['CN', 'US', 'FR'])
```

我们可以使用如下方式根据上面的 enum 快速生成一个具有任意数量的新 list

```python
countries_new = countries[np.random.randint(0, 3, 10)]

# output:
# array(['FR', 'FR', 'CN', 'US', 'CN', 'FR', 'US', 'US', 'CN', 'US'],
#       dtype='<U2')
```

## How to manipulate dates

```python
import datetime as dt
from dateutil import tz
```

### From local date time string

```python
date_str = '2022-02-25'
# construct local datetime object
dt_ = dt.datetime.fromisoformat(date_str)
# convert to UTC
dt_utc = dt_.astimezone(dt.timezone.utc)
# format to ISO string for store to db
dt_iso_str = dt_utc.isoformat()

# construct datetime from UTC ISO string (from db)
dt_local = dt.datetime.fromisoformat(dt_iso_str)
# convert to local
dt_local = dt_local.astimezone(tz.tzlocal())

print(f'UTC ISO String: {dt_iso_str}')
print(f'Local: {dt_local.isoformat()}')

# output:
# UTC ISO String: 2022-02-24T16:00:00+00:00
# Local: 2022-02-25T00:00:00+08:00
```

### From UTC current date time

```python
# create UTC current datetime object
# current local date time: 2022-02-27 09:24:55
now_utc = dt.datetime.utcnow()
# because by default datetime objects have no time zone
# so need to set the time zone to UTC
now_utc = now_utc.replace(tzinfo=dt.timezone.utc)
# format to ISO string for store to db
now_utc_iso_str = now_utc.isoformat()

# construct datetime from UTC ISO string (from db)
dt_local = dt.datetime.fromisoformat(now_utc_iso_str)
# convert to local
dt_local = dt_local.astimezone(tz.tzlocal())

print(f'UTC ISO String: {now_utc_iso_str}')
print(f'Local: {dt_local.isoformat()}')

# output:
# UTC ISO String: 2022-02-27T01:24:55.042309+00:00
# Local: 2022-02-27T09:24:55.042309+08:00
```
