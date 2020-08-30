# Grocery-Store-Inventory-System
Programming Principles - Assignment 1 (Sem 2)
I am going to make a grocery store inventory system for local grocery store owners and small businesses. The program will be made using PyCharm coding language. The program would have an easy interface and tools like time and date built in. The program would enable the employees and managers to add and delete items from the inventory easily and effieciently. 
The program would have a counter that will keep a record of all the products/goods available at any given time and also keep a record as to when was a specific product was added or deleted and by whom. It will show detailed description of all the items that are available. Managers should be able to see the total value of the products in stock and separtely as required. 
The program is going to have a simple interface so its easy to learn for the new employees. The program should be able to calculate the total value of revenue going in and out. It also would provide a report concisting of the products and the total value of purchases and revenue generated.

1. Create a welcome message, login portal, and well-designed item names. {5 hours}
2. Use a well organized and unique description of the items. {1 hour}
3. Create class setups that enable adding and subtracting items in the inventory. {5 hours}
4. Create a code that keeps a count of the stock. {4 hours}
5. Create logins for employees and managers. {4 hours}
6. Adding date and time to the program. {1 hour}
7. Deciding consistent units of measure for the items. {1 hour}
8. Creating a user-friendly and easy interface. {8 hours}
9. Making a code to calculate total revenue going in and out. {8 hours}
10. Bug fixes {8 hours}
11. Finalizing program {3 hours}

Class Diagrams:
<img src="https://embed.creately.com/PkwSZVHwpoz?token=oCZq8ubZOfZqLUwo&type=svg">

UI Diagrams:
https://docs.google.com/document/d/1TL6_I895JW0hPaeglFtT2tWgzQDdWMFXkwxWwb1pM1E/edit?usp=sharing 

PYCHARM MAIN FILE:

if __name__ == '__main__':
    print('Run Directly')
else:
    print('Run From Import')

import datetime

class Employees:
    def __init__(self, first, last):
        self.first = first
        self.last = last
        self.email = first + '.' + last + '@inventory.com'
    def fullname(self):
        return (self.first, self.last)
class Food:
    def __init__(self, snacks, vegetables, fruits, meat, cereal):
        self.snacks = snacks
        self.vegetables = vegetables
        self.fruits = fruits
        self.meat = meat
        self.cereal = cereal
class Healthcare:
    def __init__(self, deodorants, hair_products, skin_products, vitamins, first_aid):
        self.deodorants = deodorants
        self.hair_products = hair_products
        self.skin_products = skin_products
        self.vitamins = vitamins
        self.first_aid = first_aid
class Drinks:
    def __init__(self, cold_drinks, hot_drinks, cider, alcohol, dairy):
        self.cold_drinks = cold_drinks
        self.hot_drinks = hot_drinks
        self.cider = cider
        self.alcohol = alcohol
        self.dairy = dairy
class Essentials:
    def __init__(self, toilet_rolls, paper_towels, trash_bags, laundry_detergent, broom):
        self.toilet_rolls = toilet_rolls
        self.paper_towels = paper_towels
        self.trash_bags = trash_bags
        self.laundry_detergent = laundry_detergent
        self.broom = broom

PYCHARM MODULE_1:

import Grocer_Inventory_System
print ("Second module's name: {}".format(__name__))

#This module will entail the coding relating to the class of Employees, class of Food, the class of Healthcare and all their functions.
#This will help in more efficient, clean and uncluttered coding.

PYCHARM MODULE_2:

import Grocer_Inventory_System
print ("Second module's name: {}".format(__name__))

#This module will entail the coding relating to the class of Essentials, the class of Drinks and all their functions.
#This will help in more efficient, clean and uncluttered coding.
