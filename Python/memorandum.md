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
