import random

Computer_Wins =0
Player_Wins=0


print(" WELCOME TO ROCK PAPER SCISSOR SPOCK LIZARD GAME - INSPIRED BY THE BIG BANG THEORY SHOW")
print("")
print("1. Rock(r)       2.Paper(p)       3.Scissor(s)       4.Spock(sp)       5.Lizard(l)")

def Choose_Option():
    user_choice = input("Choose Your Poison: ")

    if user_choice in ["Rock", "rock", "r", "R", "ROCK"]:
        user_choice = "r"
    elif user_choice in ["Paper", "paper", "p", "P", "PAPER"]:
        user_choice = "p"
    elif user_choice in ["Scissor", "Scissor", "s", "S", "SCISSOR"]:
        user_choice = "s"
    elif user_choice in ["Spock", "spock", "sp", "SP", "SPOCK"]:
        user_choice = "sp"
    elif user_choice in ["Lizard", "lizard", "l", "L", "LIZARD"]:
        user_choice = "l"
    else:
        print("I don't understand try again please")
        Choose_Option()
    return user_choice

def Computer_Choice():
    computer_choice = random.randint(1,5)
    if computer_choice ==1:
        computer_choice = "r"
    elif computer_choice ==2:
        computer_choice = "p"
    elif computer_choice ==3:
        computer_choice = "s"
    elif computer_choice ==4:
        computer_choice = "sp"
    elif computer_choice ==5:
        computer_choice = "l"
    return computer_choice

while True:
    print("")
    user_choice = Choose_Option()
    computer_choice = Computer_Choice()
    print("")

    player_wins=0
    computer_wins=0

    if user_choice == "r":
        if computer_choice == "r":
            print("Computer chose : Rock")
            print("IT WAS A TIE")
        elif computer_choice == "p":
            print("Computer chose : Paper")
            print("YOU GOT PAPERED. YOU LOSE")
            computer_wins +=1
        elif computer_choice == "s":
            print("Computer chose : Scissor")
            print("SCISSOR DEMOLISHED. YOU WIN")
            player_wins +=1
        elif computer_choice == "sp":
            print("Computer chose : Spock")
            print("YOU GOT VAPORIZED. YOU LOSE")
            computer_wins += 1
        elif computer_choice == "l":
            print("Computer chose : Lizard")
            print("LIZARD GOT CRUSHED. YOU WIN")
            player_wins += 1

    elif user_choice == "p":
        if computer_choice == "p":
            print("Computer chose : Paper")
            print("IT WAS A TIE")
        elif computer_choice == "r":
            print("Computer chose : Rock")
            print("ROCK GOT PAPERED. YOU WIN")
            player_wins +=1
        elif computer_choice == "s":
            print("Computer chose : Scissor")
            print("TALK ABOUT A PAPER-CUT. YOU LOSE")
            computer_wins +=1
        elif computer_choice == "sp":
            print("Computer chose : Spock")
            print("SPOCK GOT DISPROVED. YOU WIN")
            player_wins += 1
        elif computer_choice == "l":
            print("Computer chose : Lizard")
            print("THAT LIZARD WAS REALLY HUNGRY, HUH?. YOU LOSE")
            computer_wins += 1

    elif user_choice == "s":
        if computer_choice == "s":
            print("Computer chose : Scissor")
            print("IT WAS A TIE")
        elif computer_choice == "r":
            print("Computer chose : Rock")
            print("YOU GOT SMASHED. YOU LOSE")
            computer_wins +=1
        elif computer_choice == "p":
            print("Computer chose : Paper")
            print("TALK ABOUT A PAPER-CUT. YOU WIN")
            player_wins +=1
        elif computer_choice == "sp":
            print("Computer chose : Spock")
            print("YOU GOT SMASHED MATE. YOU LOSE")
            computer_wins += 1
        elif computer_choice == "l":
            print("Computer chose : Lizard")
            print("LIZARD GOT DECAPITATED. YOU WIN")
            player_wins += 1

    elif user_choice == "sp":
        if computer_choice == "sp":
            print("Computer chose : Spock")
            print("IT WAS A TIE")
        elif computer_choice == "r":
            print("Computer chose : Rock")
            print("ROCK GOT VAPORIZED. YOU WIN")
            player_wins +=1
        elif computer_choice == "s":
            print("Computer chose : Scissor")
            print("SCISSOR SMASHED. YOU WIN")
            player_wins +=1
        elif computer_choice == "p":
            print("Computer chose : Paper")
            print("YOU GOT DISPROVED. YOU LOSE")
            computer_wins += 1
        elif computer_choice == "l":
            print("Computer chose : Lizard")
            print("YOU GOT POISONED. YOU LOSE")
            computer_wins += 1

    elif user_choice == "l":
        if computer_choice == "l":
            print("Computer chose : Lizard")
            print("IT WAS A TIE")
        elif computer_choice == "r":
            print("Computer chose : Rock")
            print("YOU GOT CRUSHED. YOU LOSE")
            computer_wins +=1
        elif computer_choice == "s":
            print("Computer chose : Scissor")
            print("TALK ABOUT A PAPER-CUT. YOU LOSE")
            computer_wins +=1
        elif computer_choice == "sp":
            print("Computer chose : Spock")
            print("SPOCK GOT POISONED. YOU WIN")
            player_wins += 1
        elif computer_choice == "p":
            print("Computer chose : Paper")
            print("YOU ATE PAPER. YOU WIN")
            player_wins += 1



    print("")
    print("Player Wins :" +str(player_wins))
    print("Computer Wins :" + str(computer_wins))
    print("")


    user_choice = input("Wana Play Again? (y/n) ")
    if user_choice in ("Y", "y", "YES", "yes","Yes"):
        pass
    elif user_choice in ("N", "n", "NO", "no","No"):
        break
    else:
        break
