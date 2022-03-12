# Guessing-Number-game
Created simple mathematical game of guessing number using Python.

## Installatiom
You just require python IDE in your laptop/PC.

## What is this game??
The game is straightforward. The user must select a random number between 1 to 100 from a number of choices. The system will attempt to guess the number with the minimum possible guesses. That's it.

## Algorithm 
1. Define the range of the numbers (lower and upper). It's 1-100 here.
2. Let user choose the number from the above range (1-100).
3. Set the guessed number initially to the middle of the range.
4. Start the game by displaying the user a message saying “Choose the number from X to Y”. You may update the message as you wish.
5. Initialize a variable guess_count to 0 to count the total number of chances that the computer has taken to guess the number correctly.
6. Write an infinite loop.
  a. Increment the chances that the user has taken to guess.
  a. Show the guessed number to user and also give other option to get further guesses correct.
  b. If the current guessed number is less than the users guessed number, then set lower range to guesssed number and get new guessed number.
  c. If the current guessed number is greater than the users guessed number, then set lower range to guesssed number and get new guessed number.
  b. If the current guessed number is equal to the users guessed number, break the loop and end the game.

## Python code
```python
# Start code
import time

# Ask user to choose a number
print("Please choose any integer between 1 and 100 and memorise it.")
print("I'll (computer) take a guess at the number you've chosen; nevertheless, please assist me in answering the following questions.")

time.sleep(2)

print("Have you decided on a number?")
print("Press Enter")
input()

print("Lets start the game!")

# Set the guessed number to middle of range
lower_range = 1
upper_range = 100
guessed_number = (lower_range + upper_range)//2

# Number of guesses required
guess_count = 0

while True:
  guess_count += 1
  print("Computer's guessed nummber is", guessed_number)
  print("Please Enter 1: If computer's guessed number is lower then what you have choosen!")
  print("Please Enter 2: If computer's guessed number is greater then what you have choosen!")
  print("Please Enter 3: If computer's guessed number is equal to what you have choosen!")
  
  user_response = int(input("Please Enter your response: "))

  if user_response == 1:
    lower_range = guessed_number

  elif user_response == 2:
    upper_range = guessed_number

  elif user_response == 3:
    print("Oh! I found it in ", guess_count, "guesses")
    break
  
  else:
    print("Invali Number!, Please Enter valid number")

  guessed_number = (lower_range + upper_range)//2 # New guessed number

```

## Conclusion

