# my-python-assignment
assignment1

print("Hello My Name Is: ")
Hello My Name Is: 
print("saimon rai")
saimon rai
print(3 + 3)
6
#print("Set A - Basic Pthon Programs")
#print("1.Write a python program that simulates a basic calculator, performing addition, subtraction, multiplication, and divison.")


#Basic calculator
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
operation = input("ENter operation (+, -, *, /): ")

if operation == '+':
    print("Result:", num1 + num2)
elif operation == '-':
    print("Result:", num1 - num2)
elif operation == '*':
    print("Result:", num1 * num2)
elif operation == '/':
    if num2 != 0:
        print("Result:", num1 / num2)
    else:
        print("Error:Division by Zaero!")
else:
    print("Invalid operation")
Result: 6.0
#print("2) Write a Python program that converts a given decimal number to its binary equivalent.")
#print("2.Decimal to Binary")

#Decimal to binary
decimal = int(input("Enter a decimal number: "))
print("Binary equivalent:", bin(decimal)[2:])
Binary equivalent: 1
#3) Write a Python program that asks for the user's age and then prints a message stating whether the user is a minor, an adult, or a senior

#Age Classification
age = int(input("Enter your age: "))
if age < 18:
    print("You are a minor.")
elif age < 60:
    print("You are an adult.")
else:
    print("You aare a senior.")
You aare a senior.
#4) Write a Python program to swap the values of two variables without using a third variable.

#Swap without third vaiable
a = int (input("Enter first number: "))
b = int(input("Enter second number: "))
a, b = b, a
print("After swapping: a=", a, ", b =", b)
After swapping: a= 4 , b = 2
#5) Write a Python program to print the first 10 numbers of the Fibonacci series.

#Fibonacci Series
a, b = 0, 1
for _ in range(10):
    print(a, end=" ")
    a, b = b, a + b
0 1 1 2 3 5 8 13 21 34 
#6) Write a Python program to check if a given number is prime or not.

#Prime Number Check
num = int(input("Enter a number: "))
if num > 1:
    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            print("Not Prime")
            break
    else:
        print("Prime")
else:
    print("Not Prime")
    
Prime
#7) Write a Python program that takes three numbers as input and checks if the third number is the sum of the first two numbers using logical operators.

#Logical Operators Check
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))
if c == a + b:
    print("Third number is the sum of the first two.")
else:
    print("Third number is NOT the sum of the first two.")
Third number is the sum of the first two.
#8) Write a Python program that imports a custom module you created with a function that returns the factorial of a number.

#Custom Module-Factorial
#factorial_module.py
# factorial_module.py

# factorial_module.py

def factorial(n):
    """Calculate the factorial of a number."""
    if n < 0:
        raise ValueError("Factorial is not defined for negative numbers.")
    if n == 0 or n == 1:
        return 1
    result = 1
    for i in range(2, n + 1):
        result *= i
    return result

# main_program.py

# Import the custom module

def main():
    try:
        # Input from the user
        num = int(input("Enter a number to calculate its factorial: "))
        # Call the factorial function
        result = factorial(num)
        print(f"The factorial of {num} is {result}.")
    except ValueError as e:
        print(f"Error: {e}")

if __name__ == "__main__":
    main()
The factorial of 5 is 120.
#9) Write a Python program that takes two numbers as input and performs division, handling the case where the divisor is zero.

#Division with exception Handling
try:
    num1 = float(input("Enter numerator: "))
    num2 = float(input("Enter denominator: "))
    result = a / b
    print("Result:", result)
except ZeroDivisionError:
    print("Error: Cannot divide by zero!")
else:
    print(f"The result of {num1} / {num2} is {Result}")
Error: Cannot divide by zero!
#10) Write a Python function that takes a list of numbers and returns the maximum value in the list. 

#Max in list
def find_max(numbers):
    return max(numbers)
nums =[3, 7, 2, 9, 5]
print("Max value:", find_max(nums))
Max value: 9
#11) Write a Python function that takes a name and an optional age parameter and prints a greeting. If the age is not provided, it should default to 25

#Greeting function
def greet(name, age=25):
    print(F"Hello {name}, your are {age} years old.")

greet("Saimon")
greet("Samon", 30)
Hello Saimon, your are 25 years old.
Hello Samon, your are 30 years old.
#12) Write a Python program to count the number of vowels in a given string.

#Count Vowels
string = input("Enter a string: ").lower()
count = sum(1 for char in string if char in 'aeiou')
print("Number of vowels:", count)
Number of vowels: 2
#13) Write a Python program that prints a multiplication table up to (numberx10).

#Multiplication Table
n = int(input("Enter a number: "))
for i in range(1, 11):
    print(f"{n} x {i} = {n * i}")
10 x 1 = 10
10 x 2 = 20
10 x 3 = 30
10 x 4 = 40
10 x 5 = 50
10 x 6 = 60
10 x 7 = 70
10 x 8 = 80
10 x 9 = 90
10 x 10 = 100
#14) Write a Python program to print a right-angled triangle of '*' with a given number of rows. For example, if the number of rows is 5, the output should be:
#*
#** 
#*** 
#**** 
#*****

#Right-angled triangle
rows = int(input("Enter number of rows: "))
for i in range(1, rows + 1):
    print("*" * i)
*
**
***
****
*****
#15) Write a Python program to print a pyramid of '*' with a given number of rows. For example, if the number of rows is 5, the output should be:
   # *
   #*** 
  #***** 
 #******* 
#*********

#Pyramid Pattern
rows = int(input("Enter number of rows: "))
for i in range(rows):
    print(" " * (rows - i - 1) + "*" * (2 * i  +1))
        *
       ***
      *****
     *******
    *********
   ***********
  *************
 ***************
*****************
#1) Given an integer x, return true if x is a palindrome, and false otherwise. (LeetCode: Palindrome Number)

#Palindrome number

def is_Palindrome(x: int) -> bool:
    if x < 0:
        return False
    return str(x) == str(x)[::-1]

num = int(input("Enter a number: "))
if is_palindrome(num):
    print(f"{num} is a palimndrome.")
else:
    print(f"{num} is not a palindrome.")
1 is a palimndrome.
#2) Given a non-empty array of integers nums, every element appears twice except for one. Find that single one. (LeetCode: Single Number)

#single number

def single_number(nums):
    result = 0
    for num in nums:
        result ^= num
    return result

#print(single_number([4,1,2,1,2])) # 4

nums = list(map(int, input("Enter numbers separated by space: ").split()))
print(f"The single number is: {single_number(nums)}")
The single number is: 4
#3) Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice. You can return the answer in any order. (LeetCode: Two Sum)

#TwoSum

def twoSum(nums, target):
    num_map = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in num_map:
            return [num_map[complement], i]
        num_map[num] = i

print(twoSum([2,7,11,15], 9))
[0, 1]
#4) Write an algorithm to determine if a number n is happy. (LeetCode: Happy Number)

#Happy number

def isHappy(n):
    seen = set()
    while n != 1 and n not in seen:
        seen.add(n)
        n = sum(int(ch) ** 2 for ch in str(n))
    return n == 1

print(isHappy(19))
True
#5) Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct. (LeetCode: Contains Duplicate)


#containss duplicate

def containsDuplicate(nums):
 return len(nums) != len(set(nums))
print(containsDuplicate([1,2,3,1]))
True
 
