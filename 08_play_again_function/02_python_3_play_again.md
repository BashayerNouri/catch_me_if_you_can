﻿Find the `catch-me-if-you-can/catch_me_if_you_can.py` file, and before the `main()` function add the following:

```python
# restart or quit the game
def play_again():
    print("\nWould you like to play again?")
    time.sleep(1)

    while True:
        answer = input("If yes enter \"yes\" or \"y\". If no enter \"no\" or \"n\" ").lower()
        if answer == "y" or answer == "yes":
            main()
        elif answer == "n" or answer == "no":
        	print("\nGoodbye. See you next time!")
            break
        else:
            print("Please enter \"yes\" or \"y\" or \"no\" or \"n\" ")
            time.sleep(1)

```
---
And now to make this work, we need to call the `play_again()` function at the end of the `main()` function like this:

```python
play_again()
```

Now. look carefully at this code and try to understand it.

![think winnie the pooh GIF](https://media1.giphy.com/media/mRh4cLIYhrs9G/giphy.gif?cid=ecf05e474789509d26c97e92031064b2d3236bf900dcec20&rid=giphy.gif)

 **Let me break it down for you:**

 - We have a `while` loop that only ends if the player answered with yes or no.
  
    Now what are the cases that will end our `while` loop? The following part:

      ```python
        if answer == "y" or answer == "yes":
            main()
        elif answer == "n" or answer == "no":
        	print("\nGoodbye. See you next time!")
            break
        else:
            print("Please enter \"yes\" or \"y\" or \"no\" or \"n\" ")
            time.sleep(1)
   ```


- If the player answered with `yes` or `y`, we called our `main()` function to restart the game.

- If the player answered with `no` or `n`, it will `print` a goodbye message and `break` the `while` loop.

- Any other answers, let's say the player entered Leonardo DiCaprio, the `while` loop will keep going with the following output until the player enters the right input:
   ```
   >>> Please enter "yes" or "y" or    "no" or "n" 
   ```


---
And now we are done!

![Great Job Ok GIF](https://media2.giphy.com/media/xHMIDAy1qkzNS/giphy.gif?cid=ecf05e47e9aa788d6c80f2e85ffc367f396f2a0ed8528ac2&rid=giphy.gif)

***Final Code***
-----
```python
import random
import time



# print the welcome message after 1.3 seconds
def welcome_message():
    messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
    for messsage in messsages:
        print (messsage)
        time.sleep(1.3)


# generates a random word each time you start playing the game
def get_random_word():
    file = open("wordlist.txt")
    words = file.readlines() 
    random_word = random.choice(words)
    random_word = random_word.strip("\n")
    random_word = random_word.strip("\r")
    random_word = random_word.lower()
    file.close()
    return random_word

random_word = get_random_word()

# restart or quit the game
def play_again():
    print("\nWould you like to play again?")
    time.sleep(1)

    while True:
        answer = input("If yes enter \"yes\" or \"y\". If no enter \"no\" or \"n\" ").lower()
        if answer == "y" or answer == "yes":
            main()
        elif answer == "n" or answer == "no":
            print("\nGoodbye. See you next time!")
            break
        else:
            print("Please enter \"yes\" or \"y\" or \"no\" or \"n\" ")
            time.sleep(1)

def main():

    letters_guessed = []

    # The player has 5 tries at the beginning of the game. 
    tries = 5

    # A welcome message
    welcome_message()

    print("\nThe word contains", len(random_word), 'letters. \n')
    print(len(random_word) * (" _"))
    
    while tries > 0:
        print("\nYou have %s tries." % tries)
        guess = input("\nEnter one letter or the full word: ").lower()

        # Case 1: if the player enters a single letter.
        if len(guess) == 1:
            if not guess.isalpha():
                print("\n\'%s\' is not a letter, enter a letter!\n" % guess)
                print("\nLetters Guessed: %s\n" % letters_guessed)

            elif guess in letters_guessed:
                print("\n\'%s\' has been guessed before, try another letter.\n" % guess)
                print("\nLetters Guessed: %s\n" % letters_guessed)

            elif guess not in random_word:
                print("\n\'%s\' is not part of the word, try another letter.\n" % guess)
                tries -=1
                letters_guessed.append(guess)
                print("\nLetters Guessed: %s\n" % letters_guessed)

            else:
                print("\nWell done, that letter exists in the word!\n")
                letters_guessed.append(guess)
                print("\nLetters Guessed: %s\n" % letters_guessed)

        # Case 2: if the player enters a full word.
        elif len(guess) == len(random_word):
            if guess == random_word:
                print("\nCongratulations! the word is \"%s\"" % random_word)
                break

            else:
                print("\nSomething is not part of the word, try again.\n")
                tries -= 1

        # Case 3: if the player enters a full word but it's a wrong word.
        else:
            print("\n\"%s\" lenght does not equal to \"%s\" letters, try another!\n" % (guess,len(random_word)))


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


    play_again()

if __name__ == '__main__':
    main()
```
