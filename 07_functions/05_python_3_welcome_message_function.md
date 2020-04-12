
<br>

Now, we are going to do some improvements to the welcome message and turn it into a function, and then call this function in the `main()` function.

But before we explain how were are going to do that, you need to understand the `sleep()` function.

## Python sleep()

 The `sleep()` function suspends (waits) execution of the current thread for a given number of seconds.

Python has a module named  [time](https://www.programiz.com/python-programming/time "Python time Module")  which provides several useful functions to handle time-related tasks. One of the popular functions among them is  `sleep()`.

The  `sleep()`  function suspends execution of the current thread for a given number of seconds.


## Example:

```python
import time

print("Printed immediately.")
time.sleep(3.4)
print("Printed after 3.4 seconds.")
```


Here's how this program works:

-   `"Printed immediately"`  is printed
-   Suspends (Delays) execution for 3.4 seconds.
-   `"Printed after 3.4 seconds"`  is printed.

![sleep](https://i.ibb.co/86zYhfP/sleep.gif)



----


Now, let's improve the welcome message.

Let's start.....

Find the `catch-me-if-you-can/catch_me_if_you_can.py` file. 


Before the `main()` function, add the following:

- At the ***top of the file***, add:
   ```python
   import time
   ```

- And then, ***after the import***, add:
	```python
	# print the welcome message after 1.3 seconds
	def welcome_message():
	    messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
	    for messsage in messsages:
	        print (messsage)
	        time.sleep(1.3)
	``` 


- Last, inside the `main()` function, `remove` the welcome message and then call the `welcome_message()` function like this:

	```python
    def main():

        random_word = "cinema"
        ...
        
        # A welcome message
        welcome_message()
        
        ...  

    if __name__ == '__main__':
        main()
	```

----

So, what we did?

***First***, we grabbed the welcome message and turn it into a function called `welcome_message()`
```python
def welcome_message():
```
***Then,*** to print the welcome message after a number of seconds. We imported the `time` module to use the `sleep()` function like this.

```python
import time
```
```python
print(messsage)
time.sleep(1.3)
```

<br>

And we are done!!!


## Output:
![welcome-func](https://i.ibb.co/8s5VnPR/welcome-func.gif)

## Final Full Code:

```python
import time


# print the welcome message after 1.3 seconds
def welcome_message():
    messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
    for messsage in messsages:
        print (messsage)
        time.sleep(1.3)


def main():

    random_word = "cinema"
    
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
---
### Git


```
$ git add .
$ git commit -m "turned the welcome message into a function"
$ git push
```
