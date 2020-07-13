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

When defining a new function, stop to think about which arguments should always be specified as keyword arguments when calling your function. Consider using the * operator to require those arguments be specified as keyword arguments.

And remember that you can accept arbitrary keyword arguments to the functions you define and pass arbitrary keyword arguments to the functions you call by using the ** operator.

* Python 3's f-Strings: [f-String (fast)](https://realpython.com/python-f-strings/)
```
>>> def to_lowercase(input):
...     return input.lower()

>>> name = "Eric Idle"
>>> f"{to_lowercase(name)} is funny."
'eric idle is funny.'
```

* function annotations: [doc](https://www.geeksforgeeks.org/function-annotations-python/)

Can be used in documentation or documentation.

* [Name mangling](https://www.geeksforgeeks.org/name-mangling-in-python/) in Python

In name mangling process any identifier with two leading underscore and one trailing underscore is textually replaced with _classname__identifier where classname is the name of the current class.
```
class Student: 
    def __init__(self, name): 
        self.__name = name 
  
s1 = Student("Santhosh") 
print(s1._Student__name)
```

The dir() method is used by passing the class object and it will return all valid attributes that belong to that object. print(dir(s1)) output: 
```
[‘_Student__name’, ‘__class__’, ‘__delattr__’, ‘__dict__’, ‘__dir__’, ‘__doc__’, ‘__eq__’, ‘__format__’, ‘__ge__’, ‘__getattribute__’, ‘__gt__’, ‘__hash__’, ‘__init__’, ‘__le__’, ‘__lt__’, ‘__module__’, ‘__ne__’, ‘__new__’, ‘__reduce__’, ‘__reduce_ex__’, ‘__repr__’, ‘__setattr__’, ‘__sizeof__’, ‘__str__’, ‘__subclasshook__’, ‘__weakref__’] 
```

* Python [property function](https://www.geeksforgeeks.org/python-property-function/)

