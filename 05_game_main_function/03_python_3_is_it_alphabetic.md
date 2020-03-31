Now the real work will start, so grab a very large cup of coffee sit tight and focus. Let's get started.

![adventure time coffee GIF by hoppip](https://media3.giphy.com/media/687qS11pXwjCM/giphy.gif?cid=ecf05e4734aef0502ff1adf2c1d4ef514cf3ba15447e91ea&rid=giphy.gif)


# Trello
> Move card  `As a player, I can know if I didn't add a letter.`  from the  `Backlog`  to the  `Doing`  list.

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
```



Now. look carefully at this code and try to understand it.

![think winnie the pooh GIF](https://media1.giphy.com/media/mRh4cLIYhrs9G/giphy.gif?cid=ecf05e474789509d26c97e92031064b2d3236bf900dcec20&rid=giphy.gif)

 **Let me break it down for you in steps:**
 
```python
while guessed == False and tries > 0:
        print("\nYou have %s tries." % str(tries))
        guess = input("\nEnter one letter or the full word: ").lower()
```

 

 

 - This is `while` loop that ends if the player didn't guess the correct word and runs out of tries.

 - Then we `print` the total number of `tries` the player has.
 - Then we save the player's  input. Means it saves the letter that the user entered in a variable called `guess`
----
```python
if len(guess) == 1:
    if not guess.isalpha():
        print("\n\'%s\' is not a letter, enter a letter!\n" % guess)
        print("\nLetters Guessed: %s\n" % letters_guessed)
```


 - If the player entered only **one letter**:

      ***Case One:*** if this letter is ***not an alphabet***:
      -  `print` "it is not a letter"
      - `print` `letters_guessed` list.
      
---
> The `isalpha()` methods returns “True” if all characters in the string are alphabets, Otherwise, It returns “False”.   

----

## Trello

> Move card  `As a player, I can know if I didn't add a letter.`   to the `Done`  list .
> 
----------

### Git


```
$ git add .
$ git commit -m "working on game functionality"
$ git push
```

----------

Is it dancing time? no, it is not let's continue...

![sad face GIF](https://media3.giphy.com/media/9Y5BbDSkSTiY8/giphy.gif?cid=ecf05e476309bfa2f2e759760a3ccc26a2cca96632cde1f1&rid=giphy.gif)
