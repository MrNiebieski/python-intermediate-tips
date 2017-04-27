# ConfigParser Library #

## Use Case 应用场景 ##

Hard Code 密码之类的是应该避免的一种行为, ConfigParser可以简单的把一些常数参数分到另外的文件里面.

如果在代码库里面, 可以配合`.gitignore`忽略敏感信息, 并创立一个`example.cfg`文件来解释config file schema

这是一个标准库, 无需额外安装

## Quick Start ##

```python
import ConfigParser
config = ConfigParser.ConfigParser()
config.read('example.cfg')
user = config.get("mysql", "user")
```

`example.cfg` content:

```
[mysql]
user = mysqluser
```

## Reference ##

for more detailed reference, see [https://docs.python.org/2/library/configparser.html](https://docs.python.org/2/library/configparser.html)
