import random

def display_title():
    print("Guessing Game")
    print()
    
def play_game(limit):
    number = random.randint(1, limit)
    print(f"I'm thinking of a number from 1 to {limit}. \n")
    count = 1
    guess = int(input("Your guess?: "))
    
    while(guess != number):
        if guess < number:
            print("Too low")
            count += 1
        elif guess > number:
            print("Too high")
            count += 1
            guess = int(input("Your guess?: "))
    print(f"You got it in {count} tries.")

def main():
    display_title()
    again = "yes"
    while again.lower() == "yes":
        limit = int(input("Enter limit "))
        play_game(limit)
        again = input("Play again? Enter yes or no: ")
        print()
    print("Bye!")
   
if __name__ == "__main__":
    main()
