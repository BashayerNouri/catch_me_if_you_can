
# Trello
> Move card  `As a player, I can know if I didn't add a letter.`  from the  `Backlog`  to the  `Doing`  list.

----------

## Python String `isalpha()`

The `isalpha()` method returns `True` if all characters in the string are alphabets. If not, it returns `False`.

***For example:***
```python
guess = input("Enter a letter: ").lower()

# Check if the input is a letter or not
if not guess.isalpha():
    print("Not a letter, enter a letter!")
else:
    print("this is a letter")
```

***Output:***

![alpha](https://i.ibb.co/rbpdJyg/alpha.gif)

<br>

Now Open your `script.py` file and practice what we learned.

-----
Now, before going into the code let me explain what we are trying to build.

 Right now we want to add in our program two things:

 - First, we want to check if the player input is one letter only. 
 
   ***Hint:*** we will use the `len()` function for that.
 
 - Second,  if the above condition is `True`, we will check if the player input is alphabetic.

<br>


*This will help you have a better idea of what we're trying to build in this chapter:*


![LETTER](https://i.ibb.co/xzhF86d/LETTER.gif)

<br>

Take some time to try to figure out how we are going to do this.

<br>

![thinking think GIF by Nick Jonas](https://media2.giphy.com/media/872o15eAXFBw66UfNl/giphy.gif?cid=ecf05e47f6aa97e62ac639d89b27238df25ef1204a7c1300&rid=giphy.gif =350x300)

<br>

Now...

<br>

This is how `catch-me-if-you-can/catch_me_if_you_can.py` file will look like:
```python

random_word = "cinema"
tries = 5

# A welcome message
messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
for messsage in messsages:
    print (messsage)


# prints out the word length
print("\nThe word contains %s letters." % len(random_word))
print(len(random_word) * (" _"))


# A `while` loop that breaks only if the number of `tries` equals `zero`
while tries > 0:
    print("\nYou have %s tries." % tries)
    guess = input("\nEnter one letter or the full word: ").lower()


    # Case 1: if the player enters a single letter.
    if len(guess) == 1:
        if not guess.isalpha():
            print("\n\'%s\' is not a letter, enter a letter!\n" % guess)


    # Case 2: if the player enters a full word.
    elif len(guess) == len(random_word):
        if guess == random_word:
            print("\nCongratulations! the word is %s" % random_word)
            break

        else:
            print("\nSomething is not part of the word, try again.")
            tries -=1


    # Case 3: if the player enters a full word but it's a wrong word.
    else:
        print("\n%s lenght does not equal to %s letters, try another!" % (guess,len(random_word)))
        
```

<br>

So what we added? We added the following code:
```python
# Case 1: if the player enters a single letter.
if len(guess) == 1:
    if not guess.isalpha():
        print("\n\'%s\' is not a letter, enter a letter!\n" % guess)
```
<br>

We added a new `if` statement that does the following:

 - Check if the player input is one letter only using the `len()` function 
    ```python
    if len(guess) == 1
    ```
 
 - If the above condition is `True`, it will check if the player input is alphabetic.
     ```python
     if not guess.isalpha():
        print("\n\'%s\' is not a letter, enter a letter!\n" % guess)
     ```


##  Trello

  

> Move card `As a player, I can know if I didn't add a letter.` to the `Done` list .

>

----------

###  Git

```
$ git add .
$ git commit -m "working on game functionality"
$ git push

```

  

----------
