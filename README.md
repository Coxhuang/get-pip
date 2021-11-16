# get-pip

pip 升级失败

## #1 现象

```python
Traceback (most recent call last):
  File "/usr/bin/pip3", line 11, in <module>
    sys.exit(main())
  File "/home/trunk/.local/lib/python3.5/site-packages/pip/__init__.py", line 11, in main
    from pip._internal.utils.entrypoints import _wrapper
  File "/home/trunk/.local/lib/python3.5/site-packages/pip/_internal/utils/entrypoints.py", line 4, in <module>
    from pip._internal.cli.main import main
  File "/home/trunk/.local/lib/python3.5/site-packages/pip/_internal/cli/main.py", line 57
    sys.stderr.write(f"ERROR: {exc}")
                                   ^
SyntaxError: invalid syntax
```

## #2 解决

> 找到对应的`Python`版本,我这里是`Ubuntu`自带的`Python3.5`

```python
https://bootstrap.pypa.io/
```

```python
curl https://bootstrap.pypa.io/pip/3.5/get-pip.py -o get-pip.py
python3 get-pip.py
```
