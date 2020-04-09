<br>

We are going to add number of tries to our code. But before doing that, you need to understand some concepts first.

![t](https://i.ibb.co/hc48zrf/t.gif)



## What is while loop in Python?

The while loop in Python is used to iterate over a block of code as long as the test expression (condition) is true.

We generally use this loop when we don't know beforehand, the number of times to iterate.

### Syntax of while Loop in Python

```python
while test_expression:
    Body of while
```
---

### Flowchart of while Loop
![while Loop in Python programming](https://cdn.programiz.com/sites/tutorial2program/files/whileLoopFlowchart.jpg)

## Python break statement


The Python **`break`** statement immediately terminates a loop entirely.

[Click here](https://www.programiz.com/python-programming/break-continue) to read more.

![Flowchart of break statement in Python](https://cdn.programiz.com/sites/tutorial2program/files/flowchart-break-statement.jpg)

----
### Example: 

```python

letter = "b"

while True:
    guess = input("Enter a letter: ").lower()
    if guess == letter:
        print("Congratulations!")
        break
    else:
        print("wrong, try again.")
```



