# Daily Diary

# DAY 1

I am Jashanpreet kaur from department of Computer Science Engineering.Today is my first day of training as a student of third year. On the first day of the training, we learned about Python basics such as variables and data types.

** 1. Variables: Pointers to Memory **
In many programming languages (like C or Java), a variable is seen as a **labeled box** that holds a value. 
In Python, however, a variable is a **nametag (reference)** attached to an **object** in memory.

When we write:
```python
x = 42
```
Python does three things:
1. Makes the number object:
Python first creates an object in memory that holds the value 42. Think of it like writing “42” on a sticky note and putting it somewhere in memory.

2. Creates the name (variable): 
Then it creates the name x. This is just a label, like writing “x” on another sticky note.

3. Links the name to the object: 
Finally, Python sticks the “x” label onto the sticky note that already has “42”. Now whenever you say x, Python looks at the label and finds the object 42.

We can also inspect the memory address using the `id()` function, and check the type of the object using `type()`.

Example - Creating variables and inspecting their identities
```
x = 43
print(x)
print("x")
print(f"x is a variable: {x}")
print(f"Value of x: {x}")
print(f"Data Type of x: {type(x)}")
print("Data Type of x: {type(x)}")
print(f"Memory address of x (id): {id(x)}")
```

Output :
```
43
x
x is a variable: 43
Value of x: 43
Data Type of x: <class 'int'>
Data Type of x: {type(x)}
Memory address of x (id): 140726367440632
```






