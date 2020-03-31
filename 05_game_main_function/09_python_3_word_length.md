
# Trello
> Move card  `As a player, I can know if I entered a word but this word does not equal the length of the secret word.`  from the  `Backlog`  to the  `Doing`  list.

----------


In the `main()` function, add the following code:

```python
def main():

    letters_guessed = []
    guessed = False

    # The player has 10 tries at the beginning of the game. 
    tries = 10

    weclcome_message()

    print("\nThe word contains", len(random_word), 'letters. \n')
    print(len(random_word) * (" _"))
    
    while guessed == False and tries > 0:
            print("\nYou have %s tries." % tries)
            guess = input("\nEnter one letter or the full word: ").lower()

            if len(guess) == 1:
                if not guess.isalpha():
                    print("\n\'%s\' is not a letter, enter a letter!\n" % guess)
                    print("\nLetters Guessed: %s\n" % letters_guessed)

                elif guess in letters_guessed:
                    print("\n\'%s\' has been guessed before, try another letter.\n" % guess)
                    print("\nLetters Guessed: %s\n" % letters_guessed)

                elif guess not in random_word:
                    print("\n\'%s\' is not part of the word, try another letter.\n" % guess)
                    letters_guessed.append(guess)
                    tries -=1
                    print("\nLetters Guessed: %s\n" % letters_guessed)

                elif guess in random_word:
                    print("\nWell done, that letter exists in the word!\n")
                    letters_guessed.append(guess)
                    print("\nLetters Guessed: %s\n" % letters_guessed)

            elif len(guess) == len(random_word):
                if guess == random_word:
                    print(picture[1])
                    print("\nCongratulations! the word is \"%s\"" % random_word)
                    guessed = True

                else:
                    print("\nSomething is not part of the word, try again.\n")
                    tries -=1

            else:
                print("\n\"%s\" lenght does not equal to \"%s\" letters, try another!\n" % (guess,len(random_word)))
```


 **We added the following:**
 
```python
else:
  print("\n\"%s\" lenght does not equal to \"%s\" letters, try another!\n" % (guess,len(random_word)))
```


 If the player entered a **full word** and it is length is not equal to the length of the random word:
 - `print` "lenght does not equal to the word letters"

---
## Trello

> Move card  `As a player, I can know if I entered a word but this word does not equal the length of the secret word.`   to the `Done`  list .
> 
----------

### Git


```
$ git add .
$ git commit -m "working on game functionality"
$ git push
```

----------




