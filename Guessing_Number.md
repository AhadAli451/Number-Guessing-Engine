# Statement 

Basically It's a number guessing game and it make will a simple class means object orinted programing (__OOPS__) and it simply ask you What's your number if will  your number hiegh than computer number computer tell that your number is heigh from my number same if your number lower than computer number so computer tell you it's lower from my number 

In this used
 (__OOP__), 
 __while loop__
 __If statement__
 And take input from user 
 __input__

 # solution

 ``` python
 import random

class NumberGuessingGame:
    def __init__(self):
        self.random_generate_num = random.randint(1, 20)
        self.allow_attempts = 3
        self.user_attempts = 0

    def play(self):
        print("Welcome To The Number Guessing Game!")

        while self.user_attempts < self.allow_attempts:
            try:
                print(f"Attempts left: {self.allow_attempts - self.user_attempts}")
                # Get user input and ensure it's an integer
                user_input = int(__builtins__.input("Enter a number between 1 and 20: "))
                self.user_attempts += 1

                if user_input == self.random_generate_num:
                    print(f"Congrats! You guessed the number {self.random_generate_num} correctly!")
                    break
                elif user_input < self.random_generate_num:
                    print("Too low!")
                else:  # user_input > self.random_generate_num
                    print("Too high!")
            except ValueError:
                print("Invalid input! Please enter a valid integer.")

        if self.user_attempts == self.allow_attempts and user_input != self.random_generate_num:
            print(f"Sorry! You've used all attempts. The correct number was {self.random_generate_num}.")
        print("Thank you for playing!")

game = NumberGuessingGame()
game.play()
```