This function should generates a random word each time you start playing the game:

Find the `catch-me-if-you-can/catch_me_if_you_can.py` file, and add the following:

    
    import random
    
    def get_random_word():
        file = open("wordlist.txt", "r")
        words = file.readlines() 
        random_word = random.choice(words)
        random_word = random_word.strip("\n")
        random_word = random_word.lower()
        file.close()
        return random_word
    
    random_word = get_random_word()
    
    
    def main():
    
    	print("\nThe word contains", len(random_word), 'letters. \n')
    	print(len(random_word) * " _")
    
    if __name__ == '__main__':
        main()

### Let me explain this code step by step:

**What `get_random_word()` do?** 

    def get_random_word():
        file = open("wordlist.txt", "r")
        words = file.readlines() 
        random_word = random.choice(words)
        random_word = random_word.strip("\n")
        random_word = random_word.lower()
        file.close()
        return random_word
  
  ***First:***

     file = open("wordlist.txt", "r")
     words = file.readlines() 

`open` will open the `wordlist.txt` file.
 `readlines` will read individual lines of `wordlist.txt` file.

`words` variable will contains the following:

    ['bed\n', 'wings\n', 'aliens\n', 'bowling\n', 'sleep\n', 'piano\n', 'commercial\n', 'dream\n', 'environment\n', 'magazine\n', 'cinema\n', 'bed\n', 'language']

***Second:***
    
    ---
    import random
    ---
    
    random_word = random.choice(words)
    random_word = random_word.strip("\n")
    random_word = random_word.lower()
    file.close()
    return random_word

 - The  `random`  module has a set of methods, such as `choice()`  method. You can use it to get a random element or number.
 
 - The  `choice()`  method returns a randomly selected element from the specified sequence. The sequence can be a string, a range, a list, a tuple or any other kind of sequence.
 - The `strip()` method removes any leading (spaces at the beginning) and trailing (spaces at the end) characters. In our case it is used to remove the new line between each word.

> `"\n"` in Python means a new line.
> 
 - The string `lower()` method converts all uppercase characters in a string into lowercase characters and returns it. So no matter how you write words in `wordlist.txt` file, `lower()` method will always return a lowercase characters. ***For example:*** if you wrote BED or bEd in `wordlist.txt` file, it will return bed. 
   
   
 - The `close()` method closes an open file.
 - The `return` keyword is to exit a function and return a value.

   
***Last:***

In the `main()` function:

    def main():
    
    	print("\nThe word contains", len(random_word), 'letters. \n')
    	print(len(random_word) * " _")


The `len()` function returns the number of characters in the string.

The first code to print the number of letters the word contains and the second to print this "_" character based on the number of letters in the string.

And we are done! DANCE TIME.

![dance party GIF](https://media3.giphy.com/media/zQLjk9d31jlMQ/200.webp?cid=ecf05e472c14286551df905fbe28db803386d8d62547a372&rid=200.webp)


***Final Full code:***

    import random
    import time
    
    
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
        messsages = ["Welcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
        for messsage in messsages:
            print (messsage)
            time.sleep(1.3)
    
    def main():
    
    	weclcome_message()
    	
    	print("\nThe word contains", len(random_word), 'letters. \n')
    	print(len(random_word) * " _")
    
    if __name__ == '__main__':
        main()

