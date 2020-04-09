Remamber this code?

```python
# A welcome message
print()
print("Welcome to Catch Me If You Can")
print("Get ready")
print("Starting the game...")
print("Selecting a word...")
```
What if I told you we can change this code into a better and a cleaner way by using the `for` loop?

Stop for  a while and think about it.

How can we `print` the messages using the `for` loop?

<br>

hmmmmm...

<br>

![thinking think GIF by Red Fang](https://media1.giphy.com/media/l3vRioHcAYTTZbXQA/giphy.gif?cid=ecf05e479162bd1ff634da3b63935a514c202f8249615693&rid=giphy.gif)


<br>


Do you wanna know how?

Find the `catch-me-if-you-can/catch_me_if_you_can.py` file, `remove` the old welcome message and `add` the following:

```python
# A welcome message
messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
for messsage in messsages:
    print (messsage)
```

<br>

The `for` loop goes through each element in the `messsages` list, saves it in the variable `messsage` (this variable could be named anything) and then execute the code inside the `for` loop, which is `print` the messages.


---
***Note:***

 You will find this escape character`"\n"`. `"\n"` in Python means a new line.

To know more about escape characters [click here](https://www.w3schools.com/python/gloss_python_escape_characters.asp).



## Final Code

```python
random_word = "cinema"

# A welcome message
messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
for messsage in messsages:
    print (messsage)
    
# prints out the word length
print("\nThe word contains %s letters." % len(random_word))
print(len(random_word) * " _")
```
----------

### Git


```
$ git add .
$ git commit -m "improved the welcome message"
$ git push
```

----------



