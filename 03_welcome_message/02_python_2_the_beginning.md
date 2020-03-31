When you fork and clone `catch_me_if_you_can` project you will see the following:

```python
def main():
   #write your code here

if __name__ == '__main__':
     main()
```

### What is `if __name__ == '__main__'` ??

Every [module](https://www.w3schools.com/python/python_modules.asp) in Python has a special attribute called  `__name__`. The value of  `__name__` attribute is set to  `'__main__'` when module run as main program. Otherwise, the value of  `__name__` is set to contain the name of the module.

Consider the following code for better understanding.

```python
# file my_module.py

number = 4

def hello():
    print("Hello, World!")

if __name__ == "__main__":
    print("Executing as main program")
    print("Value of __name__ is: ", __name__)
    hello()
```


Here we have defined a new module  `my_module`. We can execute this module as main program by entering the following code:

    >>> python my_module.py

**Expected Output:**

    >>> Executing as main program
    >>> Value of __name__ is: __main__
    >>> Hello, World!

Here we are creating a new module and executing it as main program so the value of  `__name__`  is set to  `'__main__'`. As a result, the if condition satisfies and the function  `hello()`  gets called.

-----
Now, if created a new file called  `module.py`  with the following code:

```python
import my_module

print(my_module.number)
my_module.hello()
print(my_module.__name__)
```

    
**Expected Output:**

    >>> 4
    >>> Hello, World!
    >>> my_module

As you can see now, the if statement in `my_module` fails to execute because the value of `__name__` is set to `'my_module'`.
