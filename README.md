# 
#add to inventory

#Set and print to check the starting inventory and first loot

playerinv = {'gold coin': 42, 'rope': 1}

print("Initial player inventory: ")

print(playerinv)

dragonLoot = ['gold coin', 'dagger', 'gold coin', 'gold coin', 'ruby']

print("Loot from Dragon: ")

print(dragonLoot)

#function to add loot to inventory

def addToInventory(inventory, loot):

    #change the loot list into a dictionary with values
    
    count_loot = {}

    for item in loot:
    
        count_loot.setdefault(item, 0)
        
        count_loot[item] = count_loot[item] + 1

    # adding the values with common key 
    
    for key in inventory: 
    
        if key in count_loot: 
        
            inventory[key] = inventory[key] + count_loot[key] 
        
        else: 
        
            pass
            
    #adding dictionaries together
    
    inventory = {**inventory, **count_loot}    

    print("The updated inventory is: ")
    print(inventory)
    

#try it the first time and check that it works

addToInventory(playerinv,dragonLoot)

witchLoot = ["gold coin", "gold coin", "witch hat"]

print("Loot from witch: ")

print(witchLoot)

#test what happens with further additions

addToInventory(playerinv,witchLoot)

ogreLoot = ["club", "rope"]

print("Loot from ogre: ")

print(ogreLoot)

addToInventory(playerinv,ogreLoot)
 

