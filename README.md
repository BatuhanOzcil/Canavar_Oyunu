import random

print("Welcome to the Adventure Game in Magic Island!")
print("A wild monster appears!")

player=100
monster=100
def perform_attack(player,monster):
    player_hasar=random.randint(10,20)
    monster_hasar=random.randint(10,20)

    player-=monster_hasar
    monster-=player_hasar

    if player <0:
        player= 0
    if monster <0:
        monster=0

    return player,monster,player_hasar,monster_hasar

def battle():
    player = random.randint(50,100)
    monster=random.randint(50,100)
    print("Player's health = ",player)
    print("Monster's health = ", monster)
    round=1
    while player >0 and monster >0:
        print("Round: ",round)
        player,monster,player_hasar,monster_hasar=perform_attack(player,monster)
        print("You attack monster and dealt ",player_hasar,"damage.")
        print("The monster attacks you back with ",monster_hasar,"damage.")
        print("Player's health = ",player)
        print("Monster's health = ", monster)
        round+=1

    if player ==0:
        print("The monster defeated you, game over.")
    else:
        print("You defeated the monster, congratulations!")
battle()

