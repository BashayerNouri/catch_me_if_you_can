<br>

Before going into the sections, you should be familiar with Python functions. 

So let' know more about functions.

## What is a function in Python?

In Python, function is a group of related statements that perform a specific task.

Why functions are important?

Functions help break our program into smaller and modular chunks. As our program grows larger and larger, functions make it more organized and manageable.

Furthermore, it avoids repetition and makes code reusable.

---

### Syntax of Function:

```python
def function_name(argument1, argument2, ...):
   statement(s)
   return <SOMETHING>
```


Above shown is a function definition which consists of following components.

1.  Keyword  `def`  marks the start of function header.

3.  A function name to uniquely identify it. Function naming follows the same  [rules of writing identifiers in Python](https://www.programiz.com/python-programming/keywords-identifier#rules "Identifier Rule in Python").
4.  Arguments (parameters) through which we pass values to a function. They are **optional**.
5.  A colon (:) to mark the end of function header.

7.  One or more valid python statements that make up the function body.
8.  An **optional**  `return`  statement to return a value from the function.

----

### How do you write functions in Python?

Functions in python are defined using the block keyword `def`, followed with the function's name as the block's name. 

***For example:***

```python
def my_function():
    print("Hello, World!")
    
my_function()
```

The following is used to call the function and use it.

```python
my_function()
```

 
 ***Output:***
```
>>> Hello, World!
```

***Note:*** to use a function, it needs to be defined before being called in the code.


---
Functions may also receive arguments (variables passed from the caller to the function). 

***For example:***
    
```python
def my_function_with_args(username, greeting):
    print("Hello, %s. I wish you %s"%(username, greeting))

my_function_with_args("Bashayer Nouri", "a great year!")
```


 ***Output:***

```
>>> Hello, Bashayer Nouri. I wish you a great year!
```
----
Functions may return a value to the caller, using the keyword  ```return``` . 

***For example:***
    
```python
def sum_two_numbers(a, b):
    return a + b
    
# after this line x will hold the value 3!
x = sum_two_numbers(1,2)
```

    

<br>

## Built-in Functions


Python has several functions that are readily available for use. These functions are called built-in functions. You've already used some of these functions, like  `print()`,  `input()`, and  `len()`.

For more functions, click  [here](https://docs.python.org/3/library/functions.html).

----
Now before going into the next section. Open your ```script.py``` file and practice. 

***To run the file:***

    $ cd catch-me-if-you-can
    $ python script.py
    

