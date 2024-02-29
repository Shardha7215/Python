# Python
Programming in Python
Write python program to print first letter of your name 
a) Example: Peter
               *      *
               *             *
               *              *
               *      *
               *
               *
               *
b) Print your name by using for loop

c) check the user name is palindrome or not

Ans.
str_pattern = "\nS" 
for Row in range(0, 7):    
    for Col in range(0, 7):     
        if ((Row == 0 or Row == 3 or Row == 6) and (Col > 0 and Col < 5)) or \
           (Col == 1 and (Row == 1 or Row == 2)) or \
           (Col == 5 and (Row == 0 or Row == 4 or Row == 5)) or \
           (Col == 4 and (Row == 1 or Row == 3 or Row == 5)):
            str_pattern += " * "    
        else:      
            str_pattern += "  "    
    str_pattern += "\n"    

print(str_pattern)

username = input("Enter the username: ")
s = username.lower() 
s = ''.join(char for char in s if char.isalnum())

if s == s[::-1]:
    print("The username is a palindrome.")
else:
    print("The username is not a palindrome.")

