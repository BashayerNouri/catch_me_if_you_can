
# Trello
> Move card  `As a player, I can know if I added the wrong letter.`  from the  `Backlog`  to the  `Doing`  list.

----------

In this section, we are trying to check if the input letter is not part of the word and then minimize the number of `tries` by one.

***For example:***
```python

random_word = "cinema"
tries = 5

guess = input("Enter one letter: ").lower()

# Check if the letter is in the random word
if guess not in random_word:
    print("not part of the word, try another letter.")
    tries -= 1
else:
    print("part of the word")
    
print("\nYou have %s tries." % tries)

```

<br>

***Output:***

![wrong](https://i.ibb.co/Dk4TvdT/wrong.gif)

<br>

Now Open your `script.py` file and practice what we learned so far before going into the next task.

----
Now take some time and try to figure out how we are going to check if the input letter is not part of the word and then minimize the number of `tries` by one in the game.

<br>

![thinking think GIF by Nick Jonas](https://media2.giphy.com/media/872o15eAXFBw66UfNl/giphy.gif?cid=ecf05e47f6aa97e62ac639d89b27238df25ef1204a7c1300&rid=giphy.gif)

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

        elif guess not in random_word:
            print("\n\'%s\' is not part of the word, try another letter.\n" % guess)
            tries -= 1
         

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
elif guess not in random_word:
    print("\n\'%s\' is not part of the word, try another letter.\n"  % guess)
    tries -= 1
```
<br>
We added an `if else`  statement that does the following:

 - Check if the player input is not part of the word.
 
 
 - If the above condition is `True`, then minimize the number of `tries` by one.



## Trello

> Move card  `As a player, I can know if I added the wrong letter.`   to the `Done`  list .
> 
----------

### Git


```
$ git add .
$ git commit -m "working on game functionality"
$ git push
```

----------




