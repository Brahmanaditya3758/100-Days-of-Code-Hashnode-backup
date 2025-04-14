---
title: "(Day 03) Task : Treasure Island Project :-"
datePublished: Mon Apr 14 2025 13:19:30 GMT+0000 (Coordinated Universal Time)
cuid: cm9h3orl8000m09jo4rmpexgs
slug: day-03-task-treasure-island-project
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1744636312303/3acd3e0e-ac38-4ff6-aa41-1f91ae3e7469.jpeg
tags: python, 100daysofcode, python-beginner, 100daysofprojects, python-100-days-of-code, dr-angela-bootcamp

---

## ***What You’ll Learn :\_***

This project focuses on:​

* Using `if`, `elif`, and `else` statements​.
    
* Nesting conditionals​.
    
* Applying logical operators (`and`, `or`)​.
    
* Handling user input with `input()`​.
    
* Creating a simple decision tree for gameplay​.
    

The game challenges players to make choices at various crossroads, leading them toward the treasure or an untimely end. It's a fun way to practice decision-making logic in Python.

1. ## `if`***,*** `else` ***Basics :-***
    

These statements help your program **make decisions**.

```python
if Condition:
    Do this
else:
    Do this
```

* `if` checks the condition.
    
* `else` runs if the `if` condition is false.
    
* Now :- we’ll elaborate the if & else (conditional) statements.
    
    * Conditionals in python are used to check a condition and execute specific lines of code based on whether the condition is True or False.
        
        * ***Condition Check :-***
            
            * In Python to check a conditions and tell the computer what to do in each case.
                
            * if &lt;this condition is true&gt;:
                
                    &lt;then execute this line of code&gt;
                
                * ```python
                    age = 18 
                    if age >= 18:
                        print("You Can vote")
                    ```
                    
        * ***What if the condition is false?***
            
            * The else keyword is used to define a block of code that will execute if the condition checked in the if statement is false.
                
            * if &lt;this condition is true&gt;:
                
                    &lt;then don’t execute this line of code&gt;
                
                else:
                
                    &lt;then execute this line of code&gt;.
                
                * ```python
                    if pigs can fly:
                        <Some code that will never execute>
                    else:
                        print("This is real life")
                    ```
                    
                * ***Note :- Python Indentation (*** Python uses indentation to denote hierarchichal relationships between lines of code such as parent and child lines).
                    
                * Example :
                    
                    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744628450489/75f81601-47d4-48da-855d-5829f1ebfcf7.png align="center")
                    
    
    2. ## ***Comparator Operators :-***
        
    
    * Comparison operators are used to **compare two values**. They always return a **Boolean value** — either `True` or `False`.
        
        ### ✅ Common Python Comparison Operators:
        
        * `==` → **Equal to :-**  
            Checks if two values are equal.  
            Example: `5 == 5` → `True`.
            
        * `!=` → **Not equal to :-**  
            Checks if two values are not equal.  
            Example: `5 != 3` → `True`.
            
        * `>` → **Greater than :-**  
            Checks if the left value is greater than the right.  
            Example: `10 > 7` → `True`.
            
        * `<` → **Less than :-**  
            Checks if the left value is less than the right.  
            Example: `3 < 8` → `True`.
            
        * `>=` → **Greater than or equal to :-**  
            True if the left value is greater than or equal to the right.  
            Example: `5 >= 5` → `True`.
            
        * `<=` → **Less than or equal to :-**  
            True if the left value is less than or equal to the right.  
            Example: `2 <= 3` → `True`.
            
    
    3. ## ***What is the Modulo Operator?***
        
    
    * The **modulo operator** `%` gives you the **remainder** after dividing one number by another.
        
    * It's like asking: “**What’s left over?**” after you divide two numbers.
        
    * ```python
        7 % 3  # output will be 1  
        6 % 2  # output will be 0
        6 % 5  # output will be 1
        6 % 4  # output will be 2
        ```
        
    * **<mark>Write some code using what you have learnt about the modulo operator and conditional checks in Python to check if the number in he input area is odd or even. If it's odd print out the word "Odd" otherwise printout "Even".</mark>**
        
        * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744630184036/d15f5086-9c84-40c2-bb39-c6e893039339.png align="center")
            
    
    4. ## ***Understanding*** `elif` ***and Nested*** `if` ***Statements in Python :***
        
    
    ### What is `elif`?
    
    * `elif` stands for **“else if”.**
        
    * It's used when you want to **check multiple conditions**, one after another.
        
    * It comes **after an** `if` and **before an** `else`.
        
    * Many elif conditions can come between if and else statement.
        
        * ```python
            age = 17
            
            if age > 18:
                print("Adult")
            elif age == 18:
                print("Just turned adult!")
            else:
                print("Minor")
            ```
            
        * The program first checks: `Is age > 18?` → No.
            
        * Then it checks: `Is age == 18?` → No.
            
        * So, it goes to the `else` and prints: **"Minor".**
            
    
    **What is Nesting (**`Nested if` **Statements)?**
    
    * **Nesting** means putting one `if` **inside** another.
        
    * It’s used when a decision **depends on another decision.**
        
        * ```python
            age = 20
            has_id = True
            
            if age >= 18:
                if has_id:
                    print("You can enter.")
                else:
                    print("ID required.")
            else:
                print("You're too young.")
            ```
            
        * First, it checks: `Is age >= 18?`
            
        * If **yes**, then it goes inside and checks: `Do you have ID?`
            
        * If either condition fails, you get the right message.
            

5. ## ***Build an automatic pizza order program :-***
    
    Based on a user's order, work out their final bill. Use the input() function to get a user's preferences and then add up the total for their order and tell them how much they have to pay.
    
    Small pizza (S): $15
    
    Medium pizza (M): $20
    
    Large pizza (L): $25
    
    Add pepperoni for small pizza (Y or N): +$2
    
    Add pepperoni for medium or large pizza (Y or N): +$3
    
    Add extra cheese for any size pizza (Y or N): +$1
    

* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744632559002/0e6f085d-1e37-4fca-a2b0-6d2b2b3f0b56.png align="center")
    

6. ## ***Treasure Island Project :-***
    

* ### ***Flow Chart :***
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744633158778/88ba3a9d-13ac-40f0-8265-bc994c9c89ea.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744636446254/2f620f28-a001-4e71-9479-0369e75f47e2.png align="center")