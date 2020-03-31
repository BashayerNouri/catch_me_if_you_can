
After prerequisites, you should be familiar with Python functions, but let me do a quick overview for you.

## What is a function in Python?

In Python, function is a group of related statements that perform a specific task.

Functions help break our program into smaller and modular chunks. As our program grows larger and larger, functions make it more organized and manageable.

Furthermore, it avoids repetition and makes code reusable.

---

### Syntax of Function:

```python
def function_name(parameters):
   """docstring"""
   statement(s)
```


Above shown is a function definition which consists of following components.

1.  Keyword  `def`  marks the start of function header.

3.  A function name to uniquely identify it. Function naming follows the same  [rules of writing identifiers in Python](https://www.programiz.com/python-programming/keywords-identifier#rules "Identifier Rule in Python").
4.  Parameters (arguments) through which we pass values to a function. They are optional.
5.  A colon (:) to mark the end of function header.
6.  Optional documentation string (docstring) to describe what the function does.
7.  One or more valid python statements that make up the function body.
8.  An optional  `return`  statement to return a value from the function.

----

### How do you write functions in Python?

Functions in python are defined using the block keyword "def", followed with the function's name as the block's name. 

***For example:***

```python
def my_function():
    print("Hello, World!")
```

 
 ***Output:***
![1](https://i.ibb.co/tZP0H7C/1.png)

Functions may also receive arguments (variables passed from the caller to the function). 

***For example:***
    
```python
def my_function_with_args(username, greeting):
    print("Hello, %s. I wish you %s"%(username, greeting))
```


 ***Output:***
![2](https://i.ibb.co/jrBTqW6/2.png)

Functions may return a value to the caller, using the keyword  'return' . 

***For example:***
    
```python
def sum_two_numbers(a, b):
    return a + b
```

    
   ---
    
### How do you call functions in Python?

Simply write the function's name followed by (), placing any required arguments within the brackets. 

***For example:***
 Lets call the functions written above (in the previous example):
    
```python
# Define our 3 functions
def my_function():
    print("Hello, World!")

def my_function_with_args(username, greeting):
    print("Hello, %s , From My Function!, I wish you %s"%(username, greeting))

def sum_two_numbers(a, b):
    return a + b

# print(a simple greeting)
my_function()

# print - "Hello, Bashayer Nouri. I wish you a great year!"
my_function_with_args("Bashayer Nouri", "a great year!")

# after this line x will hold the value 3!
x = sum_two_numbers(1,2)
```



