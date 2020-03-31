In this section we are going to add some status to our code.

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


            status = ''
            if guessed == False:
                for letter in random_word:
                    if letter in letters_guessed:
                        status += letter
                    else:
                        status += ' _'
                print(status)

            if status == random_word:
                print(picture[1])
                print("\nCongratulations! the word is \"%s\"" % random_word)
                guessed = True

            elif tries == 0:
                print(picture[0])
                print("\nOh no! You have run out of guesses, better luck next time! The word is \"%s\"" % random_word)
```

 **We added the following:**
 
```python
status = ''
if guessed == False:
    for letter in random_word:
        if letter in letters_guessed:
            status += letter
        else:
            status += ' _'
    print(status)

if status == random_word:
     print(picture[1])
     print("\nCongratulations! the word is \"%s\"" % random_word)
     guessed = True

elif tries == 0:
    print(picture[0])
    print("\nOh no! You have run out of guesses, better luck next time! The word is \"%s\"" % random_word)
    
```


---
**Let me explain this code step by step:**


```python
if guessed == False:
    for letter in random_word:
        if letter in letters_guessed:
            status += letter
        else:
            status += ' _'
    print(status)
    
```

The summary of this code is, if a letter in the random word is correctly guessed, the character `"_"` will be replaced with the correct letter.

***Example:***

> The word contains 5 letters.
> 
>  **`_ _ _ _ _`**   
>  
> You have 10 tries.
>
>---
>
> Enter one letter or the full word: **e**
> 
> Well done, that letter exists in the word!
> 
> 
> Letters Guessed: ['e']
> 
>  **`_ _ e e _`**    
> 
> You have 10 tries.
> 
>------
>
> Enter one letter or the full word: **a**
> 
> 'a' is not part of the word, try another letter.
> 
> 
> Letters Guessed: ['e', 'a']
> 
>  **`_ _ e e _`**    
> 
> You have 9 tries.
----

```python
if status == random_word:
     print(picture[1])
     print("\nCongratulations! the word is \"%s\"" % random_word)
     guessed = True
```

         
If the player successfully guessed every letter.
- `print(picture[1])` which means access and `print` the item with the index (1) in the `picture` list.
-  `print` "a win message"
-  make `guessed = True` to end the `while` loop.

    ```python
    elif tries == 0:
        print(picture[0])
        print("\nOh no! You have run out of guesses, better luck next time! The word is \"%s\"" % random_word)
        
    ```



If the play ran out of tries:
- `print` a losing message 

 - `print(picture[0])` which means access and `print` the item with the index (0) in the `picture` list.
     



