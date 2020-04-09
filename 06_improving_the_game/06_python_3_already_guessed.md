# Trello
> Move card  `As a player, I can know if I already guessed that letter before.`  from the  `Backlog`  to the  `Doing`  list.

----------

In this section, we are trying to check if the input letter is already guessed or not.

![guess](https://i.ibb.co/QpNcJz4/guess.gif)

----

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
So what we added? 

We added the following `if...else` case:
```python
elif guess in letters_guessed:
    print("\n\'%s\' has been guessed before, try another letter.\n" % guess)
    print("\nLetters Guessed: %s\n" % letters_guessed)
```

A new `if...else` statement that does the following:

 - Check if the player  already guessed the letter by checking if the input `guess` is in the `letters_guessed` list or not
 

---
Also, pay attention. We added this statement right before checking if the letter is wrong.

Let me give you a scenario to why we did that:

Let's say the player entered a wrong letter and then he added the same wrong letter again. If we added this statement right after checking if the letter is wrong, the program will go into the first if statement case and will not enter the second if statement case (the one that check if the letter is gussed). So the output will be like this:

![gussed](https://i.ibb.co/KmM2Wrc/gussed.gif)

<br>


##  Trello

  

> Move card `As a player, I can know if I already guessed that letter before.` to the `Done` list .

>

----------

###  Git

  ```
$ git add .
$ git commit -m "working on game functionality"
$ git push
```
