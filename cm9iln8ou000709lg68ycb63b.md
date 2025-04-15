---
title: "(Day 04) Task : Rock , Paper  & Scissors Project :-"
datePublished: Tue Apr 15 2025 14:29:58 GMT+0000 (Coordinated Universal Time)
cuid: cm9iln8ou000709lg68ycb63b
slug: day-04-task-rock-paper-and-scissors-project
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1744727295485/6280f4eb-c48c-41aa-ad7e-6e65b2ba46fc.jpeg
tags: python, 100daysofpython, listinpython, pythonnumbers-in-pythonpython-programmingpython-tutorialpython-numberspython-random-numbersnumbers-in-python-3python-numbers-tutorialpython-adding-numberspython-for-beginnerswhat-is-python-numberspython-numbers-modulepython-formatting-numbershow-python-numbers-workpython-multiplying-numberspython-tutorial-for-beginnerspython-integerspython-numbers-to-wordspython-numbers-complexpython-numbers-examplepython-complex-numbers, randomisation-python, day04-of-100-days-of-python

---

## What You Will Learn – Day 04: Randomisation & Python Lists

* How to use the `random` module to generate random values.
    
* Generate random integers, floats, and choices from a list.
    
* Understand and create Python lists to store multiple values.
    
* Perform basic list operations: access, update, add, remove, and count items.
    
* Combine randomisation and lists in fun, real-world mini projects.
    
* Build cool mini games like:
    
    * Coin Toss (Heads or Tails).
        
    * Banker Roulette.
        
    * Rock, Paper, Scissors game (vs Computer).
        

## ***Randomisation in Python :-***

* Randomisation is used when you want your program to do something unexpected or random, like rolling a dice, flipping a coin, or picking a random winner.
    
* Helps to take a random value from computer.
    
* Computers are not random, because they are built with circuits and switches. But randomness is very important when building software, especially games. It would be really boring if every move in a video game was pre-determined.
    
* So, some computer scientists invented pseudorandom number generators.
    
* **Pseudorandom number generators :** These are algorithms used by computers to mimic randomness , as computers are inherently not random.
    
* If you want to learn more about pseudorandom number generators, I recommend watching this video by Khan Academy: [https://www.youtube.com/watch?v=GtOt7EBNEwQ&ab\_channel=KhanAcademyLabs](https://www.youtube.com/watch?v=GtOt7EBNEwQ&ab_channel=KhanAcademyLabs)
    

## ***Different Types of Random in Python :-***

* Python’s `random` module has many useful functions. Each type helps you create different kinds of randomness depending on your use case.
    
* Now we’ll discuss basic types :-
    
    ### 1\. **Random Integers :-**
    
    #### ✅ `random.randint(a, b)`
    
    * Returns a random integer between `a` and `b` (both included).
        
    
    ```python
    random.randint(1, 10)  # Example: 7
    ```
    
    #### ✅ `random.randrange(start, stop, step)`
    
    * Like `range()`, but returns a random value from that range.
        
    
    ```python
    random.randrange(0, 10, 2)  # Possible outputs: 0, 2, 4, 6, 8
    ```
    
    ### 2\. **Random Floats :-**
    
    #### ✅ `random.random()`
    
    * Returns a float between `0.0` and `1.0`.
        
    
    ```python
    random.random()  # Example: 0.6583
    ```
    
    #### ✅ `random.uniform(a, b)`
    
    * Returns a float between `a` and `b`.
        
    
    ```python
    random.uniform(5.5, 10.5)  # Example: 7.24
    ```
    

## ***Heads or Tails :-***

* Create a coin flip program using what you have learnt about randomisation in Python. It should randomly print "Heads" or "Tails" every time it runs.
    
* ***Note :-*** Before Working on random module the basic we all have to understand is that we should always import that module first.Python doesn’t have built-in random functions ready to use by default.
    
* To use features like random numbers, random selection, or shuffling, we need to import the `random` module first.
    
* ```python
    import random.   
    f = random.randint( 0 , 1)
    if f == 0:
        print("you get tail")
    else:
        print("you get heads")
    ```
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744723027973/1778348e-b715-4192-b147-776d9ef2c4f2.png align="center")
    

## ***What is a List in Python?***

A list in Python is like a container or a box that holds multiple items in a single place.

* You can store numbers, words, or both in a list.
    
* Lists help keep things organised and grouped together.
    
* Think of a list like a shopping list or a list of your favorite songs.
    
* it’s a way of organising and storing data & it is a data structure in python.
    

### ***Key Points About Lists :-***

List\_name = \[Set Of items\]

* Lists are written using square brackets `[ ]`
    
* Items inside a list are separated by commas.
    
* You can access, add, change, or remove items.
    

### ***How to Create a List :-***

* ```python
    my_list = ["apple", "banana", "cherry"]
    ```
    
* This list has 3 items: `"apple"`, `"banana"`, and `"cherry"`.
    

## ***Common List Operations :-***

### **1\. Accessing Items in a list :**

* Get items using their position (index). Python starts counting from 0(Remember that everything computer related, the first number we count with is 0 and never 1. 0, 1, 2, 3 instead of 1, 2, 3 4.)
    
* You can provide the name of the list then a square bracket and then the item’s index that you want.
    
* ***Negative Indices:-***
    
    * You can access items in the list counting from the end of the list by using negative whole numbers. e.g. `print(states_of_america[-1])` —&gt; #output will be Hawaii.
        
* ```python
    states_of_america = ["Delaware", "Pennsylvania", "New Jersey", "Georgia", 
    "Connecticut", "Massachusetts", "Maryland", "South Carolina", "New Hampshire",
     "Virginia", "New York", "North Carolina", "Rhode Island", "Vermont", 
    "Kentucky", "Tennessee", "Ohio", "Louisiana", "Indiana", "Mississippi", 
    "Illinois", "Alabama", "Maine", "Missouri", "Arkansas", "Michigan", "Florida",
     "Texas", "Iowa", "Wisconsin", "California", "Minnesota", "Oregon", "Kansas",
     "West Virginia", "Nevada", "Nebraska", "Colorado", "North Dakota", 
    "South Dakota", "Montana", "Washington", "Idaho", "Wyoming", "Utah", 
    "Oklahoma", "New Mexico", "Arizona", "Alaska", "Hawaii"]
    
    print(states_of_america[5])    #output will be Massachusetts
    print(states_of_america[-1])   #output will be Hawaii
    ```
    

### **2\. Adding new Items in a list :**

* You can add items to the end of a List using the append() function.
    
* ```python
    fruits = ["Cherry", "Apple", "Pear"]
    fruits.append("Orange") # orange will be added to list at the final index
    ```
    

### **3\. Changing any Item in a list :**

* Nothing just like accessing we have to just use the index and give it a new value.
    
* ```python
    my_list[1] = "mango"
    ```
    
* Changes `"Apple"` to `"mango"`.
    

### **4\. Removing any Item in a list :**

* Helps to remove any element or attribute from the list.
    
* ```python
    my_list.remove("apple")
    ```
    
* Removes `"apple"` from the list.
    

### **5\. List Length :**

* Helps to find the length of any list.
    
* ```python
    print(len(my_list))
    ```
    
* Tells you how many items are in the list.
    

### **Note:-**

* Lists Can Store Different Data Types.
    
* ```python
    mixed_list = ["Python", 3.14, 10, True]
    ```
    
* A list can contain strings, numbers, booleans — anything!
    

### **Code :-**

* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744725326780/c23e86c3-4a20-4ea2-bd54-5d6fefd817e0.png align="center")
    

## **Banker Roulette :-**

* **Figure out how to pick a random name from the list of friends.**
    
    * ```python
        import random
        friends = ["Alice", "Bob", "Charlie", "David", "Emanuel"]
        #case 1
        
        F = random.choice(friends)
        print(F)
        #case 2
        
        F = random.randint(0 , 3)
        print(friends[F])
        ```
        
    * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744725741351/25789cd1-55f0-42b6-b5d4-104993324fee.png align="center")
        

## ***Rock , Paper & Scissors Project :-***

### Code :-

* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744726280029/5db06077-48c3-443a-93ad-7e1921734a4a.png align="center")
    

### Output :-

* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744726425735/66b4df5a-b24d-48ae-982b-7cee6ea28c5b.png align="center")