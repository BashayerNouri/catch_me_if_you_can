
 The `sleep()` function suspends (waits) execution of the current thread for a given number of seconds.

Python has a module named  [time](https://www.programiz.com/python-programming/time "Python time Module")  which provides several useful functions to handle time-related tasks. One of the popular functions among them is  `sleep()`.

The  `sleep()`  function suspends execution of the current thread for a given number of seconds.


## Example:

```
import time

print("Printed immediately.")
time.sleep(2.4)
print("Printed after 2.4 seconds.")
```

Here's how this program works:

-   `"Printed immediately"`  is printed
-   Suspends (Delays) execution for 2.4 seconds.
-   `"Printed after 2.4 seconds"`  is printed.

As you can see from the above example,  `sleep()`  can takes a floating-point number as an argument.


