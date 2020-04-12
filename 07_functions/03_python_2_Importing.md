<br>

Sometimes you need to use functions that are in other files or libraries. To use these functions we need to import them first.


```python
from <Library> import <FUNCTION>
```


***Example:***

 ```python
from math import pow
 
print(pow(2,2))
```

***Output:***
```
>>> 4
```
----
You can use [this](https://docs.python.org/3/library/index.html) as a reference to all the available libraries.

---
***Importing Rules:***

 - Imports are always put at the top of the file.

- Imports should usually be on separate lines:
       
   **Yes:**

   ```python
   import os 
   import sys
   ```


   **No:**

   ```python
   import sys, os
   ```

   
   **It's okay to say this though:**
  
    ```python
    from math import exp, log, pow
    ```

<br>
   
For more informations click [here](https://www.python.org/dev/peps/pep-0008/#imports).


