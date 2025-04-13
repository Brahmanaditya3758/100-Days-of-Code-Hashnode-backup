---
title: "(Day 02) Task : Data Types & Tip Calculator Project :-"
datePublished: Sun Apr 13 2025 05:18:42 GMT+0000 (Coordinated Universal Time)
cuid: cm9f72lrv000308l59hxs1cji
slug: day-02-task-data-types-and-tip-calculator-project
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1744521226476/8cccbf62-5bf3-44cf-9cb5-cf9b1293bf4e.png
tags: python, udemy, day02, dr-angela-yu, python-data-types-string-manipulation-python-python-beginner-tutorial-python-for-beginners-learning-python-python-data-types-tutorial-python-type-conversion-python-type-checking-python-variables-python-input-function-python-code-examples-python-coding-exercises-python-programming-basics-python-mathematical-operations-python-string-operations-python-interactive-coding-exercises-python-bmi-calculator-python-tip-calculator-python-projects-for-beginners-python-100-days-of-code

---

## ***Topics Covered :-***

* **Primitive data types in Python:**
    
    * `int`**,** `float`**,** `str`**, and** `bool`.
        
* **Type Error & Type Checking with** `type()`.
    
* **Type conversion using** `str()`**,** `int()`**,** `float()`.
    
* **Arithmetic operations (**`+`**,** `-`**,** `*`**,** `/`**,** `//`**,** `%`**,** `**`**).**
    
* **Number rounding using** `round()`**, floor division** `//`.
    
* **F-strings for formatting output.**
    

## ***What are Data Types in Python?***

* In Python (and all programming languages), data types are categories of data that tell the interpreter what kind of value is being stored or used.
    
    Just like we organize different things in real life (books, numbers, names), Python organizes data into types.
    

## **Two Categories of Data Types :-**

### ***Primitive Data Types :-***

* These are the most basic types of data in Python — simple and not made up of other types.
    
* Primitive types are immutable, meaning once created, their value cannot be changed.
    

1. ### `int` – **Integer :**
    
    * Represents whole numbers (no decimal point).
        
        * Positive or negative.
            
            #### ✅ Example:
            
        * ```python
            int age = 25
            int bornyear = 1999
            ```
            
    
2. ### `float` – **Floating Point Number :**
    
    * Represents decimal numbers (numbers with a point).
        
        * Used for more precise values like measurements or money.
            
            #### ✅ Example:
            
        * ```python
            float price = 99.99
            float height = 5.8
            ```
            
    
3. ### `str` – **String :**
    
    * Represents text (a sequence of characters).
        
        * Written in quotes (`'single'` or `"double"`).
            
            #### ✅ Example:
            
        * ```python
            name = "Alice"
            greeting = 'Hello, world!'
            ```
            
    
4. ### `bool` – **Boolean :**
    
    * Represents True or False values.
        
        * Used in decision making (conditions, comparisons, etc.)
            
            #### ✅ Example:
            
        * ```python
            is_raining = True
            is_sunny = False
            ```
            
    

| **Type** | **Description** | **Example** |
| --- | --- | --- |
| `int` | integer | `10`, `-3`, `1000` |
| `float` | Decimal number | `3.14`, `-0.5` |
| `str` | String (text) | `"Hello"`, `'123'` |
| `bool` | Boolean (True/False) | `True`, `False` |

### ***Non-Primitive Data Types :-***

* They can store multiple values and are built using primitive types.
    
* These types help organize, group, or relate data together.
    

1. ### **List :**
    
    * A list is a collection of items that are ordered and changeable (mutable) contains \[\].
        
        * You can store different types of data in a list.
            
        * Think of it like a grocery list — you can add, remove, or change items.
            
            #### **✅ Example:**
            
        * ```python
            fruits = ["apple", "banana", "cherry"]
            print(fruits[0])   # Output: apple
            fruits.append("orange")  # Add item
            ```
            
    
2. ### **Tuple :**
    
    * A tuple is like a list, but it is unchangeable (immutable) and contains parenthesis.
        
        * Use it when you want to store a fixed set of items that shouldn’t be modified.
            
            **✅ Example:**
            
        * ```python
            fruits = ("apple", "banana", "cherry")
            print(fruits[0])   # Output: apple
            ```
            
    
3. ### **Set :**
    
    * A set is an unordered collection of unique items.
        
        * It automatically removes duplicates.
            
        * Great for storing things like tags, unique words, etc.
            
            **✅ Example:**
            
        * ```python
            numbers = {1, 2, 3, 3, 4}
            print(numbers)  # Output: {1, 2, 3, 4}
            numbers.add(5)  # Add new unique item
            ```
            
    
4. ### **Dictionary :**
    
    * A dictionary stores data in key-value pairs.
        
        * You use the key to access the value, just like looking up a word in a dictionary.
            
            **✅ Example:**
            
        * ```python
            student = {"name": "Alice", "age": 21 ,"grade": "A"} 
            print(student["name"])  # Output: Alice
            ```
            
    

| Type | Description | Example |
| --- | --- | --- |
| `list` | Ordered, mutable collection | `[1, 2, 3]`, `["a", "b"]` |
| `tuple` | Ordered, immutable collection | `(1, 2, 3)` |
| `set` | Unordered, unique items | `{1, 2, 3}` |
| `dict` | Key-value pairs | `{"name": "John", "age": 25}` |

## What is a TypeError in Python?

* These errors occur when you are using the wrong data type , such as passing an integer to a function that expects a string.
    
    **Example :**
    
    * `len(12345)` : This function will show a type error because you can only give the string to len() function , it will refuse to work and give you a TypeError if you give it a number (Integer).
        

### ***To Cure this Problem(error) :-***

**1\. (Type Checking) —&gt;** Check the data types using `type()`.

* You can check the data type of any value or variable in python using the type() function.
    
    * **✅ Example:** print(type("abc")).
        
        * #### ***Write out 4 type checks to print all 4 primitive data types :***
            
        * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744516561416/5b0c56b6-45f7-4715-a674-510e5b1a68c0.png align="center")
            

**2\. (Type Conversion) —&gt;** Change one data type to other data type.

* It refers to converting data into different data types using functions like float() , int() or str().
    
    * **Types of Type Conversion:**
        
        1. **Implicit Type Conversion (Python does it automatically) :-**
            
            Python automatically converts smaller data types to larger ones during operations.
            
            ```python
            a = 5       # int
            b = 2.0     # float
            result = a + b  # Python converts `a` to float
            print(result)      # 7.0
            print(type(result))  # <class 'float'>
            ```
            
        2. **Explicit Type Conversion (You do it manually):-**
            
            You intentionally change the data type using built-in functions.
            
            ```python
            num = "10"
            num_int = int(num)       # 10
            num_float = float(num)   # 10.0
            ```
            
    * ***Example :-***
        
        * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744517710728/991016a7-818f-4505-82f9-4004c13fad6e.png align="center")
            

## ***Mathematical (Arithmetic) Operators in Python :-***

* Python supports several arithmetic operators to perform basic math calculations. Here’s a breakdown of each:
    
* ### `+` Addition :
    
    Adds two numbers.
    
* ### `-` Subtraction :
    
    Subtracts the second number from the first.
    
* ### `*` Multiplication :
    
    Multiplies two numbers.
    
* ### `/` Division :
    
    Divides the first number by the second.  
    Always returns a float, even if the division is exact.
    
* ### `//` Floor Division :
    
    Divides and rounds down to the nearest whole number.
    
* ### `%` Modulus (Remainder) :
    
    Returns the remainder of division.
    
* ### `**` Exponentiation (Power) :
    
    Raises the first number to the power of the second.
    
    ```python
    x = 10 + 5
    print(x)  # Output: 15
    x = 10 - 3
    print(x)  # Output: 7
    x = 4 * 3
    print(x)  # Output: 12
    x = 10 / 2
    print(x)  # Output: 5.0
    x = 10 // 3
    print(x)  # Output: 3
    x = 10 % 3
    print(x)  # Output: 1
    x = 2 ** 3  # 2 raised to the power 3
    print(x)  # Output: 8
    ```
    

## ***Mathematical (Assignment) Operators in Python :-***

### 1\. `=` Basic Assignment :

* Assigns the value on the right to the variable on the left.
    
* ```python
    x = 10
    print(x)  # Output: 10
    ```
    

### 2\. `+=` Add and Assign :

* Adds a value to a variable and updates the variable with the new value.
    
* ```python
    x = 5
    x += 3     # same as x = x + 3
    print(x)   # Output: 8
    ```
    

---

### 3\. `-=` Subtract and Assign :

* Subtract value from variable and updates the variable with the new value.
    
* ```python
    x = 10
    x -= 4     # x = x - 4
    print(x)   # Output: 6
    ```
    

---

### 4\. `*=` Multiply and Assign :

* Multiply value to the variable and updates the variable with the new value.
    
* ```python
    pythonCopyEditx = 6
    x *= 2     # x = x * 2
    print(x)   # Output: 12
    ```
    

---

### 5\. `/=` Divide and Assign :

* Divide variable and updates the variable with the new value.
    
* Always results in a `float`.
    
* ```python
    x = 12
    x /= 3     # x = x / 3
    print(x)   # Output: 4.0
    ```
    

---

### 6\. `//=` Floor Division and Assign :

* Divides and rounds down to the nearest whole number.
    
* ```python
    pythonCopyEditx = 10
    x //= 3    # x = x // 3
    print(x)   # Output: 3
    ```
    

---

### 7\. `%=` Modulus and Assign :

* Gives the remainder after division.
    
* ```python
    pythonCopyEditx = 10
    x %= 3     # x = x % 3
    print(x)   # Output: 1
    ```
    

---

### 8\. `**=` Exponentiation and Assign :

* Raises the number to the power of another.
    
* ```python
    pythonCopyEditx = 2
    x **= 3    # x = x ** 3
    print(x)   # Output: 8
    ```
    

## ***Flooring a Number :-***

* We can floor a number or remove all decimal places using the int() function which converts a floating point number (with decimal places) into an integer (whole number).
    
* ```python
    int(3.738492) # Becomes 3
    ```
    

## ***Rounding a Number :-***

* If we want to round a decimal number to the nearest whole number using the traditional mathematical way, where anything over .5 rounds up and anything below rounds down. Then you can use the python `round()` function.
    
* ```python
    round(3.738492) # Becomes 4
    round(3.14159) # Becomes 3
    round(3.14159, 2) # Becomes 3.14
    ```
    

## ***f-Strings :-***

* In Python, we can use f-strings to insert a variable or an expression into a string.
    
* ```python
    age = 12
    print(f"I am {age} years old").  # Will output I am 12 years old.
    ```
    

## ***Project: Tip Calculator (Python) :-***

### **What It Does:**

* Calculates how much each person should pay when splitting a bill, including tip.
    
* We're going to build a tip calculator.
    
    **Ex :-**
    
    If the bill was $150.00, split between 5 people, with 12% tip.
    
    Each person should pay:
    
    (150.00 / 5) \* 1.12 = 33.6
    
    After formatting the result to 2 decimal places = 33.60
    

### **Sample Output :-**

```python
Welcome to the tip calculator!
What was the total bill? $150
How much tip would you like to give? 10, 12, or 15? 12
How many people to split the bill? 5
Each person should pay: $33.6
```

## **Project :-**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744520760684/3c30d004-aae0-4a89-9c14-dca9559d91f4.png align="center")