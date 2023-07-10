# MicroPython MIP test 4

One in a series of example repos to test various mpremote mip installation patterns.

#### Install

```
$ mpremote mip install github:mcauser/micropython-mip-test4

Install github:mcauser/micropython-mip-test4
Installing github:mcauser/micropython-mip-test4/package.json to /lib
Installing: /lib/test4/__init__.py
Installing: /lib/test4/test4.py
Installing: /lib/test4/bitbang.py
Done
```

GitHub               | Device
:--------------------|:--------------------------
/lib/\_\_init\_\_.py | /lib/test4/\_\_init\_\_.py
/lib/test4.py        | /lib/test4/test4.py
/lib/bitbang.py      | /lib/test4/bitbang.py

```
$ mpremote repl

>>> import test4
>>> b = test4.Bitbang()
test4 bitbang __init__
>>> b.main()
test4 bitbang main

>>> t = test4.Test4()
test4 __init__
>>> t.main()
test4 bitbang main

>>> from test4 import Test4
>>> t = Test4()
test4 __init__
>>> t.main()
test4 bitbang main
```

#### Install examples

```
$ mpremote mip install github:mcauser/micropython-mip-test4/examples
```

GitHub                     | Device
:--------------------------|:------------------------------
/examples/test4_basic.py   | /lib/test4/examples/basic.py
/examples/test4_complex.py | /lib/test4/examples/complex.py

```python
$ mpremote repl

>>> import test4.examples.basic
test4 __init__
test4 basic
>>> import test4.examples.complex
test4 __init__
test4 bitbang complex
```
