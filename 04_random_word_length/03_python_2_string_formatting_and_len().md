Strings in Python have a unique built-in operation that can be accessed with the `%` operator. This lets you do simple positional formatting very easily. 

Here’s a simple example:

```python
# prints a random word
word = "piano"
print("The random word is: %s" % word)
```
***Output***
```
>>> The random word is: piano
```
---
In the string, you can specify the position of the variables using:

-   `%s`: for a variable of type  `string`.
-   `%d`: for a variable of type  `integer`.
-   `%f`: for a variable of type  `float`.


---
You can also use two or more argument specifiers, use a tuple (parentheses):

```python
# prints out a word, and the word length
word = "piano"
word_length = 5
print("The random word is %s. And with a length of %d" % (word, word_length))
```
***Output***
```
>>> The random word is piano. And with a length of 5
```

<br>

## Python `len()` function 

Instead of writing the length in a variable and then print it like the above example. In Python, there is a function that returns the number of characters in the string. called `len()`. 

```python
# prints the word length using len()
word = "piano"
print(len(word))
```
***Output***
```
>>> 5
```



So now, we can edit the previous example and make it better like this:

```python
# prints out a word, and the word length using len()
word = "piano"
print("The random word is %s. And with a length of %d" % (word, len(word)))
```

***Output***
```
>>> The random word is piano. And with a length of 5
```

----


Now before going into the next task. Open your ```script.py``` file and practice what we learned so far. 

GO CRAZY!


