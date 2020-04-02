Comments are very important while writing a program. It describes what's going on inside a program so that a person looking at the source code does not have a hard time figuring it out. You might forget the key details of the program you just wrote in a month's time. So taking the time to explain these concepts in the form of comments is always fruitful.

Text written in a program but not run by the computer is called a comment. Python interprets anything after a hash `#` symbol as a comment.

## Single-Line Comments in Python

### Example 1: Writing Single-Line Comments.

```
# printing a string
print('Hello, World!')
```

**Output**
```
Hello, World!
```
Here, the comment is:

```
# printing a string
```
This line is ignored by the Python interpreter.

Everything that comes after  `#`  is ignored. So, we can also write the above program in a single line as:
```
print('Hello, World!') #printing a string
```
The output of this program will be the same as in **Example 1**. The interpreter ignores all the text after `#`.

------

## Multi-Line Comments in Python

Python doesn't offer a separate way to write multiline comments. However, there are other ways to get around this issue.

We can use  `#`  at the beginning of each line of comment on multiple lines.

### Example 2: Using multiple `#`

```
# it is a
# multiline
# comment
```
Here, each line is treated as a single comment and all of them are ignored.

---

### Example 3: Using String Literals to write Multi-line Comments

```
'''

I am a
multiline comment!

'''
print("Hello World")
```

