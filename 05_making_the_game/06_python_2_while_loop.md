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
<div align=center>
<p align=center> Flowchart of while Loop <p/>
<img src="https://cdn.programiz.com/sites/tutorial2program/files/whileLoopFlowchart.jpg">

<div/>


## Python break statement


The Python **`break`** statement immediately terminates a loop entirely.

[Click here](https://cdn.programiz.com/sites/tutorial2program/files/flowchart-break-statement.jpg) to read more.



<div align=center>
<p align=center> Flowchart of break statement <p/>
<img 
width="350"
src="https://cdn.programiz.com/sites/tutorial2program/files/flowchart-break-statement.jpg">

<div/>



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
<br>

***Output:***

![out](https://i.ibb.co/j5PVxvG/out.gif)

<br>

Now Open your ```script.py``` file and practice what we learned so far.

***To run the file:***

    $ cd catch-me-if-you-can
    $ python script.py
    
