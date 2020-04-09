
Before jumping into our code and explaining what we are trying to build, you need to understand some concepts first.

Now we are going to explain to you variables.

So what are variables?

---

Programming languages offer a method of storing data for reuse. If there is a greeting we want to present, a date we need to reuse, or a user ID we need to remember we can create a  _variable_  which can store a value. In Python, we  _assign_  variables by using the equals sign (`=`).

## Let's Start

```python
# prints a random word
random_word = "guacamole"
print(random_word)
```

_**Output**_

```
>>> guacamole
```

In the above example, we store the message “guacamole” in a variable called  `random_word`. 

***Note:*** Variables can’t have spaces or symbols in their names other than an underscore (`_`).

----------

It’s no coincidence we call these creatures “variables”. If the context of a program changes, we can update a variable but perform the same logical process on it.

```python
# prints a random word
random_word = "guacamole"
print(random_word)

# prints a new random word
random_word = "piano"
print(random_word)
```

_**Output**_

```
>>> guacamole
>>> piano
```

----------

### [](https://github.com/BashayerNouri/catch_me_if_you_can/blob/557b693b5cb371843575e17cd153e2927e481491/03_welcome_message/04_python_2_variables.md#some-types-of-variables)Some types of variables:

-   `String`  : "I am a string"
-   `Integer`  : 4
-   `Float`  : 9.11
-   `Boolean`  : True or False

_**Example:**_

```python
name = "Jigglypuff" # String Variable
weight = 50 # Integer Variable
height = 5.5 # Float Variable
is_cute = True # Boolean Variable

print(name)
print(height)
```

_**Output:**_

```
Jigglypuff
5.5
```

----------
Find the `catch-me-if-you-can/script.py` file and `Comment` any code in the file.

Create a variable called `word` with any string word. 

Print the variable using the `print()` command.

`save` the file and then `run` your python code to test it out.

***Output example:***
```
>>> cinema
```
***To run the file:***

    $ cd catch-me-if-you-can
    $ python script.py
   
   <br>

Think about it, how can we print a variable?


![Meme Think GIF](https://media2.giphy.com/media/a5viI92PAF89q/giphy.gif?cid=ecf05e47d141145b34cc6d77e908ccb4b28825fe0db144db&rid=giphy.gif)

----

Are you ready the know the answer? 

Let's start!

Your `catch-me-if-you-can/script.py` file, should look like the following:

```python
# prints a random word
word = "cinema"
print(word)
```


<br>

You can play with your code and try to `print` different variables with different data types.
