# Trello
> Move card  `As a player, I have a specific number of tries`  from the  `Backlog`  to the  `Doing`  list.

----------


And we are done with the lessons. 

***Now let's start building the following:***

In this program, we will include the number of tries and minimize it every time the player guesses the wrong word.

![t](https://i.ibb.co/hc48zrf/t.gif)


<br>

This is how `catch-me-if-you-can/catch_me_if_you_can.py` file will look like:


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

 - Then, `print` the variable `tries`.
    ```python
    print("\nYou have %s tries." % tries)
      ```
- Then, if the player added the right full word, it will `break` the loop,

    ***At this part***
   ```python
   if guess == random_word:
        print("\nCongratulations! the word is %s" % random_word)
        break
   ```
   ***We added:***
   ```python
   break
   ```
 
 - Then, if the player added the wrong full word, it will minimize the variable `tries` by one.
 
    **At this part:**
    ```python
    else:
       print("\nSomething is not part of the word, try again.")
       tries -=1
    ```
    **We added:**
    ```python
    tries -=1
    ```
    **Same as:**
    ```python
    tries = tries - 1
    ```
 - And last, we created a `while` loop that breaks only if the number of `tries` equals `zero`, which means you have lost the game.
   ```python
    while tries > 0
    ```
---
## Trello

> Move card  `As a player, I have a specific number of tries`   to the `Done`  list .
> 
----------

### Git


```
$ git add .
$ git commit -m "added a specific number of tries"
$ git push
```

----------


