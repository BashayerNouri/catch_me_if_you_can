
# Trello
> Move card  `As a player, I can know if I added the wrong letter.`  from the  `Backlog`  to the  `Doing`  list.

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
```

Now. look carefully at this code and try to understand it.

![think winnie the pooh GIF](https://media1.giphy.com/media/mRh4cLIYhrs9G/giphy.gif?cid=ecf05e474789509d26c97e92031064b2d3236bf900dcec20&rid=giphy.gif)

 **We added the following:**
 

```python
elif guess not in random_word:
     print("\n\'%s\' is not part of the word, try another letter.\n" % guess)
     letters_guessed.append(guess)
     tries -=1 
     print("\nLetters Guessed: %s\n" % letters_guessed)
```

 


 - If the player entered only **one letter**:
     
      ***Case three:*** If the letter ***not part of the word***:
      - `print` "not part of the word"
      - add this letter to the `letters_guessed` list by using `append()`
      - minimize `tries` by one.
      - `print` `letters_guessed` list.
      
----
> The `append()` method appends an element to the end of the list.
---
## Trello

> Move card  `As a player, I can know if I added the wrong letter.`   to the `Done`  list .
> 
----------

### Git


```
$ git add .
$ git commit -m "working on game functionality"
$ git push
```

----------




