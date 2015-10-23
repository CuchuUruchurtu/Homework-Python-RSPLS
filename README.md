# Homework-Python-RSPLS
Homework for Python course online from Rice University
# Cuchu Uruchurtu productions presents:

#Rock-paper-scissors-lizard-Spock 


# The key idea of this program is to equate the strings
# "rock", "paper", "scissors", "lizard", "Spock" to numbers
# as follows:
#
# 0 - rock
# 1 - Spock
# 2 - paper
# 3 - lizard
# 4 - scissors

import math
import random

# helper functions

  # converts name to number

def name_to_number(name):
    if   name == "rock":
          name = 0
    elif name == "Spock":
          name = 1
    elif name == "paper":
          name = 2
    elif name == "lizard":
          name = 3
    else:
         name = 4
    return name


# converts number to name
    
def number_to_name(number):
    if number == 0:
        number = "rock"
    elif number == 1:
          number = "Spock"
    elif number == 2:
        number = "paper"
    elif number == 3:
        number = "lizard"
    else:
         number = "scissors"
    return number


# How to determite winner of game

def rpsls(player_choice):
    player_number = name_to_number(player_choice)
    comp_number = random.randrange(0, 5)
    difference = (player_number - comp_number) % 5
    print "Player chooses", number_to_name (player_number)
    print "Computer chooses",number_to_name (comp_number)
    if difference == 0:
        print "Player and Computer ties!"
    elif difference == 1:
        print "Player wins !"
    elif difference == 2:
        print "Player wins!"
    elif difference == 3:
        print "Computer wins poor human!"
    else:
        print "Computer wins porr human!"
    return ""
    
   


 # testing the code 

rpsls("rock")
rpsls("Spock")
rpsls("paper")
rpsls("lizard")
rpsls("scissors")


