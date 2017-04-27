# hashlib Library #

## Use Case 应用场景 ##

我需要做一个简单的Load Balencer, 把一些任务分给不同的worker来做, 需要reproducible, deterministic, 每次运行都要同样的分配, 所以不能用随机分配.

下面是一个简单的实现


```python
import hashlib
s = u"string to be hashed"
MODE_RANGE = 10
t = int(hashlib.sha1(s).hexdigest(),16) % MODE_RANGE
print type(t), t
```

**解释**

先用`hashlib`的hash算法, 然后把hex换成10进制, 然后取模得到一个`<type 'long'>`的结果

`sha1`可以换成`md5`或其他


## Reference ##

for more detailed reference, see [https://docs.python.org/2/library/configparser.html](https://docs.python.org/2/library/configparser.html)
