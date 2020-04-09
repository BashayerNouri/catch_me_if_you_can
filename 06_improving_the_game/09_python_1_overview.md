You should be very proud of what you accomplished. Good job!


Let's go through everything we've done in this chapter:

 - We learned about  `isalpha()` method
 - We learned about  `append()`  method.
 - We finished building the game.

<br>

Make sure that it's working properly and the correct information is showing. If all is good, push your code.

## ***Final Code:***

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


    status = ''
    for letter in random_word:
        if letter in letters_guessed:
            status += letter
        else:
            status += ' _'
    print(status)

    if status == random_word:
        print("\nCongratulations! the word is \"%s\"" % random_word)
        break

    elif tries == 0:
        print("\nOh no! You have run out of guesses, better luck next time! The word is \"%s\"" % random_word)
```

---

### Git


```
$ git add .
$ git commit -m "finished game functionality"
$ git push
```

----------

Wait.... you forgot something very important.

DANCE TIME

![happy dance GIF](https://media0.giphy.com/media/14qb1Uhf40ndw4/200.webp?cid=ecf05e4764867528fc2eb559da7e5686d6aa874edbf2a666&rid=200.webp)


