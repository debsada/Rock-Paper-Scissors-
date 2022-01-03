# Rock-Paper-Scissors-
A rock paper scissors game where the computer randomly chooses a move that corresponds with the user's inputed move and decides whether it is a win, lose or draw situation. 
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

#Write your code below this line 👇
import random

choices = [rock, paper, scissors]
print("Welcome to rock, paper, scissors!")
users_choice = int(input("what do you choose? Type 0 for Rock, 1 for paper or 2 for scissors \n"))

comp_choice = random.randint(0,2)

if users_choice >= 3 or users_choice < 0:
  print("You have chosen an invalid number, you lose!") #first checks whether user has inputed an invalid number before running rest of code
else:
  print(choices[users_choice])
  print(f" computer chose: \n {choices[comp_choice]}")

  if users_choice == comp_choice:
    print("It's a draw!")
  elif (users_choice == 0 and comp_choice == 2) or (users_choice == 1 and comp_choice == 0) or (users_choice == 2 and comp_choice == 1):
    print("You win!") #all possible situations of user winning so that else statement catches all situations of the computer winning 
  else:
    print("You lose!")

    
  
