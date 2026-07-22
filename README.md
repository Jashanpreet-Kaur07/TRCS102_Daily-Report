# Daily Diary

# DAY 1

I am Jashanpreet kaur from department of Computer Science Engineering.Today is my first day of training as a student of third year. On the first day of the training, we learned about Python basics such as variables and data types.

## Variables: Pointers to Memory
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

## Dynamic Typing

Dynamic typing means that variables don’t have fixed types. Their type is determined at runtime based on the value assigned.

Example:
x = 42
print(type(x))   # Output: <class 'int'>

x = "Hello"
print(type(x))   # Output: <class 'str'>

## Built-in Datatypes
 **1. Numeric Types** 

| Type     | Description                          | Example   |
|----------|--------------------------------------|-----------|
| `int`    | Whole numbers (positive/negative)    | `42`, `-7` |
| `float`  | Decimal numbers, scientific notation | `3.14`, `1.5e3` |
| `complex`| Numbers with real + imaginary parts  | `2+3j` |

**Key Notes**
- `int` → Unlimited size in Python.  
- `float` → Supports decimals and scientific notation.  
- `complex` → Access real part with `.real` and imaginary part with `.imag`.  

**2. String Type**

| Type   | Description                  | Example             |
|--------|------------------------------|---------------------|
| `str`  | Sequence of Unicode characters | `"Hello"`, `'Python'` |

**Key Notes**
- Strings are **immutable** (cannot be changed after creation).  
- Can be defined using single quotes `'...'`, double quotes `"..."`, or triple quotes `'''...'''` for multi-line text.  
- Support indexing and slicing:  
  ```python
  text = "Python"
  print(text[0])    # P
  print(text[1:4])  # yth

**3. Boolean & None Types** 

| Type      | Description                  | Example   |
|-----------|------------------------------|-----------|
| `bool`    | Logical values (True/False)  | `True`, `False` |
| `NoneType`| Represents "no value" or null| `None` |

**Key Notes**
- **Boolean (`bool`)**
  - Used in conditional statements and logical operations.
  - Result of comparisons:  
    ```python
    print(5 > 3)   # True
    print(2 == 4)  # False
    ```
  - Can be combined with logical operators: `and`, `or`, `not`.

- **None (`NoneType`)**
  - Special constant representing the absence of a value.
  - Often used as a default return value or placeholder.
  - Example:  
    ```python
    def greet():
        print("Hello")
        # No return → returns None by default

    result = greet()
    print(result)  # None
    ```

## Mutability vs. Immutability

- **Mutable types** → Can change after creation.  
  Examples: `list`, `dict`, `set`
  ```
  nums = [1, 2, 3]
  nums.append(4)   # [1, 2, 3, 4]
  ```

- **Immutable types** → Cannot change once created. Any update makes a new object.
Examples: `int`, `float`, `str`, `tuple`, `frozenset`, `bool`, `NoneType`
```
text = "hello"
new_text = text.upper()
# text stays "hello", new_text is "HELLO"
```

## Type Casting (Data Type Conversion)

Type casting means converting one data type into another.

### Built-in Functions
- `int()` → converts to integer  
- `float()` → converts to float  
- `str()` → converts to string  
- `bool()` → converts to boolean  
- `complex()` → converts to complex number  

**Examples**
```
x = "42"
print(int(x))    # 42 (string → int)

y = 3
print(float(y))  # 3.0 (int → float)

z = 0
print(bool(z))   # False (int → bool)

num = 5
print(str(num))  # "5" (int → string)
```

## Operators 

Python provides different types of operators to perform operations on values and variables.

**1. Arithmetic Operators**
Used for mathematical calculations.  
Examples: `+`, `-`, `*`, `/`, `%`, `**` (power), `//` (floor division)

**2. Comparison Operators**
Used to compare values, return `True` or `False`.  
Examples: `==`, `!=`, `>`, `<`, `>=`, `<=`

**3. Logical Operators**
Used to combine conditional statements.  
Examples: `and`, `or`, `not`

**4. Assignment Operators**
Used to assign values to variables.  
Examples: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `**=`, `//=`


**5. Bitwise Operators**
Used to perform operations on binary numbers.  
Examples: `&` (AND), `|` (OR), `^` (XOR), `~` (NOT), `<<` (left shift), `>>` (right shift)



# DAY - 2
Rest of the Operators are listed below:

**6. Membership Operators**
- **`in`** → Returns `True` if a value exists in a sequence (list, tuple, string, etc.).
- **`not in`** → Returns `True` if a value does not exist in a sequence.

**7. Identity Operators**
- **`is`** → Returns `True` if two variables point to the same object in memory.
- **`is not`** → Returns `True` if two variables point to different objects.

## Loops 

### Types of Loops
- **`for` loop** → Iterates over a sequence (list, tuple, string, etc.).  
- **`while` loop** → Runs as long as a condition is `True`.

### Loop Control
- **`break`** → Exit the loop early.  
- **`continue`** → Skip to the next iteration.  
- **`pass`** → Do nothing (placeholder).



# DAY - 3

## Functions and Modular Programming
**1. Built-in Functions**

- **`len()`** → Returns the length of a sequence (list, string, etc.).  
- **`sum()`** → Returns the sum of all elements in an iterable.  
- **`max()` / `min()`** → Returns the largest or smallest element.  
- **`abs()`** → Returns the absolute value of a number.  
- **`round()`** → Rounds a number to given decimals.  
- **`print()`** → Displays output to the console.

**2. Creating:**
i) Defining & Calling a simple function.
ii) Parameters & Arguments
  * 
