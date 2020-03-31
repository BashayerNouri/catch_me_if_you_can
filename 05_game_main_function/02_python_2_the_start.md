
Before explaining the functionality of the game, let me break down what we are going to do in some steps.

Look at this simple diagram first before going into the steps to understand more.

![flowchart](https://i.ibb.co/ryXT0sR/flowchart.png)

## Steps:

 - A `while` loop that ends if the player won or if the player didn't guess the correct word and runs out of tries.
 
 - Print the number of tries the player has.
 
 - Save the player's guess input.
 - If the player entered only **one letter**:

      1- If the letter is ***not an alphabet***, print "it is not a letter", print a list of all the guessed letters.
     
      2- If the letter ***already guessed***, print "letter already guessed", print a list of all the guessed letters.
     
      3- If the letter ***not part of the word***, print "not part of the word", add this letter to the guessed list, minimize the number of tries by one, print a list of all the guessed letters.
     
      4- if the letter is ***part of the word***, print "part of the word",  print a list of all the guessed letters, add this letter to the guessed list.
      
 - If the player entered a **full word** and it is length is equal to the length of the random word:
     -  If the word is correct, print "a win message"
     - if the word is not correct, print "Something is not part of the word", minimize the number of tries by one.

 - If the player entered a **full word** and it is length is not equal to the length of the random word:
     - Print "length does not equal to the word letters"


