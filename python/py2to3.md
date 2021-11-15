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
```
if six.PY2:
    import commands as subprocess
elif six.PY3:
    import subprocess
```

