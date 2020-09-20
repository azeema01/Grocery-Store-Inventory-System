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

import datetime
if __name__ == '__main__':
    print('Run Directly')
else:
    print('Run From Import')

#class of emplyees and there credentials that will be ued as logins.
class Employees:
    def __init__(self, first, last):
        self.first = first
        self.last = last

#class for food items so they are differentiated and can be used for specefic implementations relating to food products.
class Food:
    def __init__(self, snacks, vegetables, fruits, meat, cereal):
        self.snacks = snacks
        self.vegetables = vegetables
        self.fruits = fruits
        self.meat = meat
        self.cereal = cereal
#I will be using dictionaries to store information regarding the items and the amount available in stock throughout the code as it makes it easy to record the key and the value.
snacks = {"doritos": 10, "cheetos": 10, "snickers": 10}
vegetables = {"onion": 10, "tomato": 10, "potato": 10}
fruits = {"orange": 10, "banana": 10, "peach": 10}
meat = {"chicken": 10, "beef": 10, "bacon": 10}
cereal = {"coco puffs": 10, "weet bix": 10, "oats": 10}

#class for healthcare items so they are differentiated and can be used for specefic implementations relating to healthcare products.
class Healthcare:
    def __init__(self, deodorants, hair_products, skin_products, vitamins, first_aid):
        self.deodorants = deodorants
        self.hair_products = hair_products
        self.skin_products = skin_products
        self.vitamins = vitamins
        self.first_aid = first_aid
#I will be using dictionaries to store information regarding the items and the amount available in stock throughout the code as it makes it easy to record the key and the value.
deodorants = {"adidas": 10, "play boy": 10, "nike": 10}
hair_products = {"oil": 10, "shampoo": 10, "dye": 10}
skin_products = {"moisturizer": 10, "cream": 10}
vitamins = {"vitaminsA": 10, "vitaminsB": 10, "calcium": 10}
first_aid = {"bandaid": 10, "cotton": 10, "disinfectant": 10}

#class for drinks so they are differentiated and can be used for specefic implementations relating to drinks.
class Drinks:
    def __init__(self, cold_drinks, hot_drinks, cider, alcohol, dairy):
        self.cold_drinks = cold_drinks
        self.hot_drinks = hot_drinks
        self.cider = cider
        self.alcohol = alcohol
        self.dairy = dairy
#I will be using dictionaries to store information regarding the items and the amount available in stock throughout the code as it makes it easy to record the key and the value.
cold_drinks = {"coke": 10, "fanta": 10, "v": 10}
hot_drinks = {"coffee": 10, "tea": 10, "hot chocolate": 10}
cider = {"apple cider": 10, "vinegar": 10, "lime cider": 10}
alcohol = {"beer": 10, "wine": 10, "breezer": 10}
dairy = {"milk": 10, "cream": 10}

#class for essential household items so they are differentiated and can be used for specefic implementations relating to these essential household products.
class Essentials:
    def __init__(self, toilet_rolls, paper_towels, trash_bags, laundry_detergent, broom):
        self.toilet_rolls = toilet_rolls
        self.paper_towels = paper_towels
        self.trash_bags = trash_bags
        self.laundry_detergent = laundry_detergent
        self.broom = broom
#I will be using dictionaries to store information regarding the items and the amount available in stock throughout the code as it makes it easy to record the key and the value.
toilet_rolls = {"4 ply": 10, "8 ply": 10, "12 ply": 10}
paper_towels = {"big": 10, "medium": 10, "tissues": 10}
trash_bags = {"large": 10, "extra large": 10}
laundry_detergent = {"small": 10, "bucket": 10}
broom = {"cotton mop": 10}

#employee login
emp_1 = Employees('Tommy', 'Shelby')
emp_2 = Employees('Arthur', 'Shelby')

#list of employees.
#I have used lists as one of the data structures because it is super handy and easy to call in and use further in loops and different modules.
empList = [emp_1, emp_2]

who = input('Enter employee name:')

#recording which employee logged in and when.
if who == '{} {}'.format(emp_1.first, emp_1.last) or who == '{} {}'.format(emp_2.first, emp_2.last):
    print('Hello')
    print('You have been logged in and authorized to continue!')
    print(datetime.datetime.now())
    #checking inventory.
    stock = input('\nDo you want to check stock of products? (y or n)')
    if stock == 'y':
        print('Snacks:', snacks)
        print('Vegetables:', vegetables)
        print('Fruits:', fruits)
        print('Meat:', meat)
        print('Cereal:', cereal)
        print('Deodorants:', deodorants)
        print('Hair Products:', hair_products)
        print('Skin Products:', skin_products)
        print('Vitamins:', vitamins)
        print('First Aid:', first_aid)
        print('Cold Drinks:', cold_drinks)
        print('Hot Drinks:', hot_drinks)
        print('Cider:', cider)
        print('Alcohol:', alcohol)
        print('Dairy:', dairy)
        print('Toilet Rolls:', toilet_rolls)
        print('Paper Towels:', paper_towels)
        print('Trash Bags:', trash_bags)
        print('Laundry Detergents:', laundry_detergent)
        print('Brooms:', broom)

    #other features soon to come.
    else:
        print('Okay, our servers are under maintenance so other functions may not be accessible at this moment.')
        print('You have been logged out, have a good day!')
        print(datetime.datetime.now())

#wrong employee login.
if who != '{} {}'.format(emp_1.first, emp_1.last) and who != '{} {}'.format(emp_2.first, emp_2.last):
    print('Invalid employee name. Restart the program and try again with a valid employee name!')

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
