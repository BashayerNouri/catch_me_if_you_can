

# Trello
> Move card  `As a player, I can know if I added the right letter.`  from the  `Backlog`  to the  `Doing`  list.

----------

In this section, we are trying to check if the input letter is part of the word.

This is the last case in the game.

![correct](https://i.ibb.co/z6JBctf/correct.gif)

----
Now take some time and try to figure out how we are going to check if the input letter is part of the word.

<br>

![thinking think GIF by Nick Jonas](https://media2.giphy.com/media/872o15eAXFBw66UfNl/giphy.gif?cid=ecf05e47f6aa97e62ac639d89b27238df25ef1204a7c1300&rid=giphy.gif =300x300)

<br>

Now...

<br>

This is how `catch-me-if-you-can/catch_me_if_you_can.py` file will look like:

```python
random_word = "cinema"
letters_guessed = []
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
            print("\nLetters Guessed: %s\n"  %  letters_guessed)

        elif guess in letters_guessed:
            print("\n\'%s\' has been guessed before, try another letter.\n" % guess)
            print("\nLetters Guessed: %s\n" % letters_guessed)

        elif guess not in random_word:
            print("\n\'%s\' is not part of the word, try another letter.\n" % guess)
            tries -= 1
            letters_guessed.append(guess)
            print("\nLetters Guessed: %s\n"  %  letters_guessed)
        else:
            print("\nWell done, that letter exists in the word!\n")
            letters_guessed.append(guess)
            print("\nLetters Guessed: %s\n" % letters_guessed)



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
We added the following:
```python
else:
  print("\nWell done, that letter exists in the word!\n")
  letters_guessed.append(guess)
  print("\nLetters Guessed: %s\n" % letters_guessed)
```

A final statement:

 - Which means if all other cases are not `True`, that means player added a correct letter.
 
 This part:
```python
letters_guessed.append(guess)
print("\nLetters Guessed: %s\n"  %  letters_guessed)
```

Means:
- Any letters from the user input `guess` will be added in the `letters_guessed` list using the `append()` method.

- Then, we will `print` this list.


## Trello

> Move card  `As a player, I can know if I added the right letter.`   to the `Done`  list .
> 
----------

### Git


```
$ git add .
$ git commit -m "working on game functionality"
$ git push
```

----------




