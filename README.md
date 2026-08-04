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
  - Parameters - The variable listed in the function definition.
    Ex.- username
  - Arguments - The actual value sent to the function when it is called.
    Ex.- "Aman"

iii) Return function.

**Q:** Write your ATM Simulator.
```
#ATM simulator
balance=10000                                
while True:
    print("Welcome to ATM simulator")
    print("Choose an option:")
    print("1.Check your balance")
    print("2.Deposit money")
    print("3.Withdraw money")
    print("4.Exit")
    choice=int(input("Enter your choice:"))
    if choice==1:
        print("Balance = ",balance)
        break
    elif choice==2:
        amt=int(input("Enter your amount to deposit:"))
        balance+=amt
        print("Balance after deposit:",balance)
        break
    elif choice==3:
        amt=int(input("Enter your amount to withdraw:"))
        balance-=amt
        print("Balance after withdraw:",balance)
        break
    elif choice==4:
        print("Exit...")
        break
    else:
        print("Invalid option.")
        break
```
Output:
```
Welcome to ATM simulator
Choose an option:
1.Check your balance
2.Deposit money
3.Withdraw money
4.Exit
Enter your choice:1
Balance =  10000
```

**Q:** Checking for Prime Numbers.

```
#Prime Numbers
n=2
def is_prime(n):
    for i in range(2,int(n**0.5)+1):
        if n%1==0:
            print("Not Prime")
            break
    else:
        print("Prime")

is_prime(n)
```
Output:
```
Prime
```



# DAY - 4

### Types of Arguments 

- **Positional Arguments** → Values passed in order, matched by position.  
- **Default Arguments** → Parameters with default values if not provided.  
- **Keyword Arguments** → Values passed by explicitly naming the parameter.  

### Variable-Length Arguments 

- **`*args`** → Allows passing multiple positional arguments as a tuple.  
- **`**kwargs`** → Allows passing multiple keyword arguments as a dictionary.  

**Example**
```
def demo(*args, **kwargs):
    print(args)          # (1, 2, 3)
    print(kwargs)        # {'a': 10, 'b': 20}

demo(1, 2, 3, a=10, b=20)
```

### Variable Scope 

- **Local Variable** → Declared inside a function, accessible only within that function.  
- **Global Variable** → Declared outside all functions, accessible throughout the program.  

**Example**
```
x = 10      # Global

def demo():
    y = 5   # Local
    print(y)

demo()
print(x)
```

### Recursive Functions 

- **Definition** → A function that calls itself to solve a problem.  
- **Use Case** → Breaking problems into smaller sub-problems (e.g., factorial, Fibonacci).  
- **Base Case** → Stops recursion to avoid infinite loop.  

**Example**
```
def factorial(n):
    if n == 0:         # base case
        return 1
    else:
        return n * factorial(n-1)

print(factorial(5))   # 120
```

**Q:** Fibonacci Series.
```
def fib(n):
    if n <= 1:
        return n
    return fib(n-1) + fib(n-2)

print([fib(i) for i in range(7)])
```
Output:
```
[0, 1, 1, 2, 3, 5, 8]
```

### Data Structures 

- **List** → Ordered, mutable collection. Allows duplicates.  
  Example: `[1, 2, 3]`



# DAY - 5

- **Tuples** → Ordered, immutable collection. Allows duplicates.(Unpacking)
  Example: `(1, 2, 3)`

**example of unpacking and splitting**
 ```
d_splits=(([1,2,3],[4,5,6]),     # train: (x,y)
    ([1,2],[7,8]),               # val: (x,y)
    ([1],[0]))                   # test: (x,y)
train,val,test=d_splits
x_train,y_train=train
print(len(x_train))
```
Output:
```
3
```
- **Dictionary** → Key‑value pairs, unordered, mutable. Keys must be unique.  
  Example: `{"name": "Alice", "age": 20}`

- **Set** → Unordered collection of unique elements and it is mutable.  
  Example: `{1, 2, 3}`

**Q:** Intersection & Difference
```
# intersection
print("Intersection:",train_classes & val_classes)
print(train_classes.intersection(val_classes))

# difference
print("Difference:",train_classes - val_classes)
print(train_classes.difference(val_classes))
```
Output:
```
Intersection: {'dog'}
{'dog'}
Difference: {'bird', 'cat'}
{'bird', 'cat'}
```

**Q:** Temperature Filter Set
```
temp=[28,32,18,15,30,22,17]
cold_days=[]
hot_days=[]
for i in temp:
    if i<20:
        cold_days.append(i)
    else:
        hot_days.append(i)
print(cold_days)
print(hot_days)
```
Output:
```
[18, 15, 17]
[28, 32, 30, 22]
```



# DAY - 6

### NumPy Fundamentals (Array Creation)

- **`np.zeros(shape)`** → Creates an array filled with 0's.  
- **`np.ones(shape)`** → Creates an array filled with 1's.  
- **`np.arange(start,stop,step)`** → It does not include stop value. 
- **`np.linspace(start,stop,num)`** → It includes stop value.(num-how many values you want to generate).
- **`np.eye(shape)`** → Creates an identity matrix of the given shape.

### NumPy Array Attributes

- **`.ndim`** → Number of dimensions (axes).  
- **`.shape`** → Tuple showing size of each dimension.  
- **`.size`** → Total number of elements.  
- **`.dtype`** → Data type of elements.  
- **`.itemsize`** → Size (in bytes) of each element.  
- **`.nbytes`** → Total bytes consumed by elements.  

**Example**
```
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6]])

print(arr.ndim)    # 2
print(arr.shape)   # (2, 3)
print(arr.size)    # 6
print(arr.dtype)   # int64 (depends on system)
```

### Indexing in Array
```
arr=np.array([1,2,3,4])
arr[-2]=500
print(arr)               
print(arr[0])
print(arr[2])
```
Output:
```
[  1   2 500   4]
1
500
```

### Boolean Indexing
```
data=np.array([5,12,3,6,8,90,20])
print(data>12)          # prints 'true' on value >12
data[data>12]           # prints index of elements greater than 12
hot_days=data[data>12]  # prints the same o/p in hot and cold days ex
data[data<12]=12        # it makes the ele <12 = to 12
print(data)
```
Output:
```
[False False False False False  True  True]
[12 12 12 12 12 90 20]
```

### Boolean Masking & np.where
```
salaries=np.array([23000,-45000,50000,-82000,30000])
fixed=np.where(salaries<0,10000,salaries)
print(fixed)
```
Output:
```
[23000 10000 50000 10000 30000]
```

### Mean & Median 
```
x=np.array([10,30,20,40,10])
print(np.mean(x))
print(np.median(x))
print(np.std(x))
```
Output:
```
22.0
20.0
11.661903789690601
```

### Mean & Median of 2D Array
```
x=np.array([
    [10.0,200.0],
    [30.0,100.0],
    [20.0,400.0]
])
col_means=np.mean(x,axis=0)
row_means=np.mean(x,axis=1)
print("Column wise mean:",col_means)
print("Row wise mean:",row_means)
```
Output:
```
Column wise mean: [ 20.         233.33333333]
Row wise mean: [105.  65. 210.]
```

### Reshaping 
Reshaping means moving from 1d to 2d array.
```
flat_array=np.arange(6)
print("Original 1D array:",flat_array)
matrix_2d=flat_arr.reshape(2,3)
print(matrix_2d)
```
Output:
```
Original 1D array: [0 1 2 3 4 5]
[[0 1 2]
 [3 4 5]]
```

### Flatten the 2D Array back to 1D
```
flattened=matrix_2d.flatten()
print(flattened)
print("Flattened array back to 1d:",flattened)
```
Output:
```
[0 1 2 3 4 5]
Flattened array back to 1d: [0 1 2 3 4 5]
```

### Dot Product
```
inputs=np.array([1.0,2.0])
weights=np.array([
    [0.2,0.8,-0.5],
    [0.5,-0.1,0.4]
])
print(np.dot(inputs,weights))
```
Output:
```
[1.2 0.6 0.3]
```

### 1D Array & 2D Array

- **1D Array** → Single row/line of elements.  
  Example:

  ```
  import numpy as np
  arr1 = np.array([1, 2, 3, 4])
  print(arr1.ndim)       # 1
  print(arr1.shape)      # (4,)
  ```


- **2D Array** → Matrix with rows and columns.
Example:

```
arr2 = np.array([[1, 2, 3], [4, 5, 6]])
print(arr2.ndim)        # 2
print(arr2.shape)       # (2, 3)
```



# DAY - 7

### Pandas
There are two types of data structure:

* Series
* Data Frames (data in table format) - It is used to make CSV file.

### Mean & Median in Pandas

- **`mean()`** → Returns the average of values in a Series/DataFrame.  
- **`median()`** → Returns the middle value of values in a Series/DataFrame.  

Example (Series):
```
import pandas as pd
data = pd.Series([10, 20, 30, 40, 50])
print(data.mean())    # 30.0
print(data.median())  # 30.0
```

Example (DataFrame):
```
df = pd.DataFrame({
    "A": [1, 2, 3],
    "B": [4, 5, 6]
})

print(df.mean())       # Column-wise mean
print(df.median())     # Column-wise median
```



# DAY - 8

### Data Visualization

- **Matplotlib** → Low-level plotting library.  
  - `plt.plot()` → Line plots  
  - `plt.bar()` → Bar charts  
  - `plt.hist()` → Histograms  
  - `plt.scatter()` → Scatter plots  

- **Seaborn** → High-level interface built on Matplotlib.  
  - `sns.histplot()` → Histogram with KDE  
  - `sns.boxplot()` → Box plots  
  - `sns.heatmap()` → Correlation heatmaps  
  - `sns.scatterplot()` → Scatter plots with style  

- **Pandas Integration** → Quick plots from DataFrames.  
  - `df.plot(kind="line")`  
  - `df.plot(kind="bar")`  
  - `df.plot(kind="hist")`  

**Example**
```
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd

df = pd.DataFrame({"A":[1,2,3,4], "B":[4,3,2,1]})

# Line plot with Matplotlib
plt.plot(df["A"], df["B"])
plt.title("Line Plot")
plt.show()

# Scatter plot with Seaborn
sns.scatterplot(x="A", y="B", data=df)
plt.show()
```



# DAY - 9

### Countplot in Seaborn
A bar plot showing the count of observations in each category.  
- **Function** → `sns.countplot()`  

**Example**
```
import seaborn as sns
import matplotlib.pyplot as plt

data = ["A", "B", "A", "C", "B", "A"]

sns.countplot(x=data)
plt.title("Count of Categories")
plt.show()
```

### Exploratory Data Analysis (EDA)
 Process of analyzing datasets to summarize main characteristics.  
- **Goal** → Understand data distribution, detect patterns, spot anomalies, and prepare for modeling.  

**Common Steps**
- **Data Inspection** → `df.head()`, `df.info()`, `df.describe()`  
- **Missing Values** → `df.isnull().sum()`  
- **Data Types** → `df.dtypes`  
- **Summary Stats** → Mean, Median, Mode, Std, Var  
- **Correlation** → `df.corr()`  
- **Visualization** → Histograms, Boxplots, Countplots, Heatmaps  

**Example**
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv("data.csv")

print(df.head())        # first rows
print(df.describe())    # summary stats
print(df.isnull().sum())# missing values

sns.heatmap(df.corr(), annot=True)
plt.show()
```



# DAY - 10

### Interquartile Range (IQR)
 Measure of statistical spread, difference between 75th percentile (Q3) and 25th percentile (Q1).  
- **Formula** → `IQR = Q3 - Q1`  
- **Use** → Detecting outliers and understanding data variability.  

**Example**
```
import pandas as pd

data = pd.Series([7, 8, 5, 6, 3, 4, 9, 12, 15])

Q1 = data.quantile(0.25)
Q3 = data.quantile(0.75)
IQR = Q3 - Q1

print("Q1:", Q1)   # 5.0
print("Q3:", Q3)   # 9.0
print("IQR:", IQR) # 4.0
```



# DAY - 11

### Linear Regression 
 A statistical method to model the relationship between a dependent variable (y) and one/more independent variables (x).  
- **Goal** → Find the best‑fit line that minimizes error.  
- **Library** → `sklearn.linear_model.LinearRegression`

**Example**
```
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

# Sample dataset
df = pd.DataFrame({
    "Size": [1000, 1500, 2000, 2500],
    "Price": [200000, 250000, 300000, 350000]
})

X = df[["Size"]]   # independent variable
y = df["Price"]    # dependent variable

# Train/test split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Train model
model = LinearRegression()
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)
print("Predicted:", y_pred)
```

### Multiple Linear Regression 
 A statistical method to model the relationship between one dependent variable (y) and multiple independent variables (x1, x2, …).  
- **Goal** → Find the best‑fit plane/hyperplane that minimizes error.  
- **Library** → `sklearn.linear_model.LinearRegression`

**Example**
```
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

# Sample dataset
df = pd.DataFrame({
    "Size": [1000, 1500, 2000, 2500],
    "Rooms": [2, 3, 3, 4],
    "Price": [200000, 250000, 300000, 350000]
})

X = df[["Size", "Rooms"]]  # independent variables
y = df["Price"]            # dependent variable

# Train/test split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Train model
model = LinearRegression()
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)
print("Predicted:", y_pred)

# Coefficients & intercept
print("Coefficients:", model.coef_)
print("Intercept:", model.intercept_)
```

### Polynomial Regression 
 A regression technique where the relationship between independent (x) and dependent (y) variables is modeled as an nth‑degree polynomial.  
- **Goal** → Capture non‑linear patterns in data.  
- **Library** → `sklearn.preprocessing.PolynomialFeatures` + `LinearRegression`

**Example**
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import PolynomialFeatures

# Sample dataset
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
y = np.array([1, 4, 9, 16, 25])  # quadratic relation

# Transform features into polynomial (degree=2)
poly = PolynomialFeatures(degree=2)
X_poly = poly.fit_transform(X)

# Train model
model = LinearRegression()
model.fit(X_poly, y)

# Prediction
y_pred = model.predict(X_poly)

# Plot
plt.scatter(X, y, color="blue")
plt.plot(X, y_pred, color="red")
plt.title("Polynomial Regression (degree=2)")
plt.show()
```



# DAY - 12

### Ridge & Lasso Regression 

- **Ridge Regression** → Linear regression with L2 regularization (penalizes large coefficients).  
- **Lasso Regression** → Linear regression with L1 regularization (can shrink some coefficients to 0 → feature selection).  
- **Goal** → Prevent overfitting, improve generalization.  
- **Library** → `sklearn.linear_model.Ridge`, `sklearn.linear_model.Lasso`

**Example**
```
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import Ridge, Lasso

# Sample dataset
df = pd.DataFrame({
    "Size": [1000, 1500, 2000, 2500],
    "Rooms": [2, 3, 3, 4],
    "Price": [200000, 250000, 300000, 350000]
})

X = df[["Size", "Rooms"]]
y = df["Price"]

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Ridge Regression
ridge = Ridge(alpha=1.0)
ridge.fit(X_train, y_train)
print("Ridge Coefficients:", ridge.coef_)

# Lasso Regression
lasso = Lasso(alpha=0.1)
lasso.fit(X_train, y_train)
print("Lasso Coefficients:", lasso.coef_)
```

### Logistic Regression 
 A classification algorithm that models the probability of a binary outcome (0/1, True/False).  
- **Goal** → Estimate probability using the logistic (sigmoid) function.  
- **Library** → `sklearn.linear_model.LogisticRegression`

**Example**
```
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

# Sample dataset
df = pd.DataFrame({
    "Hours_Studied": [2, 4, 6, 8, 10],
    "Passed": [0, 0, 1, 1, 1]  # binary outcome
})

X = df[["Hours_Studied"]]   # independent variable
y = df["Passed"]            # dependent variable (0/1)

# Train/test split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Train model
model = LogisticRegression()
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)
print("Predicted:", y_pred)

# Probability estimates
print("Probabilities:", model.predict_proba(X_test))
```



# DAY - 13

### Classification

**What is classification?**
A supervised learning technique used to predict categorical outcomes (labels).

**Types of Classification:**
* Binary Classification: The target variable has only two possible values.
Example: Email is spam(1) or not spam(0)
         Passenger Survived (1) or Did not Survived (0)

* Multiclass Classification: The target variable has three or more possible values.
Example: Predict weather (Sunny, Rainy, Cloudy, Snowy)
         Predict Passenger Class (1st class, 2nd class, 3rd class)
  
**Common Algorithms used:** 
  - Logistic Regression → Binary classification.  
  - Decision Trees → Rule-based splits.  
  - Random Forest → Ensemble of decision trees.  
  - K-Nearest Neighbors (KNN) → Classifies based on nearest data points.  
  - Support Vector Machine (SVM) → Finds optimal separating boundary.  
  - Naive Bayes → Probabilistic classifier based on Bayes’ theorem.  

**Example (Logistic Regression)**
```
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

# Sample dataset
df = pd.DataFrame({
    "Hours_Studied": [2, 4, 6, 8, 10],
    "Passed": [0, 0, 1, 1, 1]  # binary outcome
})

X = df[["Hours_Studied"]]
y = df["Passed"]

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

model = LogisticRegression()
model.fit(X_train, y_train)

print("Predicted:", model.predict(X_test))
```



# DAY - 14

### Clustering 
 An unsupervised learning technique that groups data points into clusters based on similarity.  
- **Goal** → Discover hidden patterns or natural groupings in data.  
- **Types of Clustering** →  
  - **K‑Means** → Partitions data into K clusters.  
  - **Hierarchical** → Builds nested clusters (tree/dendrogram).  
  - **DBSCAN** → Groups based on density, handles noise/outliers.  

**Example (K‑Means)**
```
import pandas as pd
from sklearn.cluster import KMeans

# Sample dataset
df = pd.DataFrame({
    "X": [1, 2, 3, 8, 9, 10],
    "Y": [1, 2, 3, 8, 9, 10]
})

# KMeans clustering
kmeans = KMeans(n_clusters=2, random_state=42)
df["Cluster"] = kmeans.fit_predict(df[["X", "Y"]])

print(df)
```






