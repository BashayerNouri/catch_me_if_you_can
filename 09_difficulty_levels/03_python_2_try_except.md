<br>

## Exception Handling

When an error occurs, or exception as we call it, Python will normally stop and generate an error message.


***Example***
```python
print(x)
```
***Output***
```
Traceback (most recent call last):
  File "C:\Users\User\Desktop\script.py", line 1, in <module>
    print(x)
NameError: name 'x' is not defined
```
The program will crash and raise an error because  `x`  is not defined.


These exceptions can be handled using the  `try`  statement:

The `try` block will generate an exception, because `x` is not defined:

***Example:***
```python
try:  
	print(x)  
except:  
	print("An exception occurred")
```
----

***Output***
```
>>> An exception occurred
```
Since the try block raises an error, the except block will be executed.




## Built-in Exceptions

There are plenty of built-in exceptions in Python that are raised when corresponding errors occur. 

Such as `ValueError` from the following example:

***Example:***

```python
print("\nThere are multiple difficulty settings shown below:\n")
print("\t1. Easy (10 attempts)")
print("\t2. Intermediate (6 attempts)")
print("\t3. Difficult (2 attempts)")

level = input("\nEnter a level (1, 2 or 3): ")

try:  
	level = int(level)
	print("Your level is %s" % level)  
except ValueError:  
	print("You didn't enter a number!")
```
Since the `input()`  converts any user input into a string. We used a build-in function called `int()`, it changes the type of the data. For example, In this case, the input `level` had to be converted to an integer so we used `int(level)`.

If the player did not enter a number, the `ValueError` exception will be raised with the message `You didn't enter a number!`



***Output:***

![level](https://i.ibb.co/rbxc2rR/level.gif)

---

`ValueError` exception is a type of exception that is raised when an operation or function receives an argument with an inappropriate value assigned to it. The situation is not described by a more precise exception such as  [`IndexError`].

---

Click [here](https://docs.python.org/3/library/exceptions.html) to view more built-in exceptions.

---

Now before building the difficulty levels. Open your ```script.py``` file and practice. 

***To run the file:***

    $ cd catch-me-if-you-can
    $ python script.py
    

