---
title: "(Day 05) Task : Python Loops & Password Generator Task :-"
datePublished: Sun Apr 20 2025 08:43:32 GMT+0000 (Coordinated Universal Time)
cuid: cm9pegzgj000509i302j9fo6g
slug: day-05-task-python-loops-and-password-generator-task
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1745138518570/a94dd064-b7cb-47d7-b509-fb9681d0c7f0.jpeg
tags: python, python3, 100daysofcode, for-loop, 100daysofpython, 100daysofprojects, dr-angela-yu

---

## ***Loops in Python :-***

### `For` ***Loop :-***

* A `for` loop is used to repeat a block of code for each item in a sequence (like a list, string, or range of numbers).
    

## ***Syntax of a*** `for` ***loop :-***

```python
for item in sequence:
    # do something with item
```

* `item`: A variable name you choose (like `fruit`, `number`, etc.)
    
* `sequence`: A list, string, range, etc.
    
* The code inside the loop **runs once for each item** in the sequence.
    

## ***Why use a*** `for` ***loop?***

* When you want to do something multiple times, especially for every item in a group.
    
* ***Example:***
    
    * Print every fruit in a basket, one by one.
        
    * ```python
        fruits = ["apple", "peach", "banana"]
        for fruit in fruits:
            # Process each fruit here
            print(fruit)
        ```
        
    * Here it’s assigning the values of fruits to a variable fruit.
        

## `for` ***loops and the*** `range()` ***Function:-***

* When you use `for` loops with the `range()` function, you're telling Python:
    
    “<mark>Hey, repeat this code a certain number of times.</mark>”
    

### ***What does*** `range()` ***do?***

* The `range()` function generates a sequence of numbers.
    
* ```python
    range(start, stop, step)
    ```
    
* `start`: The number to begin from (default is 0).
    
* `stop`: The number to stop before.
    
* `step`: How much to increment each time (default is 1).
    

## `range()` ***can be defined in three parts :-***

1. ### ***Use*** `for i in range(n)` ***to repeat code n times :-***
    

* Do something n times. It's a simple way to repeat a block of code again and again.
    
* `range(n)` creates a list of numbers from `0` to `n-1`
    
* ***Note :-*** Remember `range()` excludes the stop number.
    
    * **Example :-**
        
        * ```python
            for i in range(5):
                print(i)             # Output : 0, 1, 2, 3, 4
            ```
            
        * This prints numbers: `0, 1, 2, 3, 4`
            
        * Starts from 0 by default, ends before 5 (as it excludes the stop number).
            

2. ### ***Use*** `range(start, stop)` ***to control where it begins and ends :-***
    

* “<mark>Start counting from </mark> `start` <mark> and stop before </mark> `stop`".
    
    You're telling Python exactly where to begin and where to end the loop.
    
* `start` → the number where the loop **starts**
    
* `stop` → the number where the loop **ends (but not included)** ❌
    
* The loop runs from `start` to `stop - 1`.
    
    * **Example :-**
        
        * Print roll numbers from 1 to 30:
            
        * ```python
            for roll_no in range(1, 31):
                print(f"Roll Number: {roll_no}")
            ```
            

3. ### ***Use*** `range(start, stop, step)` ***for custom steps :-***
    
    “<mark>Start from </mark> `start`<mark>, stop before </mark> `stop`<mark>, and jump by </mark> `step` <mark> each time</mark>.”
    
    You're not just telling Python where to start and stop, but also how big each jump (step) should be.
    

* `start` → where the loop begins.
    
* `stop` → where it stops (but not included).
    
* `step` → how much to increase or decrease each time.
    
    * **Example :-**
        
        * ```python
            for i in range(2, 11, 2):
                print(i)            # Output :- 2 4 6 8 10 
            ```
            
* ## ***Note :-***
    
    * You can use positive steps (count up).
        
    * Or negative steps (count down).
        
    * If `step` is not given, it defaults to `1`.
        
    

## **Project :-** You are going to write a program that automatically prints the solution to the FizzBuzz game. These are the rules of the FizzBuzz game: Your program should print each number from 1 to 100 in turn and include number 100. But when the number is divisible by 3 then instead of printing the number it should print "Fizz". When the number is divisible by 5, then instead of printing the number it should print "Buzz". And if the number is divisible by both 3 and 5 e.g. 15 then instead of the number it should print "FizzBuzz"

```python
# FizzBuzz from 1 to 100

for number in range(1, 101):  # Includes 100
    if number % 3 == 0 and number % 5 == 0:
        print("FizzBuzz")  # Divisible by both 3 and 5
    elif number % 3 == 0:
        print("Fizz")      # Divisible by 3 only
    elif number % 5 == 0:
        print("Buzz")      # Divisible by 5 only
    else:
        print(number)      # Not divisible by 3 or 5
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1745138316720/744eb6af-d849-41de-bfde-b504ae85bbdd.png align="center")

## ***Password Generator :-***

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1745138403136/f4ab4800-2eb0-4ec5-b68d-52e302e461ef.png align="center")