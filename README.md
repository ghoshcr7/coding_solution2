# coding_solution2
A simple tic tac toe game
import random
computer_score=0
user_score=0
while True:
    option=['stone','paper','scissor']
    a=random.choice(option)
    user_input=input('''enter your option
          1)stone
          2)paper
          3)scissor

          press q to exit

          enter your value: ''')
    if user_input.isdigit()==True:
        user_input=int(user_input)
        if option[user_input-1]==a:
            computer_score,user_score=computer_score,user_score
            print("we are same")
            
        elif option[user_input-1]=='stone':
            if a=='paper':
                computer_score=computer_score+1
                print("computer wins")
                print("computer score=",computer_score,"    user score=",user_score)
                print(" ")
            elif a=='scissor':
                user_score=user_score+1
                print("user wins")
                print("computer score=",computer_score,"    user score=",user_score)
                print(" ")
        elif option[user_input-1]=='paper':
            if a=='scissor':
                computer_score=computer_score+1
                print("computer wins")
                print("computer score=",computer_score,"    user score=",user_score)
                print(" ")
            elif a=='stone':
                user_score=user_score+1
                print("user wins")
                print("computer score=",computer_score,"    user score=",user_score)
                print(" ")
        elif option[user_input-1]=='scissor':
            if a=='stone':
                computer_score=computer_score+1
                print("computer wins")
                print("computer score=",computer_score,"    user score=",user_score)
                print(" ")
            elif a=='paper':
                user_score=user_score+1
                print("user wins")
                print("computer score=",computer_score,"    user score=",user_score)
                print(" ")    
    elif user_input.isdigit()==False:
        if str(user_input)=='q':
          print("final score")
          print("computer score=",computer_score,"    user score=",user_score)
          break
        else:
          print("invalid input")
          print(" ")    
