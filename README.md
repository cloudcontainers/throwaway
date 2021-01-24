# throwaway

[![Build Status](https://travis-ci.org/cloudcontainers/throwaway.svg?branch=main)](https://travis-ci.org/cloudcontainers/throwaway)
[![license]](https://img.shields.io/github/license/cloudcontainers/throwaway)


Get cycle going

## setup python dependencies

Install pytest:

```bash
pip2 install -U pytest
```

Check that we have it:

```bash
$ pytest --version
pytest 6.2.1
```

## create first test

New file sample:

```python
# content of test_sample.py

def myfunc(x):
    return x + 1

def test_answer():
    assert myfunc(5) == 60
```

### travis output

After putting in travis config and requirements files.

```text
$ pytest
============================= test session starts ==============================
platform linux -- Python 3.6.7, pytest-5.4.3, py-1.7.0, pluggy-0.12.0
rootdir: /home/travis/build/cloudcontainers/throwaway
collected 1 item
test_sample.py F                                                         [100%]
```

## Fix it

Correct the error.

```python
# content of test_sample.py

def myfunc(x):
    return x + 1

def test_answer():
    assert myfunc(5) == 60
```
