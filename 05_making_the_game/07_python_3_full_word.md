<br>

Now Let's start building....

![done](https://i.ibb.co/gTzdRVd/done.gif)


# Trello
> Move card  `As a player, I can know if I added the right or wrong full word.`  from the  `Backlog`  to the  `Doing`  list.

----------

This is how `catch-me-if-you-can/catch_me_if_you_can.py` file will look like:

```python
random_word = "cinema"

# A welcome message
messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
for messsage in messsages:
    print (messsage)

# prints out the word length
print("\nThe word contains %s letters." % len(random_word))
print(len(random_word) * (" _"))

guess = input("\nEnter a full word: ").lower()

# check the user input
if len(guess) == len(random_word):
    if guess == random_word:
        print("\nCongratulations! the word is %s" % random_word)
    else:
        print("\nSomething is not part of the word, try again.")
else:
    print("\n%s lenght does not equal to %s letters, try another!" % (guess,len(random_word)))

```

<br>


 **We added the following:**
```python
guess = input("\nEnter a full word: ").lower()

# check the user input
if len(guess) == len(random_word):
    if guess == random_word:
        print("\nCongratulations! the word is %s" % random_word)
    else:
        print("\nSomething is not part of the word, try again.")
else:
    print("\n%s lenght does not equal to %s letters, try another!" % (guess,len(random_word)))
```
<br>

Now. look carefully at this code and try to understand it.

<br>

![think winnie the pooh GIF](https://media1.giphy.com/media/mRh4cLIYhrs9G/giphy.gif?cid=ecf05e474789509d26c97e92031064b2d3236bf900dcec20&rid=giphy.gif)

<br>

 **Let me break it down for you in steps:**
 

First, we will save the player input in a variable called `guess`. Then, we will check the variable case:

   - If the length of the variable `guess` is the same length as the secret word. It will enter the other `if..else` statement.
   
      - Which is, if the variable `guess`, is the same as the secret word. Then, a winning message will be printed.
      
      - Else, if the variable `guess`, is **not** the same as the secret word. Then, a warning message will be printed.
  
  - Else, for example the length of the variable `guess` is **not** the same as the length of the secret word. For example, the player entered "cinemaaa" and the word is "cinema". Then, a warning message will be printed.


---
***Note:***

 You will find this escape character`"\n"`. `"\n"` in Python means a new line.

To know more about escape characters [click here](https://www.w3schools.com/python/gloss_python_escape_characters.asp).

---
## Trello

> Move card  `As a player, I can know if I added the right or wrong full word.`   to the `Done`  list .
> 
----------

### Git


```
$ git add .
$ git commit -m "working on game functionality"
$ git push
```

----------




