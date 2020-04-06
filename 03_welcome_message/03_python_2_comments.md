Comments are very important while writing a program. It describes what's going on inside a program so that a person looking at the source code does not have a hard time figuring it out. You might forget the key details of the program you just wrote in a month's time. So taking the time to explain these concepts in the form of comments is always fruitful.

Text written in a program but not run by the computer is called a comment. Python interprets anything after a hash `#` symbol as a comment.

## Comments in Python

This is how you write a comment on Python
```python
# I'm a comment
```
If you run a file that contains a comment, Python will ignore the comment lines.

---

Now let's take an example from our previous lesson:
```python
# printing a greeting message
print('Hi, My name is Bashayer')
```

**Output**
```
Hi, My name is Bashayer
```
Here, the comment is:

```python
# printing a greeting message
```
This line is ignored by the Python interpreter.

Everything that comes after  `#`  is ignored. 

We can also write a cooment in a single line like this:
```python
print(4) # prints an integer
```
The output of this program will be the same as in **Example 1**. The interpreter ignores all the text after `#`.

<br>

Now, find the `catch-me-if-you-can/demo.py` file and comment your codes.