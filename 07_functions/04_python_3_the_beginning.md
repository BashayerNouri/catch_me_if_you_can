<br>

And we are done with the lessons. Now let's get some work done and turn the game into a function.

The `catch_me_if_you_can.py` file will basically look like this:

```python
def main():
   #write your code here

if __name__ == '__main__':
    main()
```
The following is used to call the ***main*** function.

```python
if __name__ == '__main__':
    main()
```
---
Now, think about it for a while...

Try to figure out how we are going to turn our code into a function.

![think winnie the pooh GIF](https://media2.giphy.com/media/mRh4cLIYhrs9G/giphy.gif?cid=ecf05e477f3668e9be242fed760055c83eb7cea511df8307&rid=giphy.gif)

---

Now...

Find the `catch-me-if-you-can/catch_me_if_you_can.py` file, `remove` everthing in the file, and `add` the following: 


```python

def main():

    random_word = "cinema"
    letters_guessed = []

    # The player has 5 tries at the beginning of the game. 
    tries = 5

    # A welcome message
    messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
    for messsage in messsages:
        print (messsage)

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
<br>

Take a moment.. read the file very carefully and try to figure out what we did.

<br>


![think winnie the pooh GIF](https://media2.giphy.com/media/mRh4cLIYhrs9G/giphy.gif?cid=ecf05e477f3668e9be242fed760055c83eb7cea511df8307&rid=giphy.gif)

<br>

----
So what did we do? 

The code is the same, but all we did is that we added the code inside a function called ` main()`:

```python
def main():
``` 

Then, we called the `main()` function at the end using:
```python
if __name__ == '__main__':
    main()
```

<br>

And that's it. Congratulation, you just created your first function in the game!

---


### Git


```
$ git add .
$ git commit -m "created the main function"
$ git push
```
