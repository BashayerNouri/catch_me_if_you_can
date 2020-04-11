
A conditional statement is a statement that checks if a certain condition is `True` to run a certain block of code.

## Syntax of if...elif...else

```python
if test expression:
    Body of if
elif test expression:
    Body of elif
else: 
    Body of else
```
It will check the first condition if it was  `True`, only the block of code under it will run. Otherwise, it will check the condition below and run the block of code under it if the condition was  `True`. Finally, it will go to the block of code under  `else`  if none were  `True`.

-----

The  `elif`  is short for else if. It allows us to check for multiple expressions.

If the condition for  `if`  is  `False`, it checks the condition of the next  `elif`  block and so on.

If all the conditions are  `False`, the body of else is executed.

Only one block among the several  `if...elif...else`  blocks is executed according to the condition.

The  `if`  block can have only one  `else`  block. But it can have multiple  `elif`  blocks.

You can read more about this [here](https://www.programiz.com/python-programming/if-elif-else).

---
***Example:***

In this program, we check if the number is positive or negative or zero and display an appropriate message.

```python

number = 3

# Try these two variations as well:
# number = 0
# number = -4

if number > 0:
    print("Positive number")
elif number == 0:
    print("Zero")
else:
    print("Negative number")
```

<br>

Now before jumping into the answer. Take your time and figure out which condition will become `True` and which message will be printed.

<br>

![thinking think GIF by Red Fang](https://media1.giphy.com/media/l3vRioHcAYTTZbXQA/giphy.gif?cid=ecf05e479162bd1ff634da3b63935a514c202f8249615693&rid=giphy.gif =300x300)


<br>

The answer is.......

<br>

***Example output:***
```
>>> Positive number
```

<br>

Now Open your ```script.py``` file and practice what we learned so far before going into the next task. 

***To run the file:***

    $ cd catch-me-if-you-can
    $ python script.py
    
