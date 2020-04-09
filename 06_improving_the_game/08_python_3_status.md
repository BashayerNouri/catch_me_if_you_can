In this section we are going to add some simple and easy status to our code.

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


    status = ''
    for letter in random_word:
        if letter in letters_guessed:
            status += letter
        else:
            status += ' _'
    print(status)

    if status == random_word:
        print("\nCongratulations! the word is \"%s\"" % random_word)

    elif tries == 0:
        print("\nOh no! You have run out of guesses, better luck next time! The word is \"%s\"" % random_word)
```

                    

 **We added the following:**
 ```python
 
    status = ''
    for letter in random_word:
        if letter in letters_guessed:
            status += letter
        else:
            status += ' _'
    print(status)

    if status == random_word:
        print("\nCongratulations! the word is \"%s\"" % random_word)

    elif tries == 0:
        print("\nOh no! You have run out of guesses, better luck next time! The word is \"%s\"" % random_word)

```
---
**Let me explain this code step by step:**


    if guessed == False:
        for letter in random_word:
            if letter in letters_guessed:
                status += letter
            else:
                status += ' _'
        print(status)

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

    if status == random_word:
         print("\nCongratulations! the word is \"%s\"" % random_word)
         
If the player successfully guessed every letter.

-  It will `print` "a winning message"

If the play ran out of tries:

     elif tries == 0:
        print("\nOh no! You have run out of guesses, better luck next time! The word is \"%s\"" % random_word)
            



- It will `print` a "losing message"



