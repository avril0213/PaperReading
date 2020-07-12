* Keyword parameters [named parameters](https://treyhunner.com/2018/04/keyword-arguments-in-python/)

Python allows functions to capture any keyword arguments provided to them using the ** operator when defining the function:
```
def format_attributes(**attributes):
    """Return a string of comma-separated key-value pairs."""
    return ", ".join(
        f"{param}: {value}"
        for param, value in attributes.items()
    )
```
That ** operator will allow our format_attributes function to accept any number of keyword arguments. The given arguments will be stored in a dictionary called attributes.

* Python 3's f-Strings: [f-String (fast)](https://realpython.com/python-f-strings/)
```
>>> def to_lowercase(input):
...     return input.lower()

>>> name = "Eric Idle"
>>> f"{to_lowercase(name)} is funny."
'eric idle is funny.'
```
