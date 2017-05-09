
### Short Conclusion ###

`xrange` is faster than `range`, `reverse` almost as fast as `-1`

I found `reversed` used in combination with `xrange` in one of the Python standard library, it should be fine.

[https://hg.python.org/cpython/file/2.7/Lib/heapq.py](https://hg.python.org/cpython/file/2.7/Lib/heapq.py)


```python
import timeit
MAX = 500000
cnt = 0
t = timeit.default_timer()
for i in reversed(range(MAX)):
  cnt+=i
print 'reversed  range: ', timeit.default_timer() - t,cnt

cnt = 0
t = timeit.default_timer()
for i in reversed(xrange(MAX)):
  cnt+=i
print 'reversed xrange: ', timeit.default_timer() - t, cnt

cnt = 0
t = timeit.default_timer()
for i in range(MAX-1,-1,-1):
  cnt+=i
print ' step -1  range: ', timeit.default_timer() - t, cnt

cnt=0
t = timeit.default_timer()
for i in xrange(MAX-1,-1,-1):
  cnt+=i
print ' step -1 xrange: ', timeit.default_timer() - t, cnt
```
