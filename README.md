import random

print(" Welcome to Rock, Paper, Scissors!")
print("Get ready to test your luck and reflexes against the computer.\n")


user_score = 0
computer_score = 0


while True:
    
    user_choice = input("Choose rock, paper, or scissors (or type 'quit' to exit): ").lower()

    if user_choice == 'quit':
        print(" Thanks for playing! Final score:")
        print(f" You: {user_score} | Computer: {computer_score}")
        break

    if user_choice not in ['rock', 'paper', 'scissors']:
        print("Invalid choice! Please choose rock, paper, or scissors.\n")
        continue

    
    options = ['rock', 'paper', 'scissors']
    computer_choice = random.choice(options)

    
    print(f"\n You chose: {user_choice}")
    print(f"Computer chose: {computer_choice}")

   
    if user_choice == computer_choice:
        print(" It's a tie!")
    elif (
        (user_choice == 'rock' and computer_choice == 'scissors') or
        (user_choice == 'paper' and computer_choice == 'rock') or
        (user_choice == 'scissors' and computer_choice == 'paper')
    ):
        print("🎉 You win this round!")
        user_score += 1
    else:
        print(" Computer wins this round!")
        computer_score += 1

    
    print(f" Current Score — You: {user_score} | Computer: {computer_score}\n")
