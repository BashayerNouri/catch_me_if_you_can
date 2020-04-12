# Trello
> Move card  `As a player, I can have a randomized word each time I play.`  from the  `Backlog`  to the  `Doing`  list.

----------

Now, let's start building the random word function.

This function should generates a random word each time you start playing the game:


---
Find the `catch-me-if-you-can/catch_me_if_you_can.py` file. 

Before the `main()` function, add the following:

- At the ***top of the file***, add:
   ```python
    import random
   ```

- And then, ***after the import***,  add:

	```python
	# generates a random word each time you start playing the game
	def get_random_word():
	    file = open("wordlist.txt", "r")
	    words = file.readlines() 
	    random_word = random.choice(words)
	    random_word = random_word.strip("\n")
	    random_word = random_word.lower()
	    file.close()
	    return random_word

	random_word = get_random_word()

	```
- Last, inside the `main()` function, `remove`

  ```python 
   random_word = "cinema"
   ```




----

### Let me explain this code step by step:

**What `get_random_word()` do?** 

```python
def get_random_word():
    file = open("wordlist.txt")
    words = file.readlines() 
    random_word = random.choice(words)
    random_word = random_word.strip("\n")
    random_word = random_word.lower()
    file.close()
    return random_word
    
random_word = get_random_word()
```

  
  ***First:***

```python
file = open("wordlist.txt")
words = file.readlines()
```


`open` will open the `wordlist.txt` file.

 `readlines` will read individual lines of `wordlist.txt` file.

`words` variable will contains the following:

```python
['bed\n', 'wings\n', 'aliens\n', 'bowling\n', 'sleep\n', 'piano\n', 'commercial\n', 'dream\n', 'environment\n', 'magazine\n', 'cinema\n', 'bed\n', 'language']
```


***Second:***
    
```python
import random
```
```python
random_word = random.choice(words)
random_word = random_word.strip("\n")
random_word = random_word.lower()
file.close()
return random_word
```


 - The  `random`  module has a set of methods, such as `choice()`  method. You can use it to get a random element or number.
 
 - The  `choice()`  method returns a randomly selected element from the specified sequence. The sequence can be a string, a range, a list, a tuple or any other kind of sequence.
 - The `strip()` method removes any leading (spaces at the beginning) and trailing (spaces at the end) characters. In our case it is used to remove the new line between each word.

> `"\n"` in Python means a new line.
> 
 - The string `lower()` method converts all uppercase characters in a string into lowercase characters and returns it. So no matter how you write words in `wordlist.txt` file, `lower()` method will always return a lowercase characters. 
 
   *For example:* if you wrote BED or bEd in `wordlist.txt` file, it will return bed. 
   
  
   
 - The `close()` method closes an open file.
 - The `return` keyword is to exit a function and return a value.
 - Last, we will call the function inside a variable called `random_word` 
   ```python
   random_word = get_random_word()
    ```

   
<br>


And we are done! DANCE TIME.

![dance party GIF](https://media3.giphy.com/media/zQLjk9d31jlMQ/200.webp?cid=ecf05e472c14286551df905fbe28db803386d8d62547a372&rid=200.webp)


## Final Full code:

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


if __name__ == '__main__':
    main()
```

## Trello

> Move card  `As a player, I can have a randomized word each time I play`   to the `Done`  list .
> 
----------

### Git


```
$ git add .
$ git commit -m "finished random word functionality"
$ git push
```

----------



