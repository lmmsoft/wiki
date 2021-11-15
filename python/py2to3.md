在多个项目中做过 python2 to python3 的迁移，最推荐的工具是 python-modernize

## python-modernize
- Links:
  - https://github.com/mitsuhiko/python-modernize
  - https://python-modernize.readthedocs.io/en/latest/
  - https://pypi.org/project/modernize/
- Usage:
  - 安装
    - pip install modernize
  - 使用
    - python-modernize -w example.py
    - 参数解释， -w, --write Write back modified files


## 特殊写法（python-modernize无法自动转换）
- reload(sys)
```
if six.PY2:
    reload(sys)
    sys.setdefaultencoding('utf-8')
```

-  ModuleNotFoundError: No module named 'commands'
  -  https://docs.python.org/3.3/library/subprocess.html#legacy-shell-invocation-functions
```
import six
if six.PY2:
    import commands as subprocess
elif six.PY3:
    import subprocess

# in code
commands.getstatusoutput change to subprocess.getstatusoutput
```

- TypeError: '<' not supported between instances of 'dict' and 'dict'
  - python3 不再支持dict的排序，原因和解法可以看这个: 
  - https://stackoverflow.com/questions/22333388/dicts-are-not-orderable-in-python-3
```
>>> dicts = [{'a':'a'},{'b':'b'}]
>>> sorted(dicts, key=lambda x:sorted(x.keys()))
[{'a': 'a'}, {'b': 'b'}]
```

