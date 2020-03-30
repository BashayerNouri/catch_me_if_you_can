## What is a file?

File is a named location on disk to store related information. It is used to permanently store data in a non-volatile memory (e.g. hard disk).

When we want to read from or write to a file we need to open it first. When we are done, it needs to be closed, so that resources that are tied with the file are freed.

Hence, in Python, a file operation takes place in the following order.

1.  Open a file
2.  Read or write (perform operation)
3.  Close the file


Open `wordlist.txt` and read it carefully.

## How to open a file?

Python has a built-in function  `open()`  to open a file. This function returns a file object, also called a handle, as it is used to read or modify the file accordingly.

```
>>> f = open("test.txt")    # open file in current directory
>>> f = open("C:/Python33/README.txt")  # specifying full path
```

We can specify the mode while opening a file. In mode, we specify whether we want to read  `'r'`, write  `'w'`  or append  `'a'`  to the file. We also specify if we want to open the file in text mode or binary mode.

The default is reading in text mode. In this mode, we get strings when reading from the file.

On the other hand, binary mode returns bytes and this is the mode to be used when dealing with non-text files like image or exe files.

```
f = open("test.txt")      # equivalent to 'r' or 'rt'
f = open("test.txt",'w')  # write in text mode
f = open("img.bmp",'r+b') # read and write in binary mode
```

## How to close a file Using Python?

When we are done with operations to the file, we need to properly close the file.

Closing a file will free up the resources that were tied with the file and is done using Python `close()`  method.


```
f = open("test.txt")
f.close()
```
## How to read files in Python?

we can use `readline()` method to read individual lines of a file. This method reads a file till the newline, including the newline character.

For example, if we used `readline()` for our `wordlist.txt` file like this:

    file = open("wordlist.txt", "r")
    words = file.readlines() 

`words` variable will hold a list that contains `wordlist.txt` words including the newline character:

    ['bed\n', 'wings\n', 'aliens\n', 'bowling\n', 'sleep\n', 'piano\n', 'commercial\n', 'dream\n', 'environment\n', 'magazine\n', 'cinema\n', 'bed\n', 'language']

