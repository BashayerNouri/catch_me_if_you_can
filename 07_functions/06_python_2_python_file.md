<br>

Now, our next lesson...

Right now, you have a variable called `random_word` that we use as our secret word. But what if you want a different word each time you play the game?

That's what we are going to do in the next sections, but before we jump into that you need to understand some concepts first.



## What is a file?

File is a named location on disk to store related information.

When we want to read from or write to a file we need to open it first. When we are done, it needs to be closed, so that resources that are tied with the file are freed.

Hence, in Python, a file operation takes place in the following order.

1.  Open a file
2.  Read or write (perform operation)
3.  Close the file


Now, in the `catch-me-if-you-can` folder, open the `wordlist.txt` file and read it.

You will find random words.

## How to open a file in python?

Python has a built-in function  `open()`  to open a file. This function returns a file object, also called a handle, as it is used to read or modify the file accordingly.




```python
f = open("wordlist.txt")
```



## How to read files in Python?

We can use `readline()` method to read individual lines of a file. This method reads a file till the newline, including the newline character.

For example, if we used `readline()` for our `wordlist.txt` file like this:

```python
f = open("wordlist.txt")
words = f.readlines()
```

`words` variable will hold a list that contains `wordlist.txt` words including the newline character:

```python
['bed\n', 'wings\n', 'aliens\n', 'bowling\n', 'sleep\n', 'piano\n', 'commercial\n', 'dream\n', 'environment\n', 'magazine\n', 'cinema\n', 'bed\n', 'language']
```

## How to close a file Using Python?

When we are done with operations to the file, we need to  close the file.

Closing a file will free up the resources that were tied with the file and is done using Python `close()`  method.


```python
f = open("wordlist.txt")
words = f.readlines()
f.close()
```
