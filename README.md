# Guess A Number Game

## Overview
The **Guess A Number Game** is a simple Python-based guessing game where the player tries to guess a randomly generated number between 1 and 100. The game provides feedback to help guide the player’s guesses, indicating if the guess is too high or too low. The game ends when the player correctly guesses the number.

## How It Works
1. The computer randomly selects a number between 1 and 100.
2. The player is prompted to guess the number.
3. Based on the player's guess, the game provides hints:
   - "Too High!" if the guess is higher than the target number.
   - "Too Low!" if the guess is lower than the target number.
   - "You guessed it!" if the player’s guess matches the computer's number, ending the game.

## Code Example

```python
import random

computer_number = random.randint(1, 100)

while True:
    player_input = input('Guess the number (1 - 100): ')

    if not player_input.isdigit():
        print('Invalid input. Try again...')
        continue

    player_number = int(player_input)

    if player_number == computer_number:
        print('You guessed it!')
        break
    elif player_number > computer_number:
        print('Too High!')
    else:
        print('Too Low!')
