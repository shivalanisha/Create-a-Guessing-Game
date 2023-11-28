# Create-a-Guessing-Game
import random

def guessing_game():
    # Generate a random number between 1 and 100
    secret_number = random.randint(1, 100)
    attempts = 0

    print("Welcome to the Guessing Game!")
    print("I've selected a number between 1 and 100. Try to guess it.")

    while True:
        # Prompt the user for their guess
        user_guess = int(input("Enter your guess: "))
        attempts += 1

        # Compare the guess with the secret number
        if user_guess == secret_number:
            print(f"Congratulations! You guessed the correct number {secret_number} in {attempts} attempts.")
            break
        elif user_guess < secret_number:
            print("Too low! Try again.")
        else:
            print("Too high! Try again.")

# Run the game
guessing_game()
