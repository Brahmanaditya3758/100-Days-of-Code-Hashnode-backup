---
title: "(Day 10) Task : Functions with Output and Calculator Project :-"
datePublished: Tue May 13 2025 02:49:00 GMT+0000 (Coordinated Universal Time)
cuid: cmalwxn3w000908jvgtq35nzg
slug: day-10-task-functions-with-output-and-calculator-project
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1747104471673/9d9045f8-c1d8-4dcf-a0ee-64998cba2eed.jpeg
tags: functions, python, python3, calculator, angela-yu, docstring-in-python

---

We've seen functions with only an execution body, functions with inputs that allow for variation in execution of the function body and now we'll see the final form of functions. Functions that can have outputs.

### ***TODO 1 :***

**Create a function called format\_name() that takes two inputs: f\_name and \`l\_name'.**

```python
def format_name(fname, I_name):
    print(fname)
    print(I_name)
format_name("adItya" , "ShaRma")      #Output :adItya ShaRma
```

### ***TODO 2 :***

**Use the title() function to modify the f\_name and l\_name parameters into Title Case.**

In Python, the term "title" refers to a string method that converts the first character of each word in a string to uppercase and the remaining characters to lowercase. This is often referred to as "title case." Non-alphanumeric characters are ignored.

```python
def format_name(f_name,l_name):
    print(f_name.title())
    print(l_name.title())

format_name("adItya rAm" , "ShaRma")    #Output : Aditya Ram Sharma
```

### ***Print (Display) vs. Output (Return) :-***

The return statement is used to give back a value from a function, which can be used later vs the print statement is used to display a value to the console only for the programmer to see.

### `return`: Sending Data Back to the Caller

The `return` statement is used within a function to send the result of the function's computation back to the caller. This returned value can then be stored, manipulated, or used in further computations.

```python
def add(a, b):
    return a + b

result = add(3, 4)
print(result)  # Outputs: 7
```

### `print`: Displaying Information to the Console

The `print` function outputs information to the console. It's primarily used for displaying messages or debugging purposes. Unlike `return`, `print` does not send data back to the caller; it merely displays it.

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Outputs: Hello, Alice!
```

### Syntax :-

***You can create a function with a body, input and output like this:***

```python
def function_name(input_parameter):
    <body of function that uses input_argument>
    return output

Function_name()
```

### ***Multiple Return Value :-***

Functions terminate at the return keyword. If you write code below the return statement that code will not be executed. However, you can have multiple return statements in one function. So how does that work?

### *Conditional Returns :*

Conditional Returns allow a function to return different values or take different execution paths based on conditional checks.

When we have control flow, as in the code will behave differently (go down different execution paths) depending on certain conditional checks, we can end up with multiple endings (returns).

```python
def canBuyAlcohol(age):
    if age >= 18:
        return True
    else:
        return False
```

### *Empty Returns :*

An Empty Return is a return statement without any value, used to exit a function without returning anything. You can also write return without anything afterwards, and this just tells the function to exit.

```python
def canBuyAlcohol(age):
    if type(age) != int: #If the data type of the age input is not a int, then exit.
        return
    if age >= 18:
        return True
    else:
        return False
```

### ***Docstrings :-***

You can use docstrings to write multiline comments that document your code. Just enclose your text inside a pair of three double quotes.

**Documenting Functions :**

it involves using docstrings just below a function definition to describe its purpose , which can be displayed when hover the function call.A neat feature of docstrings is you can use it just below the definition of a function and that text will be displayed when you hover over a function call. It's a good way to remind yourself what a self-created function does.

```python
def my_function(num):
    """Multiplies a number by itself."""
    return num * num

my_function
```

## ***Calculator Project :-***

The goal is to build a calculator program. <mark>Demo </mark> [https://appbrewery.github.io/python-day10-demo/](https://appbrewery.github.io/python-day10-demo/)

1. **Import art :-**
    
    ```python
    import art
    ```
    
2. **Write out 4 functions - addition, subtract, multiply and divide :-**
    
    ```python
    def add(n1, n2):
        return n1 + n2
    #TODO: Write out the other 3 functions - subtract, multiply and divide.
    def multiply(n1 , n2):
        return n1 * n2
    
    def divide(n1 , n2):
        return n1/n2
    
    def subtract(n1 , n2):
        return n1 - n2
    ```
    
3. **Add these 4 functions into a dictionary as the values. Keys = "+", "-", "\*", "/" :-**
    
    ```python
    operations = {"+": add , "*" : multiply , "/" : divide , "-" : subtract}
    ```
    
    ### ***Other Functionalities :-***
    
4. **Function Definition and Logo Display :**
    
    ```python
    def calculator():
        print(art.logo)
    ```
    
    * Defines the `calculator` function.
        
    * Displays a logo or banner from the `art` module.
        
5. **Initialization :**
    
    ```python
    should_accumulate = True
        num1 = float(input("What is the first number: "))
    ```
    
    * Sets a flag `should_accumulate` to control the loop for continuous calculations.
        
    * Prompts the user to input the first number and converts it to a float.
        
6. **Main Calculation Loop :**
    
    ```python
    while should_accumulate:
            for symbol in operations:
                print(symbol)
    ```
    
    * Enters a loop that continues as long as `should_accumulate` is `True`.
        
    * Iterates over the keys in the `operations` dictionary (e.g., '+', '-', '\*', '/') and prints them.
        
7. **User Input for Operation and Second Number :**
    
    ```python
    operational_symbol = input("Pick an operator: ")
    num2 = float(input("What is your next number: "))
    ```
    
    * Prompts the user to select an operator.
        
    * Prompts the user to input the next number and converts it to a float.
        
8. **Perform Calculation :**
    
    ```python
    answer = operations[operational_symbol](num1, num2)
    ```
    
    * Retrieves the function corresponding to the selected operator from the `operations` dictionary and applies it to `num1` and `num2`.
        
9. **Display Result :**
    
    ```python
    print(f"{num1} {operational_symbol} {num2} = {answer}")
    ```
    
    * Displays the calculation and result in a formatted string.
        
10. **Prompt for Continuation :**
    
    ```python
    choice = input(f"Type 'y' to continue calculating with {answer}, or type 'n' to start a new calculation: ")
    ```
    
    * Asks the user whether to continue with the current result or start anew.
        
11. **Handle User Choice**
    
    ```python
    if choice == "y":
        num1 = answer
    else:
        should_accumulate = False
        print("\n" * 20)
        calculator()
    ```
    
    * If the user chooses to continue, `num1` is updated to the current `answer`.
        
    * If not, sets `should_accumulate` to `False`, prints multiple newlines to clear the screen, and recursively calls `calculator()` to start over.
        
12. **Initial Function Call :**
    
    ```python
    calculator()
    ```
    
    * Initiates the calculator by calling the function.
        

## ***Code :-***

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1747104113918/62f5eb35-2070-4c3c-bd9b-29f6225f3d29.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1747104130270/bf1e4849-997e-4f72-b308-e1387e3cd52e.png align="center")