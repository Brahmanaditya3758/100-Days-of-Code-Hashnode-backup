---
title: "(Day 07) Task : Hangman Project :-"
datePublished: Tue Apr 29 2025 02:31:11 GMT+0000 (Coordinated Universal Time)
cuid: cma1w4sp0000r09k1bwac9qcb
slug: day-07-task-hangman-project
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1745893856264/f1d1d3ce-aa40-45fe-974b-0d4aeb07f7ba.png
tags: python, 100daysofcode, dr-angela-yu, day-07, hangman-project, python-day-07

---

Our goal is to build a Hangman game using everything we have learnt about Python programming.

**Goal:**  
The player has to guess a hidden word, letter by letter, before running out of lives (wrong guesses).

# How It Works:

1. **Random Word Selection**:
    
    * The game randomly picks a word from a word list (`hangman_`[`words.py`](http://words.py)).
        
2. **Display**:
    
    * A series of blanks `_ _ _` are shown, one for each letter in the word.
        
3. **User Input**:
    
    * The player guesses one letter at a time.
        
4. **Checking the Guess**:
    
    * If the letter is in the word, it reveals the letter(s) at the correct position(s).
        
    * If the letter is wrong, the player loses one life.
        
5. **Lives and Hangman Drawing**:
    
    * The player starts with 6 lives.
        
    * Each wrong guess draws part of the hangman (from `hangman_`[`art.py`](http://art.py)).
        
    * Full drawing = game over.
        
6. **End Game**:
    
    * **Win**: Player guesses all letters correctly.
        
    * **Lose**: Player runs out of lives (0 lives left).
        
7. **Extra Features**:
    
    * Shows already guessed letters.
        
    * Does not deduct life for repeated guesses.
        
    * Displays logo at the start.
        
    * Shows lives left after every wrong guess.
        

# Key Python Concepts Used:

* Random choice (`random.choice`)
    
* Loops (`for`, `while`)
    
* Lists (`display`, `guessed_letters`)
    
* String operations (lowercase, joining)
    
* Imports (separate files for better organization)
    

### ***Demo Final Project :***

[https://appbrewery.github.io/python-day7-demo/](https://appbrewery.github.io/python-day7-demo/)

The project is split into 5 major steps. In each step, there will be multiple TODOs. Your goal is to go through each todo in order and complete them.

### ***TODO-1 :***

Randomly choose a word from the word\_list and assign it to a variable called chosen\_word. Then print it.

```python
import random

word_list = ['apple', 'banana', 'cherry', 'date', 'elderberry']

# Randomly choose a word
chosen_word = random.choice(word_list)

# Print the chosen word
print(chosen_word)
```

***Explanation:***

* `random.choice(word_list)` picks a random element from the list.
    
* Then it gets stored in the variable `chosen_word`.
    
* Finally, `print(chosen_word)` displays it.
    

### ***TODO-2 :***

Ask the user to guess a letter and assign their answer to a variable called guess. Make the String stored in guess lowercase.

```python
# Ask the user to guess a letter
guess = input("Guess a letter: ").lower()

# Print the guess to check
print(guess)
```

***Explanation:***

* `input()` takes the user’s input as a string.
    
* `.lower()` converts the input to lowercase, so even if they enter a capital letter, it becomes lowercase.
    

### ***TODO-3 :***

Check if the letter the user guessed guess is one of the letters in the chosen\_word. Loop through each of the letters in the chosen\_word and print "Right" if the letter is a match, "Wrong" if it's not.

```python
# Loop through each letter in the chosen_word
for letter in chosen_word:
    if letter == guess:
        print("Right")
    else:
        print("Wrong")
```

***Explanation:***

* Loops through each letter in the chosen word.
    
* If the letter matches the guess, prints `"Right"`, otherwise prints `"Wrong"`.
    

### ***TODO-4 :***

* Create an empty String called placeholder.
    
* For each letter in the chosen\_word, add a \_ to placeholder.
    
* So if the chosen\_word was "apple", placeholder should be *with 5 ""* representing each letter to guess.
    
* Print out hint.
    

```python
# Create an empty string for the placeholder
placeholder = ""

# Add an underscore "_" for each letter in the chosen word
for letter in chosen_word:
    placeholder += "_ "

# Print the hint
print(placeholder)
```

### ***TODO-5 :***

* Create an empty string called "display".
    
* Loop through each letter in the chosen\_word
    
* If the letter at that position matches guess then reveal that letter in the display at that position.
    
* e.g. If the user guessed "p" and the chosen word was "apple", then display should be *p p* \_.
    
* Print display and you should see the guessed letter in the correct position.
    
* But every letter that is not a match is represented with a "\_".
    

```python
# Create an empty string (or better: list) for the display
display = ""

# Loop through each letter in the chosen_word
for letter in chosen_word:
    if letter == guess:
        display += letter + " "  # reveal the guessed letter
    else:
        display += "_ "  # show _ for unguessed letters

# Print the updated display
print(display)
```

### TODO-6 :

* Use a while loop to let the user guess again.
    
* The loop should only stop once the user has guessed all the letters in the chosen\_word.
    
* At that point display has no more blanks ("\_"). Then you can tell the user they've won.
    

```python
while "_" in display:
    guess = input("Guess a letter: ").lower()

    # Check guessed letter against each position
    for position in range(len(chosen_word)):
        letter = chosen_word[position]
        if letter == guess:
            display[position] = letter

    # Print current state
    print(" ".join(display))

# All blanks are filled -> user wins
print("Congratulations! You guessed the word:", chosen_word)
```

### TODO-7 :

* Create a variable called lives to keep track of the number of lives left.
    
* Set lives to equal 6.
    
* If guess is not a letter in the chosen\_word, Then reduce lives by 1.
    
* If lives goes down to 0 then the game should end, and it should print "You lose."
    
* print the ASCII art from the list stages that corresponds to the current number of lives the user has remaining.
    

```python
# Set the number of lives
lives = 6
# Hangman ASCII stages (index 6 -> 0 lives)
stages = [
    '''
      +---+
      |   |
      O   |
     /|\\  |
     / \\  |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
     /|\\  |
     /    |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
     /|\\  |
          |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
     /|   |
          |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
      |   |
          |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
          |
          |
          |
    =========
    ''',
    '''
      +---+
      |   |
          |
          |
          |
          |
    =========
    '''
]
while "_" in display and lives > 0:
    guess = input("Guess a letter: ").lower()

    # Track if guess was correct
    if guess in chosen_word:
        for position in range(len(chosen_word)):
            letter = chosen_word[position]
            if letter == guess:
                display[position] = letter
    else:
        lives -= 1
        print(f"Wrong guess. Lives left: {lives}")

    # Print the current state of display
    print(" ".join(display))

# Final result
if "_" not in display:
    print("Congratulations! You guessed the word:", chosen_word)
else:
    print("You ran out of lives. The word was:", chosen_word)
```

## ***Project :***

### TODO-1 :

* Update the word list to use the word\_list from hangman\_words.py
    

### TODO-2 :

* Update the code to use the stages from the file hangman\_art.py
    

### TODO-3 :

* Import the logo from hangman\_[art.py](http://art.py) and print it at the start of the game.
    

### TODO-4 :

* If the user has entered a letter they've already guessed, print the letter and let them know.
    
* We should not deduct a life for this.
    
* e.g. You've already guessed a
    

### TODO-5 :

* If the letter is not in the chosen\_word, print out the letter and let them know it's not in the word.e.g. You guessed d, that's not in the word. You lose a life.
    

### TODO-6 :

* Update the code below to tell the user how many lives they have left. print("\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*&lt;???&gt;/6 LIVES LEFT\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*")
    

### TODO-7 :

* Update the print statement to give the user the correct word they were trying to guess.
    
* e.g. IT WAS &lt;Correct Word&gt;! YOU LOSE
    

```python
word_list = [
    'apple', 'banana', 'cherry', 'date', 'elderberry', 'fig', 'grape',
    'honeydew', 'kiwi', 'lemon', 'mango', 'nectarine', 'orange', 'peach',
    'pear', 'plum', 'raspberry', 'strawberry', 'tangerine', 'watermelon'
]

logo = '''
 _                                             
| |                                            
| |__   __ _ _ __   __ _ _ __ ___   __ _ _ __  
| '_ \ / _` | '_ \ / _` | '_ ` _ \ / _` | '_ \ 
| | | | (_| | | | | (_| | | | | | | (_| | | | |
|_| |_|\__,_|_| |_|\__, |_| |_| |_|\__,_|_| |_|
                    __/ |                      
                   |___/   
'''

stages = [
    '''
      +---+
      |   |
      O   |
     /|\\  |
     / \\  |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
     /|\\  |
     /    |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
     /|\\  |
          |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
     /|   |
          |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
      |   |
          |
          |
    =========
    ''',
    '''
      +---+
      |   |
      O   |
          |
          |
          |
    =========
    ''',
    '''
      +---+
      |   |
          |
          |
          |
          |
    =========
    '''
]

import random
from hangman_words import word_list
from hangman_art import stages, logo

# TODO-3: Print the logo
print(logo)

# Choose a random word from word_list
chosen_word = random.choice(word_list)

# Create display with "_"
display = []
for _ in chosen_word:
    display.append("_")

# Set number of lives
lives = 6

# Create a list to store already guessed letters
guessed_letters = []

# Start game loop
while "_" in display and lives > 0:
    guess = input("Guess a letter: ").lower()

    # TODO-4: Check if user already guessed this letter
    if guess in guessed_letters:
        print(f"You've already guessed '{guess}'. Try a new letter.")
        continue
    else:
        guessed_letters.append(guess)

    # Check guess
    if guess in chosen_word:
        # Correct guess
        for position in range(len(chosen_word)):
            letter = chosen_word[position]
            if letter == guess:
                display[position] = letter
    else:
        # Wrong guess
        lives -= 1
        # TODO-5: Tell the user the wrong letter
        print(f"Oops! '{guess}' is not in the word.")
        # TODO-6: Show how many lives are left
        print(f"****************************<{lives}/6 LIVES LEFT>****************************")
        print(stages[lives])

    # Show the current guessed letters
    print(" ".join(display))
    print("\n")

# Final result
if "_" not in display:
    print(f"Congratulations! You guessed the word: {chosen_word}")
else:
    # TODO-7: Tell user the correct word when they lose
    print(f"IT WAS '{chosen_word.upper()}'! YOU LOSE!")
```