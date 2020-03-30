Sometimes you need to use functions that are in other files or libraries. To use these functions we need to import them first.

    from <Library> import <FUNCTION>

***Example:***

    from math import pow
    
    print(pow(2,2))

***Output:***

> 4


---
***Importing Rules:***

 - Imports are always put at the top of the file.

- Imports should usually be on separate lines:
       
   **Yes:**

       import os
       import sys

   **No:**

       import sys, os
   
   **It's okay to say this though:**
  
      from math import exp, log, pow

  
   
For more informations click [here](https://www.python.org/dev/peps/pep-0008/#imports).

