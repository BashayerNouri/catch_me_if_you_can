<br>

And we are done with the lessons. 

Let's start building...

![t](https://i.ibb.co/hc48zrf/t.gif)

# Trello
> Move card  `As a player, I have a specific number of tries`  from the  `Backlog`  to the  `Doing`  list.

----------

Find the `catch-me-if-you-can/catch_me_if_you_can.py` file, and add the following:

```python
random_word = "cinema"
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
    guess = input("\nEnter a full word: ").lower()

    if len(guess) == len(random_word):
        if guess == random_word:
            print("\nCongratulations! the word is %s" % random_word)
            break

        else:
            print("\nSomething is not part of the word, try again.")
            tries -=1

    else:
        print("\n%s lenght does not equal to %s letters, try another!" % (guess,len(random_word)))

```
<br>

So what we did?


 **We added the following:**

 - We created a variable called `tries` to specify the number of attempted up to `5` tries.
    ```python
    tries = 5
    ```

 - Then `print` the variable `tries`.
    ```python
    print("\nYou have %s tries." % tries)
      ```

 
 - If the player added the wrong full word, it will minimize the variable `tries` by one.
    ```python
    tries -=1
    ```
 - And last, we created a `while` loop that breaks only if the number of `tries` equals `zero`, which means you have lost the game.
   ```python
    while tries > 0
    ```
----------

### Git


```
$ git add .
$ git commit -m "added a specific number of tries"
$ git push
```

----------


