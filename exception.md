# Exception handling #

## Use Case 应用场景 ##

lower level control for `Exception` handling

## Quick Example ##

```python
d = {}
RERAISE = False
try:
    d['a']
except Exception as e:
    import sys, traceback
    exc_type, exc_value, exc_traceback = sys.exc_info()
    print isinstance(e, KeyError) #True
    print e == exc_value #True
    traceback.print_exc(file=sys.stdout)
    if RERAISE:
        custom_message = " this is custom_message"
        raise exc_type, exc_type(str(e)+custom_message), exc_traceback
finally:
    print "Finally statement"
print "After try...except"
```

## Reference ##

for more detailed reference, see 

[https://docs.python.org/2/library/exceptions.html](https://docs.python.org/2/library/exceptions.html)

[https://docs.python.org/2/library/traceback.html](https://docs.python.org/2/library/traceback.html)
