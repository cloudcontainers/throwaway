# Project throwaway

[![Build Status](https://travis-ci.org/cloudcontainers/throwaway.svg?branch=main)](https://travis-ci.org/cloudcontainers/throwaway)
[![License](https://img.shields.io/github/license/cloudcontainers/throwaway.svg)](https://opensource.org/licenses/MIT)

A simple first project to check dependencies.

## Use python as base platform

We need pytest to get a first test going.

```bash
pip2 install -U pytest
```

Check that we have the latest version.

```bash
$ pytest --version
pytest 6.2.1
```

## A first failing test

Very boring stuff, of course.

```python
# content of test_sample.py

def myfunc(x):
    return x + 1

def test_answer():
    assert myfunc(5) == 60
```

### Output failing on Travis

After putting in travis config and requirements files.

```text
$ pytest
============================= test session starts ==============================
platform linux -- Python 3.6.7, pytest-5.4.3, py-1.7.0, pluggy-0.12.0
rootdir: /home/travis/build/cloudcontainers/throwaway
collected 1 item
test_sample.py F                                                         [100%]
```

## A first successful test

Correct the error.

```python
# content of test_sample.py

def myfunc(x):
    return x + 1

def test_answer():
    assert myfunc(5) == 6
```

### Output ok on Travis

```text
$ pytest
============================= test session starts ==============================
platform linux -- Python 3.6.7, pytest-5.4.3, py-1.7.0, pluggy-0.12.0
rootdir: /home/travis/build/cloudcontainers/throwaway
collected 1 item
test_sample.py .                                                         [100%]
============================== 1 passed in 0.01s ===============================
The command "pytest" exited with 0.
```
