# throwaway

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
