
# Python List append()

The  `append()`  method adds a single item to the end of the list.

The syntax of the  `append()`  method is:
```python
list.append(item)
```


***Example: Adding Element to a List***
```python

random_word = "cinema"
letters_guessed = []

guess = input("Enter one letter: ").lower()

# Check if the letter is in the random word
if guess not in random_word:
    print("not part of the word, try another letter.")
    letters_guessed.append(guess)
    print("\nLetters Guessed: %s\n"  %  letters_guessed)
else:
    print("part of the word")
    letters_guessed.append(guess)
    print("\nLetters Guessed: %s\n"  %  letters_guessed)
```

<br>

***Output:***

![append](https://i.ibb.co/99XcLN3/append.gif)

<br>

Now Open your `script.py` file and practice what we learned so far before going into the next task.

----

Now we are making some changes in our code.

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
<br>

So what we added? 

We added a available called `letters_guessed` that contains an empty list.

```python
letters_guessed = []
```
And in this part from our previous section:
```python
elif guess not in random_word:
    print("\n\'%s\' is not part of the word, try another letter.\n"  % guess)
    tries -=  1
    letters_guessed.append(guess)
    print("\nLetters Guessed: %s\n"  %  letters_guessed)
```

We added the following:
```python
letters_guessed.append(guess)
print("\nLetters Guessed: %s\n"  %  letters_guessed)
```

Which means:
- Any letters from the user input `guess` will be added in the `letters_guessed` list using the `append()` method.

- Then, we will `print` this list.

<br>

We also will `print` the `letters_guessed` list in case the player didn't enter a letter so we can keep viewing this list and remind the players of their entered letters.

So in:


```python
if not guess.isalpha():
    print("\n\'%s\' is not a letter, enter a letter!\n" % guess)
    print("\nLetters Guessed: %s\n"  %  letters_guessed)
```

We added:
```python
print("\nLetters Guessed: %s\n"  %  letters_guessed)
```

----------

### Git


```
$ git add .
$ git commit -m "working on game functionality"
$ git push
```

----------
