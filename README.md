# rock-paper-and-scissors
rock,paper and scissors assignment





import numpy as np     #library
user_name=input('Enter your name: ')       #user name
def play_again():           #func to check if user wants to play again or not
    start_game()            #recursion function

def start_game():          #the function of the game
    user_choice=input('Enter your choice: ')          #user choice
    def computer():        #computer choose randomly
        if np.random.randint(3)==0 and user_choice !='paper':
           computer_choice='paper'
        elif np.random.randint(3)==1 and user_choice !='rock':
           computer_choice='rock'
        else :
           computer_choice='scissors'   
        return computer_choice
    computer_choice=computer()
    print('Computer choice is: '+ computer_choice)
    if computer_choice=='paper' and user_choice=='rock':
        print('Computer won!')
    elif computer_choice=='paper' and user_choice=='scissors':
        print(user_name +' won!')
    elif computer_choice=='rock' and user_choice=='scissors':
        print('Computer won!')
    elif computer_choice=='scissors' and user_choice=='paper':
        print('Computer won!')
    elif computer_choice=='rock' and user_choice=='paper':
        print(user_name +' won!')
    else :
        print(user_name +' won!')
    play_agai=input('Do you want to play again? ' )
    if play_agai=='yes':
        play_again()
    elif play_agai=='no':
        print('Thank you!')
    else:
        print('Undefined word! ')
start_game()
