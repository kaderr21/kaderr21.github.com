---
layout: default
title: Python coding
description: This page is to show my random projects and my development.
---


[Link to the main page](./index.md).


# Progress
This is currently what I have learnt, I will try to update this page frequently with everything that I learn.

## Test projects
### First project

```python
try:
    number1 = int(input("Enter 1st number: "))
    number2 = int(input("Enter 2nd number: "))
    
    if number1 > number2:
        print("The first number is greater!")
    elif number2 > number1:
            print("The second number is greater!")
            
    else:
        print("They're the same!")
except ValueError:
    print("Please enter valid numbers!")
```
### Project number two
```python
try:
    number1 = int(input("Enter 1st number: "))
    number2 = int(input("Enter 2nd number: "))
    number3 = int(input("Enter 3rd number: "))

    if number1 == number2 == number3:
        print("All numbers are equal!")
    elif number1 == number2 > number3:
        print("Number 1 and number 2 are the largest numbers!")
    elif number1 < number2 == number3:
        print("Number 2 and number 3 are the largest numbers!")
    elif number1 == number3 > number2:
        print("Number 1 and number 3 are the largest numbers!")
    elif number1 > number2 and number1 > number3:
        print("Number 1 is the largest!")
    elif number1 < number2 and number2 > number3:
        print("Number 2 is the largest!")
    elif number3 > number1 and number2 < number3:
        print("Number 3 is the largest!")
except ValueError:
    print("Please input valid numbers :(")
```
### Project number three
```python
try:
    grade = int(input("Input your grade here: "))

    if grade > 100 or grade < 0:
        print("Input a valid grade")
    elif grade >= 90:
        print("Your grade is: A")
    elif grade >= 80:
        print("Your grade is: B") 
    elif grade >= 70:
        print("Your grade is: C")
    elif grade >= 60:
        print("Your grade is: D")
    else:
        print("You didn't pass, better luck next time!")
except ValueError:
    print("Input a valid number!")
```
### Project number four
```python
while True:
    user_input = input("Enter a number or type 'quit' to exit!: ")

    if user_input == 'quit':
        print("Bye!")
        break

    try:
        number = int(user_input)
        if number == 0:
            print("0 is neither odd or even")
        elif number % 2 == 0:
            print(f"{number} is an even number!")
        else: 
            print(f"{number} is an odd number!")
    except ValueError:
        print("Error: Please input a valid number!")
```
### Project number five (Favorite color program)
```python
print("Welcome to my Favorite color program!")

favorite_colors = []
while True:
    favorite_color = input("What is your favorite color? ").strip()
    if not favorite_color:
        print("Please input a valid color!")
        continue
    
    favorite_colors.append(favorite_color.capitalize())
    print(f"Wow, {favorite_color.capitalize()} is a great color! ")
    
    repeat =  input("Do you have another favorite color? (Yes/no)").lower()
    if repeat not in ['yes', 'y']:
        print("Here are all the colors you shared: ")
        print(", ".join(favorite_colors))
        print(f"Okay then! Enjoy having {favorite_colors[-1]} as your favorite color! Goodbye :)")
        break

```
### Project number six (Number guessing game)
```python
import random

print("Welcome to Maciejs guess the number game!")

secret_number = random.randint(1, 10)

while True:
    try:

        guess = int(input("Enter your guess (1-10): "))

        if guess == secret_number:
            print("Congratulations, you guessed the number!")
            break
        elif guess < secret_number:
            print("Too low, guess again!")
        else:
            print("Too high, guess again!")
        
    except ValueError:
        print("Invalid input!! Please enter a valid number!")
```

## Actually useful programs

### Calculator program with options.
```python
print("Welcome to Maciejs python calculator!")

while True:
    number1 = float(input("Enter the first number: "))
    number2 = float(input("Enter the second number: "))

    print("Choose your operation: ")
    print("1 = Addition")
    print("2 = Subtraction")
    print("3 = Multiplication")
    print("4 = Division")
    choice = int(input("Enter your choice! (1/2/3/4)"))

    if choice == 1:
        result = number1 + number2
        print(f"The result of the addition is: {result}")
    elif choice == 2:
        result = number1 - number2
        print(f"The result of the subtraction is: {result}")
    elif choice == 3:
        result = number1 * number2
        print(f"The result of the multiplication is: {result}")
    elif choice == 4:
        if number2 == 0:
            print("Division by zero is not possible!")
        else:
            result = number1 / number2
            print(f"The result of the division is: {result}")
    else:
        print("Invalid choice! Input 1, 2, 3 or 4")

    repeat = input("Do you want to perform another calculation? (Yes/No)").lower()
    if repeat != 'yes':
        print("Thank you for using Maciejs python calculator! Have a nice day/evening/night!")
        break
```
### Number list program with memory functions
```python
print("Welcome to Maciejs number list program!")

numbers_list = []

while True:
    print("\nChoose an Option: ")
    print("1. Add a number to the list")
    print("2. Remove a number from the list")
    print("3. Find the largest number in the list")
    print("4. Find the smallest number in the list")
    print("5. Calculate the average of the numbers in the list")
    print("6. Display all the numbers in the list")
    print("7. Exit")

    try:
        choice = int(input("Enter your choice! (1,2,3,4,5,6,7): "))
    except ValueError:
        print("Invalid action! Please input a valid number between 1 and 7! ")
        continue

    if choice == 1:

        try: 
            number = float(input("Enter a number to add to the list: "))
            numbers_list.append(number)
            print(f"The number {number} has been added to the list.")
        except ValueError:
            print("Invalid input! Please enter a valid number!")
    
    elif choice == 2:

        try: 
            number = float(input("Enter a number to delete from the list: "))
            numbers_list.remove(number)
            print (f"The number {number} has been removed from the list")
        except ValueError:
            print("Invalid input! Please enter a valid number!")
    
    elif choice == 3:

        if numbers_list:
            largest = max(numbers_list)
            print(f"Largest number in the list is: {largest}")
        else:
            print("The list is empty, first provide a number with option 1!")
    
    elif choice == 4:

        if numbers_list:
            smallest = min(numbers_list)
            print(f"Smallest number in the list is: {Smallest}")
        else:
            print("The list is empty, first provide a number with option 1")
    
    elif choice == 5:

        if numbers_list:
            average = sum(numbers_list) / len(numbers_list)
            print(f"The average of the numbers list is: {average}")
        else:
            print("The list is empty, first provide a number with option 1")

    elif choice == 6:

        if numbers_list:
            print("The numbers in the list are: ", numbers_list)
        else:
            print("The list is empty, first provide a number with option 1")

    elif choice == 7:

        print("Thank you for using Maciejs number list! Goodbye!")
        break

    else:
        print("Invalid choice! Please choose option between 1 and 7!")

    repeat = input("Do you want to perform another action? (Yes/no)").lower()
    if repeat != 'yes':
        print("Thank you for using Maciejs number list! Goodbye!")
        break
```
### Shopping list with a save function
```python
shopping_list = {}


def add_item():
    item = input("Enter the item to add: ")
    try:
        price = float(input(f"Enter the price of {item}: €"))
        shopping_list[item] = price
        print(f"{item} has been added to the list with a price of €{price:.2f}. ")
    except ValueError:
        print("Invalid price, please enter a number!")

def remove_item():
    if not shopping_list:
        print("Shopping list is empty, nothing to remove!")
        return

    print("Here is your shopping list: ")
    for i, (item, price) in enumerate(shopping_list.items(), start=1):
        print(f"{i}. {item} - €{price:.2f}")
    
    while True:
        try:
            choice = int(input("Enter the number of the item to remove: "))
            if 1 <= choice <= len(shopping_list):
                removed_item = list(shopping_list.keys())[choice - 1]
                shopping_list.pop(removed_item)
                print(f"{removed_item} has been deleted from the list!")
                break
            else:
                print("Invalid number. Please choose a valid number!")
        except ValueError:
            print("Invalid input, please enter a number!")

def view_list():
    if shopping_list:
        print("Your shopping list contains: ")
        for i, (item, price) in enumerate(shopping_list.items(), start=1):
            print(f"{i}. {item} - €{price:.2f}")
    else: 
        print("Your shopping list is empty!")

def total_price():
    if shopping_list:
        total = sum(shopping_list.values())
        print(f"The total price of your shopping cart is: €{total:.2f}")
    else:
        print("Your shopping cart is empty!")

def save_list():
    try:

        with open("shopping_list.txt", "w") as file:
            for item, price in shopping_list.items():
                file.write(f"{item}: €{price:.2f}\n")
        print("Shopping list has been saved to 'shopping_list.txt'.")
    except Exception as e:
        print(f"An error occurred while saving the list: {e}")

def load_list():
    try:
        with open("shopping_list.txt", "r") as file:
            for line in file:
                try:
                    item, price = line.split(": €")
                    shopping_list[item] = float(price.strip())
                except ValueError:
                    print(f"Skipping invalid line: {line.strip()}")
        print("Shopping list has been loaded.")
    except FileNotFoundError:
        print("No saved shopping list has been found.")
    except Exception as e:
        print(f"An error has occurred while loading the list: {e}")

def main():

    load_list()


    while True:
        print("\nGrocery Store Helper")
        print("1. Add item")
        print("2. Remove item")
        print("3. View list")
        print("4. Calculate total")
        print("5. Save list")
        print("6. Exit")
        choice = input("Choose an option between (1-6): ")

        if choice == '1':
            add_item()
        elif choice == '2':
            remove_item()
        elif choice == '3':
            view_list()
        elif choice == '4':
            total_price()
        elif choice == '5':
            save_list()
        elif choice == '6':
            print("Goodbye!")
            break
        else:
            print("Invalid choice! Choose between 1, 2, 3, 4, 5 or 6.")

main()
```


# Summary ish
This is what I have currently taught myself, I use chatgpt to give me "assignments" and I try to do my best. If I get stuck, I ask chatgpt to give me a skeleton code and either improve upon it or use it as a template.

***
