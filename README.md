# rock paper scissors game
import random

def get_user_choice():
    choices = ['rock', 'paper', 'scissors']
    user_input = input("Enter Rock, Paper, or Scissors: ").lower()
    while user_input not in choices:
        user_input = input("Invalid choice. Please enter Rock, Paper, or Scissors: ").lower()
    return user_input

def get_computer_choice():
    return random.choice(['rock', 'paper', 'scissors'])

def determine_winner(user, computer):
    if user == computer:
        return "It's a tie!"
    elif (user == 'rock' and computer == 'scissors') or \
         (user == 'scissors' and computer == 'paper') or \
         (user == 'paper' and computer == 'rock'):
        return "You win!"
    else:
        return "Computer wins!"

def play_game():
    print("=== Rock Paper Scissors Game ===")
    user_choice = get_user_choice()
    computer_choice = get_computer_choice()

    print(f"\nYou chose: {user_choice}")
    print(f"Computer chose: {computer_choice}")

    result = determine_winner(user_choice, computer_choice)
    print(f"\nResult: {result}")

if __name__ == "__main__":
    play_game()

💡 Features:

Accepts case-insensitive user input.

Validates input until the user enters a correct option.

Displays both user and computer choices.

Announces the result: win, lose, or tie.


🕹 To make it replayable:

Add a loop to keep playing until the user wants to quit. Let me know if you want that version too!

