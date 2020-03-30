

Now, how we can do our `weclome message` function? think about it

This function should print the following message with **1.3 scounds delay** between each message:

    Welcome to Catch Me If You Can
    Get ready
    Starting the game...
    Selecting a word...
    
![think winnie the pooh GIF](https://media1.giphy.com/media/mRh4cLIYhrs9G/giphy.gif?cid=ecf05e477ebb61a6d20c10df7197015310f6adea5c26691d&rid=giphy.gif)

Are you ready? Let's start.

Find the `catch-me-if-you-can/catch_me_if_you_can.py` file, and add the following:

    import time
    
    def weclcome_message():
        messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
        for messsage in messsages:
            print (messsage)
            time.sleep(1.3)
    
    def main():
         weclcome_message()
    
    if __name__ == '__main__':
        main()



### Let me explain this code step by step:

`weclcome_message` function:

    def weclcome_message():
        messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
        for messsage in messsages:
            print (messsage)
            time.sleep(1.3)

`Variables` are a place to save any type of data.

 `Lists` are another datatype just like `strings` or `integers`. Just as the name suggests, a list is a list of elements.

`messsages` is a variable of a `List` datatype.

    messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]

**Other Types of variables:**
`String`  : "I am a string"
`Integer`  : 2
`Float`  : 3.7
`Boolean`  : True or False

`"\n"` in Python means a new line and it is used inside a string. This is optional in our case to add space above our first message.
    
You can write what ever messages you like.

-----
**Now, how to access the `messages` list and print it one by on?**

The `for` loop in Python is used to iterate over a sequence ([list](https://www.programiz.com/python-programming/list "Python list"), [tuple](https://www.programiz.com/python-programming/tuple "Python tuple"), [string](https://www.programiz.com/python-programming/string "Python string")) or other iterable objects.

Loop continues until we reach the last item in the sequence. 

    messsages = ["Welcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
    for messsage in messsages:
        print (messsage)


The `for` loop goes through each element in the `messsages` list, saves it in the variable `messsage` (this variable could be named anything) and then execute the code inside the `for` loop.


This will print the messages immediately, but wait... we don't want that, we want to print our messages with a delay.

So think, what did we explain in the previous section to suspends execution?

![think winnie the pooh GIF](https://media1.giphy.com/media/mRh4cLIYhrs9G/giphy.gif?cid=ecf05e477ebb61a6d20c10df7197015310f6adea5c26691d&rid=giphy.gif)

Did I hear `sleep()`  function yes? no? 
I can't hear you but yes we will use `sleep()`  function.

So first we need to import  the python module `time` like this:

    import time
    
And than add `time.sleep(1.3)` for a 1.3 delay.

You can play around with this.

    import time
    
        def weclcome_message():
            messsages = ["\nWelcome to Catch Me If You Can","Get ready","Starting the game...","Selecting a word..."]
            for messsage in messsages:
                print (messsage)
                time.sleep(1.3)

Our last step is that we need to call the `welcome message` function.

In `main()` function we will write this:

    def main():
         weclcome_message()

And thats it we are done!!! Happy Dance.

![dance party GIF](https://media3.giphy.com/media/zQLjk9d31jlMQ/200.webp?cid=ecf05e472c14286551df905fbe28db803386d8d62547a372&rid=200.webp)

