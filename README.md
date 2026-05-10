# Python Basic Operations Notebook

This repository contains Python notebook practice programs for learning basic Python programming concepts.

🎯 Learning Objectives

By completing this notebook, you will understand:

How to take user input and display output

Basic arithmetic and logical operations

String manipulation and indexing

Conditional logic (if-else statements)

Loop structures (for loops)

Type conversion (int, float, string)

List operations and methods

Mathematical calculations and formulas

📚 Program 1: Cube Root Calculation
Concept: Mathematical operations and exponentiation
python
# Taking input from user
number = float(input("Enter a number: "))

# Calculating cube root using exponentiation
cube_root = number ** (1/3)

# Displaying result with 2 decimal places
print(f"Cube root of {number} is {cube_root:.2f}")
Key Learning Points:
** operator for exponentiation (power)

(1/3) as exponent gives cube root

float() converts input to decimal number

:.2f formats output to 2 decimal places

Mathematical Formula:
text
cube_root = number^(1/3)
Example: 27^(1/3) = 3
Real-world Applications:
Volume calculations in 3D graphics

Scaling objects in computer games

Engineering calculations

📚 Program 2: String Letter Extraction
Concept: String indexing and manipulation
python
# Sample strings
first_name = "Python"
last_name = "Programming"

# String indexing (0-based indexing)
# Position:    0    1    2    3    4    5
# Characters:  P    y    t    h    o    n

third_letter = first_name[2]   # Gets 't'
fourth_letter = last_name[3]    # Gets 'g'

print(f"Character at index 2: {third_letter}")
print(f"Character at index 3: {fourth_letter}")

# Checking string length
length = len(first_name)
print(f"String length: {length}")
Key Learning Points:
Python uses 0-based indexing (first character = index 0)

len() function returns string length

Strings are immutable (cannot be changed after creation)

Index [n] gets character at position n

Index Reference Table:
Position	Index	Example: "Python"
1st char	[0]	'P'
2nd char	[1]	'y'
3rd char	[2]	't'
4th char	[3]	'h'
5th char	[4]	'o'
6th char	[5]	'n'
Last char	[-1]	'n'
Real-world Applications:
Text preprocessing for Natural Language Processing

Data validation and cleaning

Password strength checking

📚 Program 3: Name Separation
Concept: String methods and list operations
python
# Taking full name as input
full_name = input("Enter full name: ")

# Splitting string into list using space as delimiter
name_parts = full_name.split()  # Returns ['First', 'Last']

# Extracting individual parts
first_name = name_parts[0]
last_name = name_parts[1]

print(f"First name: {first_name}")
print(f"Last name: {last_name}")
Alternative method with multiple words:
python
full_name = "Mr. John Michael Doe"
name_parts = full_name.split()  # ['Mr.', 'John', 'Michael', 'Doe']

title = name_parts[0]      # 'Mr.'
first = name_parts[1]       # 'John'
middle = name_parts[2]      # 'Michael'
last = name_parts[3]        # 'Doe'
Key Learning Points:
.split() breaks string into list using spaces

List indexing [0] gets first element

Multiple variables can be assigned from a list

Default delimiter is space, can be customized: .split(',')

Common Delimiters Examples:
python
csv_data = "apple,banana,orange"
fruits = csv_data.split(',')  # ['apple', 'banana', 'orange']

date = "2024-05-20"
parts = date.split('-')  # ['2024', '05', '20']
Real-world Applications:
Parsing CSV files

Processing form data

Log file analysis

Command-line argument parsing

📚 Program 4: Average of Five Numbers
Concept: Lists, loops, and arithmetic operations
python
# Method 1: Using individual variables
num1 = float(input("Enter number 1: "))
num2 = float(input("Enter number 2: "))
num3 = float(input("Enter number 3: "))
num4 = float(input("Enter number 4: "))
num5 = float(input("Enter number 5: "))

average = (num1 + num2 + num3 + num4 + num5) / 5
print(f"Average: {average:.2f}")
python
# Method 2: Using list and loop (more efficient)
numbers = []

for i in range(5):
    num = float(input(f"Enter number {i+1}: "))
    numbers.append(num)

average = sum(numbers) / len(numbers)
print(f"Average: {average:.2f}")
Key Learning Points:
float() converts input to decimal number

sum() calculates total of all elements

len() returns number of elements in list

range(5) generates numbers 0,1,2,3,4

f-string {i+1} for user-friendly counting

Mathematical Formula:
text
Average = (Sum of all numbers) / (Count of numbers)

Example: (10 + 20 + 30 + 40 + 50) / 5 = 150 / 5 = 30
Real-world Applications:
Calculating student grades

Finding average temperature

Analyzing sensor data

Sports statistics (batting average, etc.)

📚 Program 5: Temperature Conversion
Concept: Mathematical formulas and floating-point arithmetic
Fahrenheit to Celsius:
python
fahrenheit = float(input("Enter temperature in Fahrenheit: "))

# Conversion formula
celsius = (fahrenheit - 32) * 5 / 9

print(f"{fahrenheit}°F = {celsius:.2f}°C")
Celsius to Fahrenheit:
python
celsius = float(input("Enter temperature in Celsius: "))

# Conversion formula
fahrenheit = (celsius * 9 / 5) + 32

print(f"{celsius}°C = {fahrenheit:.2f}°F")
Complete bidirectional converter:
python
print("Temperature Converter")
print("1. Fahrenheit to Celsius")
print("2. Celsius to Fahrenheit")

choice = input("Choose (1/2): ")
temp = float(input("Enter temperature: "))

if choice == "1":
    result = (temp - 32) * 5 / 9
    print(f"{temp}°F = {result:.2f}°C")
elif choice == "2":
    result = (temp * 9 / 5) + 32
    print(f"{temp}°C = {result:.2f}°F")
Key Learning Points:
Mathematical formulas require correct operator precedence

Parentheses ensure proper calculation order

Different formulas for different conversions

Temperature Reference Points:
Scale	Freezing	Body Temp	Boiling
Celsius	0°C	37°C	100°C
Fahrenheit	32°F	98.6°F	212°F
Real-world Applications:
Weather applications

Cooking and baking

Scientific experiments

Medical thermometers

HVAC systems

📚 Program 6: Even or Odd Number
Concept: Conditional statements and modulo operator
python
number = int(input("Enter a number: "))

# Modulo operator (%) gives remainder after division
if number % 2 == 0:
    print(f"{number} is an even number")
else:
    print(f"{number} is an odd number")
Modulo Operator Explained:
Number	Division	Quotient	Remainder	Even/Odd
10 ÷ 2	10 / 2 = 5	5	10 % 2 = 0	Even
7 ÷ 2	7 / 2 = 3.5	3	7 % 2 = 1	Odd
100 ÷ 2	100 / 2 = 50	50	100 % 2 = 0	Even
99 ÷ 2	99 / 2 = 49.5	49	99 % 2 = 1	Odd
Extended version with multiple checks:
python
number = int(input("Enter a number: "))

# Check if number is even or odd
if number % 2 == 0:
    print(f"{number} is EVEN")
    
    # Additional check for even numbers
    if number % 4 == 0:
        print(f"{number} is divisible by 4")
else:
    print(f"{number} is ODD")
    
    # Additional check for odd numbers
    if number % 3 == 0:
        print(f"{number} is divisible by 3")
Key Learning Points:
% (modulo) returns remainder after division

== compares equality

if-else creates conditional branches

Even numbers: remainder when divided by 2 is 0

Odd numbers: remainder when divided by 2 is 1

Real-world Applications:
Alternating patterns in UI (zebra striping)

Load balancing (distribute tasks)

Game logic (turn-based systems)

Data validation

Cryptography basics

📚 Program 7: Multiplication Table
Concept: Loops and repeated operations
python
number = int(input("Enter a number: "))

# Method 1: Simple multiplication
for i in range(1, 11):
    print(number * i)
python
# Method 2: Formatted output
number = int(input("Enter a number: "))

print(f"\nMultiplication Table of {number}")
print("-" * 25)

for i in range(1, 11):
    print(f"{number} × {i:2} = {number * i:3}")
python
# Method 3: Custom range table
number = int(input("Enter a number: "))
start = int(input("Start from: "))
end = int(input("End at: "))

print(f"\nMultiplication Table of {number} (from {start} to {end})")
print("-" * 35)

for i in range(start, end + 1):
    print(f"{number} × {i:2} = {number * i:4}")
Output Example:
text
Enter a number: 5

Multiplication Table of 5
-------------------------
5 ×  1 =   5
5 ×  2 =  10
5 ×  3 =  15
5 ×  4 =  20
5 ×  5 =  25
5 ×  6 =  30
5 ×  7 =  35
5 ×  8 =  40
5 ×  9 =  45
5 × 10 =  50

