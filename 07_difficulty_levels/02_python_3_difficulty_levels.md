

First things first, we need to need to specify the levels. So we will create a dictionary that contains ***levels*** as `keys` and ***number of attempts*** as the keys `values`

So in the `main()` function delete this:

```python
# The player has 10 tries at the beginning of the game. 
tries = 10
```
and instead, add the following:
```python

    level = { 
    "easy": 10,
    "intermediate": 6,
    "difficult":  2,
    }

    selection = False
```
And now before going into the game difficulty functionality let's add the following in the `main()`:

```python
    level = { 
    "easy": 10,
    "intermediate": 6,
    "difficult":  2,
    }

    selection = False
    letters_guessed = []
    guessed = False 
    
    print("\nThere are multiple difficulty settings shown below:")
    time.sleep(1)
    print("\t1. Easy (10 attempts)")
    time.sleep(1)
    print("\t2. Intermediate (6 attempts)")
    time.sleep(1)
    print("\t3. Difficult (2 attempts)")
    time.sleep(1)
 ```

And now we will add the the game difficulty functionality, in the `main()` add the following:

```python
    level = { 
    "easy": 10,
    "intermediate": 6,
    "difficult":  2,
    }

    selection = False
    letters_guessed = []
    guessed = False
    

    print("\nThere are multiple difficulty settings shown below:")
    time.sleep(1)
    print("\t1. Easy (10 attempts)")
    time.sleep(1)
    print("\t2. Intermediate (6 attempts)")
    time.sleep(1)
    print("\t3. Difficult (2 attempts)")
    time.sleep(1)
    
    while selection == False:
        level_selection = input("\nSelect A Level: ")
        try:
            level_selection = int(level_selection)
            if level_selection == 1:
                tries = level['easy']
                selection = True
            elif level_selection == 2:
                tries = level['intermediate']
                selection = True
            elif level_selection == 3:
                 tries = level['difficult']
                 selection = True
            else:
                print("Please select a number from 1 to 3...")
        except ValueError:
                print("You didn't enter a number!")

```
---

Now before explaining this code try to take a look at it, look at each code really carefully and take your time to understand it.

![think sesame street GIF](https://media2.giphy.com/media/8acGIeFnqLA7S/giphy.gif?cid=ecf05e47068c7f80a41019d157f10ebe1c9436e15808a176&rid=giphy.gif)

---
 **Let me break it down for you:**

- We have a `while` loop that will end if the player added a correct level selection.

- We have `try/except` where the `try` block lets you test a block of code for errors and the `except` block lets you handle the error.

     If you take a look at this part:
   ```python
   except ValueError:
           print("You didn't enter a number!")
   ```
   You will see a `ValueError` _exception_, raised when an operation or function receives an argument that has the right type but an inappropriate value, and the situation is not described by a more precise exception such as  [`IndexError`]

   If you take a closer look at this code:

  ```python
   level_selection = int(level_selection)
   ```

   You will find that we added `int()` method,  which means the selected level should be an integer. 

   **For example**, if the player enters a letter instead of a number. The `ValueError` will raise and this message will show up:
    
      >>> You didn't enter a number!

---
So now the ```main()``` function will look like this:
```python
def main():

    level = { 
    "easy": 10,
    "intermediate": 6,
    "difficult":  2,
    }

    selection = False
    letters_guessed = []
    guessed = False
    

    print("\nThere are multiple difficulty settings shown below:")
    time.sleep(1)
    print("\t1. Easy (10 attempts)")
    time.sleep(1)
    print("\t2. Intermediate (6 attempts)")
    time.sleep(1)
    print("\t3. Difficult (2 attempts)")
    time.sleep(1)

    while selection == False:
        level_selection = input("\nSelect A Level: ")
        try:
            level_selection = int(level_selection)
            if level_selection == 1:
                tries = level['easy']
                selection = True
            elif level_selection == 2:
                tries = level['intermediate']
                selection = True
            elif level_selection == 3:
                 tries = level['difficult']
                 selection = True
            else:
                print("Please select a number from 1 to 3...")
        except ValueError:
                print("You didn't enter a number!")

    weclcome_message()

    print("\nThe word contains", len(random_word), 'letters. \n')
    print(len(random_word) * (" _"))
    
...
    play_again()
...

if __name__ == '__main__':
    main()

```

---
And we are done! 

![running man dancing GIF](https://media3.giphy.com/media/hVYVYZZBgF50k/giphy.gif?cid=ecf05e47340eef31914637d97def3731ae1df59a5e57d733&rid=giphy.gif)

***Final Code***
-----

```python
import random
import time

picture = ['''
                +---+
                |   |
               _O_  |
                |   |
               / \  |
                    |
              =========''', 
        '''
                +---+
                    |
                    |
               \O/  |
                |   |
               | |  |
              =========''']



def get_random_word():
    file = open("wordlist.txt", "r")
    words = file.readlines() 
    random_word = random.choice(words)
    random_word = random_word.strip("\n")
    random_word = random_word.strip("\r")
    random_word = random_word.lower()
    file.close()
    return random_word

random_word = get_random_word()

def weclcome_message():
    messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
    for messsage in messsages:
        print (messsage)
        time.sleep(1.3)

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
            print("Please enter \"yes\" or \"y\". \"no\" or \"n\" ")
            time.sleep(1)

def main():

    level = { 
    "easy": 10,
    "intermediate": 6,
    "difficult":  2,
    }

    selection = False
    letters_guessed = []
    guessed = False
    

    print("\nThere are multiple difficulty settings shown below:")
    time.sleep(1)
    print("\t1. Easy (10 attempts)")
    time.sleep(1)
    print("\t2. Intermediate (6 attempts)")
    time.sleep(1)
    print("\t3. Difficult (2 attempts)")
    time.sleep(1)

    while selection == False:
        level_selection = input("\nSelect A Level: ")
        try:
            level_selection = int(level_selection)
            if level_selection == 1:
                tries = level['easy']
                selection = True
            elif level_selection == 2:
                tries = level['intermediate']
                selection = True
            elif level_selection == 3:
                 tries = level['difficult']
                 selection = True
            else:
                print("Please select a number from 1 to 3...")
        except ValueError:
                print("You didn't enter a number!")

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

    play_again()

if __name__ == '__main__':
    main()
```
