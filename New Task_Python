1. Write python program to check Aadhaar card number is valid or not. If valid, display his details like name, company name.
2. Given a list of N numbers, use a single list comprehension to produce a new list that only contains:
a) Even numbers
b) from elements in the original list that even indices
c) Print the Occurrences of an individual element
If the list[2] contains a value that is even, that value should be included in the new list,
since it is also at an index (i.e. 2) in the original list. If the list[3] contains an even
number, that number should not be included in the list since it is at an odd index in the
original list.
3.Write python program to generate basic online shopping cart. This program will allow users:
a) to add items to their cart,
b) view their cart,
c) calculate the total price.


ANSWER:-
1)
import re

aadhaar_details = {
    "123456789012": {"name": "Piyush", "company": "ABC Corporation"},
    "234567890123": {"name": "Pratham", "company": "XYZ Enterprises"}
}

def validate_aadhaar(aadhaar_number):
    if re.match(r"^\d{12}$", aadhaar_number):
        if aadhaar_number in aadhaar_details:
            return True
    return False

def display_aadhaar_details(aadhaar_number):
    if validate_aadhaar(aadhaar_number):
        details = aadhaar_details[aadhaar_number]
        print("Name:", details["name"])
        print("Company:", details["company"])
    else:
        print("Invalid Aadhaar number or details not found")

aadhaar_number = input("Enter Aadhaar number: ")
display_aadhaar_details(aadhaar_number)
2)
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
even_numbers = [num for num in numbers if num % 2 == 0]
even_indices_even_numbers = [numbers[i] for i in range(len(numbers)) if i % 2 == 0 and numbers[i] % 2 == 0]
occurrences = {num: numbers.count(num) for num in set(numbers)}

print("Even numbers:", even_numbers)
print("Even numbers from elements at even indices:", even_indices_even_numbers)
print("Occurrences of individual elements:", occurrences)
3)
class ShoppingCart:
    def _init_(self):
        self.cart = {}

    def add_item(self, item, price):
        if item in self.cart:
            self.cart[item] += price
        else:
            self.cart[item] = price

    def view_cart(self):
        if self.cart:
            print("Items in Cart:")
            for item, price in self.cart.items():
                print(item, ":", price)
        else:
            print("Cart is empty")

    def calculate_total(self):
        total = sum(self.cart.values())
        print("Total Price:", total)

cart = ShoppingCart()

while True:
    print("\n1. Add item to cart")
    print("2. View cart")
    print("3. Calculate total")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == '1':
        item = input("Enter item name: ")
        price = float(input("Enter item price: "))
        cart.add_item(item, price)
    elif choice == '2':
        cart.view_cart()
    elif choice == '3':
        cart.calculate_total()
    elif choice == '4':
        print("Exiting program...")
        break
    else:
        print("Invalid choice")
\]
