# actionmenu
#RPG Action Menu Charlie Parks

actions = ['run', 'fight', 'play guitar', 'give up']
locations =  ['temple', 'farm', 'cave', 'cygnus']

"""This function prints the original menu"""
def menu():
    
    v = 0
    z = -1
    
    print("2112: A Rush Fan Game")#Prints the game menu header
    print("Options for actions:")
    print("Actions to Complete:")
    for action in actions:#prints action list
        v = v + 1
        z = z + 1
        print(f"{v}. {actions[z]}")
        
    print("Locations available for travel:")
    
    v = 0
    z = -1
    
    for location in locations:#prints locations list
        v = v + 1
        z = z + 1
        print(f"{v}. {locations[z]}")

"""This functon is for user interaction"""
def interact():
    
    print("Select From the Choices Above")#instruction for entering input
    a = input("Choose Your Action or Enter Place to Travel:")
    b = a.lower()

    if b in actions:#if the user chose an action
        print(f"You chose to {b.title()}")
        
        if b == actions[0]:
            print("You chose to run back to your farma and away from the Solar Federation")
        elif b == actions[1]:
            print("You choose to stand and fight the Solar federation and their oppression")
        elif b == actions[2]:
            print("You chose to try and persude the priests with your music and show them how it isnt bad")
        elif b == actions[3]:
            print("You chose to give up and become yet another mindless follower of the solar federation")
            
    elif b in locations:#if the user chose to travel
        print(f"You chose to travel to {b.title()}")
        
        if b == locations[0]:
            print("You chose to travel to the Temple and confront the priests")
        elif b == locations[1]:
            print("You choose to travel back to your farm and relax")
        elif b == locations[2]:
            print("You chose to travel to the cave on your farm and play the guitar")
        elif b == locations[3]:
            print("You chose to travel to the black hole Cygnus and leave the Earth behind")
            
    else:#if there was an error entering the input
        print("Please try again")
            
#calls the above functions
menu()
interact()
