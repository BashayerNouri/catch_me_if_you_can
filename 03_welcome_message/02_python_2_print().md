
Now what we’re going to do is teach our computer to communicate. The gift of speech is valuable, a computer can answer many questions we have about “how” or “why” or “what” it is doing. In Python, the `print()` function is used to tell a computer to talk. The message to be printed should be surrounded by quotes.


For example, if you want to print the following in you console:

```
Hello, World!
```


You should write the following in your Python file:

```python
print("Hello, World!")
```
or
```python
print('Hello, World!')
```

In Python a string is either surrounded by double quotes (`"Hello, World!"`) or single quotes (`'Hello, World!'`). It doesn’t matter which kind you use, just be consistent.

-----

Now find the `catch-me-if-you-can/demo.py` file, Print a greeting message along with your name using the `print()` command, `save` the file and 
then `run` your python code to test it out.


 Output example:


    Hi, My name is Bashayer

***To run the file:***

    $ cd catch_me_if_you_can
    $ python demo.py

Feel free to play with your code. Print anything you like. Perhaps a song lyrics, your favourite book or a small description about yourself. Go crazy!


## Built-in Types

 There are other data types that can be printed using the `print()` function, such as:

### Booleans

- `bool:`  A boolean value of either `True` or `False`. 

  ```python
  print(True)
  print(False)
  ```


### Numbers 

 - `int`: Integer number
     
     ```python
     print(9)
     ```

 - `float`: Floating point number
 
     ```python
     print(3.14)
     ```


### Sequences and collections

- `list`: An ordered collection. In Python lists are written with square brackets.
   ```python
   print([1, 2, 3])
     ```

 
- `tuple`: An ordered collection. In Python tuples are written with round brackets
     ```python
     print((1, 2, 3))
     ```

- `set`: An unordered collection of items. In Python sets are written with curly brackets.
     ```python
    print({'red', 'green', 'blue'})
     ```
      

 
- `dict`: An unordered collection of unique key-value pairs. In Python dictionaries are written with curly brackets, and they have keys and values.
     ```python
    print({'name': 'Bashayer', 'age': 24})
     ```
     <br>
   Read the above really carefully and try to understand it. Take your time.

 ---
Now find the `catch-me-if-you-can/catch_me_if_you_can.py` file, Print the following output using the `print()` command, `save` the file and 
then `run` your python code to test it out.
 
 ```
 True
 4
 9.11
 ['red','green','blue']
 ('Apple','Bannan','Orange')
 {1, 2, 3}
{'brand': 'volkswagen', 'model': 'jetta', 'year': 2013}
 ```

***To run the file:***

    $ cd catch_me_if_you_can
    $ python demo.py
    
   <br>
   
Now it's thinking time, try to figure out.
<br>

![Meme Think GIF](https://media2.giphy.com/media/a5viI92PAF89q/giphy.gif?cid=ecf05e47d141145b34cc6d77e908ccb4b28825fe0db144db&rid=giphy.gif)

----
So now!

Are you ready the know the answer? 

Let's start!

Your `catch-me-if-you-can/demo.py` file, should look like the following:

```python
print(True)
print(4)
print(9.11)
print(['red','green','blue'])
print(('Apple','Bannan','Orange'))
print({1, 2, 3})
print({'brand': 'volkswagen', 'model': 'jetta', 'year': 2013})```
