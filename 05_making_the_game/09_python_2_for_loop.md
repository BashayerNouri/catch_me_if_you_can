<br>

Now, we are going to do improvements to the code. But before improving the code, you need to understand the `for` loop.


## What is for loop in Python?

The for loop in Python is used to iterate over a sequence ([list](https://www.programiz.com/python-programming/list),  [tuple](https://www.programiz.com/python-programming/tuple),  [string](https://www.programiz.com/python-programming/string)) or other iterable objects. Iterating over a sequence is called traversal.

---

### Syntax of for Loop

```python
for value in sequence:
     Body of for
```

Here,  `value`  is the variable that takes the value of the item inside the sequence on each iteration.

Loop continues until we reach the last item in the sequence. The body of for loop is separated from the rest of the code using indentation.

<br>

<p align=center> </p>

<div align=center>
<p align=center> Flowchart of for Loop <p/>
<img src="https://cdn.programiz.com/sites/tutorial2program/files/forLoop.jpg">

<div/>



---
***Example:***
```python
# Program that prints every word on the list

# List of words
words = ["dog","cat","cinema","bed"]

# iterate over the list
for word in words:
	print(word)
```


***Output:***
```
dog
cat
cinema
bed
```

<br>

Now Open your ```script.py``` file and practice what we learned so far before going into the next task. 

***To run the file:***

    $ cd catch-me-if-you-can
    $ python script.py
    
