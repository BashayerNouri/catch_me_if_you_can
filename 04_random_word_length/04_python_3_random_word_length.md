﻿<br>

And we are done with the lessons. Let's start building.

---

Find the `catch-me-if-you-can/catch_me_if_you_can.py` file.

And after your welcome message, create a variable called `random_word` with any string word you like.    

Print the `random_word` length with a message like the following output using the `print()` command.

`save` the file and then `run` your python code to test it out.

***The output should be:***
```
>>> The word contains 6 letters.
```

***Hint:*** use the `len()` function to print the word length.

---

***To run the file:***

    $ cd catch-me-if-you-can
    $ python catch_me_if_you_can.py
   
   ---
<br>

Thinking time...

<br>

![think winnie the pooh GIF](https://media1.giphy.com/media/mRh4cLIYhrs9G/giphy.gif?cid=ecf05e47204de58667707c71cb4faf2d18d22b779688046a&rid=giphy.gif)

<br>

----

Are you ready the know the answer? 


Let's start!

Your `catch-me-if-you-can/catch-me-if-you-can.py` file, will look like the following:

```python
random_word = "cinema"

# A welcome message
print()
print("Welcome to Catch Me If You Can")
print("Get ready")
print("Starting the game...")
print("Selecting a word...")

# prints the word length
print("\nThe word contains %s letters." % len(random_word))
```
<br>

***We added the following:***

A variable called `random_word` that contains a secret word.

```python
random_word = "cinema"
```
And then, `print` the random word length.

```python
# prints the word length
print("\nThe word contains %s letters." % len(random_word))
```
---
*Pay attention at this part:*
```python
print("\nThe word contains %s letters." % len(random_word))
```

 You will find this escape character`"\n"`. `"\n"` in Python means a new line.

To know more about escape characters [click here](https://www.w3schools.com/python/gloss_python_escape_characters.asp).

---
The output before adding the escape character `"\n"`

![no-new](https://i.ibb.co/99f8m8f/no-new.png)

<br>

The output after adding the escape character `"\n"`

![new](https://i.ibb.co/NVSG2zQ/new.png)



## Final Touch


Add the following code on the `catch-me-if-you-can/catch-me-if-you-can.py` file.

```python
random_word = "cinema"

# A welcome message
print()
print("Welcome to Catch Me If You Can")
print("Get ready")
print("Starting the game...")
print("Selecting a word...")

# prints the word length
print("\nThe word contains %s letters." % len(random_word))
print(len(random_word) * " _")
```
<br>

***The new line is:***
```python
print(len(random_word) * " _")
```
This code print this `_` character based on the number of letters in the string.

<br>

***So the output will look like this:***


![we](https://i.ibb.co/K5z0mVy/we.gif)



