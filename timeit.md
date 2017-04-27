# timeit Library #

## Use Case 应用场景 ##

标准库, 可以用来简单的计时

## Quick Start ##

```python
import timeit
import time
time_start = timeit.default_timer()
time.sleep(1)
time_diff = timeit.default_timer() - time_start
print 'time used: %ds=%.1fmin'%(time_diff, time_diff/60.0)
```

## Reference ##
for more detailed reference, see [https://docs.python.org/2/library/timeit.html](https://docs.python.org/2/library/timeit.html#module-timeit)
