import random
def start_game():
welcome = ("Welcome to the Number Guessing Game!")
welcome_length=(len(welcome)+3)
border = print("*"* welcome_length)
print(welcome)
border = print("*"* welcome_length)
attempt_count = 0 
correct_number = random.randint(1,10)
high_score = [10]                 
while attempt_count > -1:
    try:
        guess = int(input("\nPlease pick a number between 1 and 10:  ")) 
        if guess not in range(1,11):
            print("Sorry, that number is not between 1 and 10. Please try again")
            continue
        if guess > correct_number:
            print("Sorry, that is higher than the correct number.  Please try again.")
            guess = int(input("\nPlease pick a number between 1 and 10:  "))
            attempt_count += 1
        if guess < correct_number:
            print("Sorry, that is lower than the correct number.  Please try again.")
            guess = int(input("\nPlease pick a number between 1 and 10:  "))
            attempt_count += 1             
        if guess == correct_number:
            attempt_count += 1
            high_score.append(attempt_count)
            new_high_score = min(high_score)              
            print("\nYou got it!") 
            print("It took {} guesses.".format(attempt_count))
            print("The highest score is {} guesses.".format(new_high_score))
            play_again = input("This game is over. Would you like to play again? Y/N   ")
            play_again = play_again.lower()
            if play_again == "y":
                    attempt_count = 0
                    correct_number = random.randint(1,10)
                    continue
            if play_again == "n":
                    print("Thanks for playing. Have a great day!")
                    break
    except ValueError:
             print("That is not a number between 1 and 10. try again...")
