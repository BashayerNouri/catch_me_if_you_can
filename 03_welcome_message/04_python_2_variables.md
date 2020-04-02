
Programming languages offer a method of storing data for reuse. If there is a greeting we want to present, a date we need to reuse, or a user ID we need to remember we can create a  _variable_  which can store a value. In Python, we  _assign_  variables by using the equals sign (`=`).

```python
# Greeting Message
message_string = "Hello, World!"
print(message_string)
```
***Output***
```
>>> Hello, World!
```

In the above example, we store the message “Hello, World!” in a variable called  `message_string`. Variables can’t have spaces or symbols in their names other than an underscore (`_`).

---

It’s no coincidence we call these creatures “variables”. If the context of a program changes, we can update a variable but perform the same logical process on it.

```python
# Greeting Message
message_string = "Hello, World!"
print(message_string)

# Farewell
message_string = "Hasta la vista"
print(message_string)
```
***Output***
```
Hello, World!
Hasta la vista
```

Above, we create the variable `message_string`, assign a welcome message, and print the greeting. After we greet the user, we want to wish them goodbye. We then update `message_string` to a departure message and `print` that out.

-----
### Some types of variables:

-   `String`  : "I am a string"
-   `Integer`  : 4
-   `Float`  : 9.11
-   `Boolean`  : True or False

***Example:***
```python
name = "Jigglypuff" # String Variable
weight = 50 # Integer Variable
height = 5.5 # Float Variable
is_cute = True # Boolean Variable

print(name)
print(height)
```
***Output:***
```
Jigglypuff
5.5
```
---
Also, you can use pre-existing variables to define new variables. 

***Example:***

```python
name = "Bashayer"
message = "Hello, " + name
print(message)
```

**Output:**

```
Hello, Bashayer
```

***Note:*** the `+` was used to concatenate the two strings.
