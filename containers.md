# Containers: Set, List, Dict and Collections family #

## Set ##

`.remove()` removes element and returns `None`, raises `KeyError` if not exsit

`.discard()` is similar to `.remove()` but does not raise `KeyError` if not exsit


```python
a = set(1,2,3)
for x in a:
    print x
    a.discard(x)
```

This will raise `RuntimeError: Set changed size during iteration`

`set` can be initiated by `list`

`set` is unsorted.

for `Python 2.7`

```python
a = {1,2,3}
print type(a) # <type 'set'>
a = {1}
print type(a) # <type 'set'>
a = {}
print type(a) # <type 'dict'>
```
