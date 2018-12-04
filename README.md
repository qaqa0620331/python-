# 教科書:Python程式設計入門指南

```
CH01　電腦、程式及Python概述
CH02　基本程式設計
CH03　數學函式、字元與字串
CH04　選擇
CH05　迴圈
CH06　函式

CH07　物件與類別
CH08　再論字串與特殊方法

CH09　GUI程式設計使用Tkinter

CH10　串列
CH11　多維串列

CH12　繼承與多型

CH13　檔案與異常處理

CH14　數組、集合及詞典

CH15　遞迴
```

# CH01　電腦、程式及Python概述
```
1.1 Welcom.py
# Display two messages
print("Welcome to Python")
print("Python is fun")
```
```
1.2 WelcomeWithThreeMessages.py
# Display three messages
print("Welcome to Python")
print("Python is fun")
print("Problem Driven")  
```
```
1.3 ComputeExpression.py
# Compute expression
print((10.5 + 2 * 3) / (45 – 3.5))
```
```
1.4 ShowLogicErrors.py
# Convert Fahrenheit to Celsius
print("Fahrenheit 35 is Celsius degree ")
print(5 / 9 * (35 - 32))
```
```
1.5 OlympicSymbol.py
import turtle

turtle.color("blue")
turtle.penup()
turtle.goto(-110, -25)
turtle.pendown()
turtle.circle(45)

turtle.color("black")
turtle.penup()
turtle.goto(0, -25)
turtle.pendown()
turtle.circle(45)

turtle.color("red")
turtle.penup()
turtle.goto(110, -25)
turtle.pendown()
turtle.circle(45)

turtle.color("yellow")
turtle.penup()
turtle.goto(-55, -75)
turtle.pendown()
turtle.circle(45)

turtle.color("green")
turtle.penup()
turtle.goto(55, -75)
turtle.pendown()
turtle.circle(45)

turtle.done() 
```

# CH02　基本程式設計

```
2.1 ComputeArea.py
# Assign a radius
radius = 20 # radius is now 20

# Compute area
area = radius * radius * 3.14159

# Display results
print("The area for the circle of radius", radius, "is", area)
```

```
2.2 ComputeAreaWithConsoleInput.py
# Prompt the user to enter a radius
radius = eval(input("Enter a number for radius: "))

# Compute area
area = radius * radius * 3.14159

# Display results
print("The area for the circle of radius", radius, "is", area)

```

```
2.3 ComputeAverage.py
# Prompt the user to enter three numbers
number1, number2, number3 = eval(input("Enter three numbers separated by commas: "))

# Compute average
average = (number1 + number2 + number3) / 3

# Display result
print("The average of", number1, number2, number3, "is", average)

```

```
2.4 ComputeAverageWithSimultaneousAssignment.py
# Prompt the user to enter three numbers
number1, number2, number3 = eval(input(
  "Enter three numbers separated by commas: "))

# Compute average
average = (number1 + number2 + number3) / 3

# Display result
print("The average of", number1, number2, number3,
    "is", average)

```

```
2.5 DisplayTime.py
# Prompt the user for input
seconds = eval(input("Enter an integer for seconds: "))

# Get minutes and remaining seconds
minutes = seconds // 60     # Find minutes in seconds
remainingSeconds = seconds % 60   # Seconds remaining
print(seconds, "seconds is", minutes,  
  "minutes and", remainingSeconds, "seconds")

```

```
2.6 SalesTax.py
# Prompt the user for input
purchaseAmount = eval(input("Enter purchase amount: "))

# Compute sales tax
tax = purchaseAmount * 0.06

# Display tax amount with two digits after decimal point
print("Sales tax is", int(tax * 100) / 100.0)

```

```
2.7 ShowCurrentTime.py
import time

currentTime = time.time() # Get current time

# Obtain the total seconds since midnight, Jan 1, 1970
totalSeconds = int(currentTime)

# Get the current second 
currentSecond = totalSeconds % 60 

# Obtain the total minutes
totalMinutes = totalSeconds // 60 

# Compute the current minute in the hour
currentMinute = totalMinutes % 60

# Obtain the total hours
totalHours = totalMinutes // 60

# Compute the current hour
currentHour = totalHours % 24

# Display results
print("Current time is " + str(currentHour) + ":"
    + str(currentMinute) + ":" + str(currentSecond) + " GMT")
```

```
2.8 ComputeLoan.py
# Enter yearly interest rate
annualInterestRate = eval(input(
  "Enter annual interest rate, e.g., 8.25: "))
monthlyInterestRate = annualInterestRate / 1200

# Enter number of years
numberOfYears = eval(input(
  "Enter number of years as an integer, e.g., 5: "))
    
# Enter loan amount
loanAmount = eval(input("Enter loan amount, e.g., 120000.95: "))
    
# Calculate payment
monthlyPayment = loanAmount * monthlyInterestRate / (1
  - 1 / (1 + monthlyInterestRate) ** (numberOfYears * 12))
totalPayment = monthlyPayment * numberOfYears * 12

# Display results
print("The monthly payment is", int(monthlyPayment * 100) / 100)
print("The total payment is", int(totalPayment * 100) /100)

```

```
2.9 ComputeDistance.py
# Enter the first point with two double values
x1, y1 = eval(input("Enter x1 and y1: "))

# Enter the second point with two double values
x2, y2 = eval(input("Enter x2 and y2: "))
 
# Compute the distance
distance = ((x1 - x2) * (x1 - x2) + (y1 - y2) * (y1 - y2)) ** 0.5
    
print("The distance between the two points is", distance) 

```

```
2.10 ComputeDistanceGraphics.py
import turtle

# Prompt the user for inputing two points
x1, y1 = eval(input("Enter x1 and y1 for Point 1: "))
x2, y2 = eval(input("Enter x2 and y2 for Point 2: "))
              
# Compute the distance
distance = ((x1 - x2) ** 2 + (y1 - y2) ** 2) ** 0.5

# Display two points and the connecting line
turtle.penup()
turtle.goto(x1, y1) # Move to (x1, y1)
turtle.pendown()
turtle.write("Point 1") 
turtle.goto(x2, y2) # draw a line to (x2, y2)
turtle.write("Point 2")

# Move to the center point of the line
turtle.penup()
turtle.goto((x1 + x2) / 2, (y1 + y2) / 2) 
turtle.write(distance)

turtle.done() 

```

# CH03　數學函式、字元與字串

```
3.1 MathFunctions.py
import math # import Math module to use the math functions
 
# Test algebraic functions
print("exp(1.0) =", math.exp(1))
print("log(3.78) =", math.log(math.e))
print("log10(10, 10) =", math.log(10, 10))
print("sqrt(4.0) =", math.sqrt(4.0))
 
# Test trigonometric functions
print("sin(PI / 2) =", math.sin(math.pi / 2))
print("cos(PI / 2) =", math.cos(math.pi / 2))
print("tan(PI / 2) =", math.tan(math.pi / 2))
print("degrees(1.57) =", math.degrees(1.57))
print("radians(90) =", math.radians(90))

```

```
3.2 ComputeAngles.py
import math

x1, y1, x2, y2, x3, y3 = eval(input("Enter six coordinates of three points \
separated by commas like x1, y1, x2, y2, x3, y3: "))
 
a = math.sqrt((x2 - x3) * (x2 - x3) + (y2 - y3) * (y2 - y3))
b = math.sqrt((x1 - x3) * (x1 - x3) + (y1 - y3) * (y1 - y3))
c = math.sqrt((x1 - x2) * (x1 - x2) + (y1 - y2) * (y1 - y2))

A = math.degrees(math.acos((a * a - b * b - c * c) / (-2 * b * c)))
B = math.degrees(math.acos((b * b - a * a - c * c) / (-2 * a * c)))
C = math.degrees(math.acos((c * c - b * b - a * a) / (-2 * a * b)))

print("The three angles are ", round(A * 100) / 100.0,  
    round(B * 100) / 100.0, round(C * 100) / 100.0)

```

```
3.3 DisplayUnicode.py
import turtle

turtle.write("\u6B22\u8FCE \u03b1 \u03b2 \u03b3")

turtle.done() 

```

```
3.4 ComputeChange.py
# Receive the amount 
amount = eval(input("Enter an amount in double, e.g., 11.56: "))

# Convert the amount to cents
remainingAmount = int(amount * 100)

# Find the number of one dollars
numberOfOneDollars = int(remainingAmount / 100)
remainingAmount = int(remainingAmount % 100)

# Find the number of quarters in the remaining amount
numberOfQuarters = int(remainingAmount / 25)
remainingAmount = remainingAmount % 25

# Find the number of dimes in the remaining amount
numberOfDimes = int(remainingAmount / 10)
remainingAmount = remainingAmount % 10

# Find the number of nickels in the remaining amount
numberOfNickels = int(remainingAmount / 5)
remainingAmount = remainingAmount % 5

# Find the number of pennies in the remaining amount
numberOfPennies = remainingAmount

# Display results
print("Your amount", amount, "consists of\n", 
    "\t", numberOfOneDollars, "dollars\n", 
    "\t", numberOfQuarters, "quarters\n",
    "\t", numberOfDimes,  "dimes\n",
    "\t", numberOfNickels, "nickels\n",
    "\t", numberOfPennies, "pennies")


```

```
3.5 SimpleShapes.py
import turtle

turtle.pensize(3)
turtle.penup()
turtle.goto(-200, -50)
turtle.pendown()
turtle.circle(40, steps = 3) # Draw a triangle

turtle.penup()
turtle.goto(-100, -50)
turtle.pendown()
turtle.circle(40, steps = 4) # Draw a square

turtle.penup()
turtle.goto(0, -50)
turtle.pendown()
turtle.circle(40, steps = 5) # Draw a pentagon

turtle.penup()
turtle.goto(100, -50)
turtle.pendown()
turtle.circle(40, steps = 6) # Draw a hexagon

turtle.penup()
turtle.goto(200, -50)
turtle.pendown()
turtle.circle(40) # Draw a circle

turtle.done() 

```

```
3.6 ColorShapes.py
import turtle

turtle.pensize(3) # Set pen thickness to 3 pixels
turtle.penup() # Pull the pen up
turtle.goto(-200, -50)
turtle.pendown() # Pull the pen down
turtle.begin_fill() # Begin to fill color in a shape
turtle.color("red")
turtle.circle(40, steps = 3) # Draw a triangle
turtle.end_fill() # Fill the shape

turtle.penup()
turtle.goto(-100, -50)
turtle.pendown()
turtle.begin_fill() # Begin to fill color in a shape
turtle.color("blue")
turtle.circle(40, steps = 4) # Draw a square
turtle.end_fill() # Fill the shape

turtle.penup()
turtle.goto(0, -50)
turtle.pendown()
turtle.begin_fill() # Begin to fill color in a shape
turtle.color("green")
turtle.circle(40, steps = 5) # Draw a pentagon
turtle.end_fill() # Fill the shape

turtle.penup()
turtle.goto(100, -50)
turtle.pendown()
turtle.begin_fill() # Begin to fill color in a shape
turtle.color("yellow")
turtle.circle(40, steps = 6) # Draw a hexagon
turtle.end_fill() # Fill the shape

turtle.penup()
turtle.goto(200, -50)
turtle.pendown()
turtle.begin_fill() # Begin to fill color in a shape
turtle.color("purple")
turtle.circle(40) # Draw a circle
turtle.end_fill() # Fill the shape

turtle.color("green")
turtle.penup()
turtle.goto(-100, 50)
turtle.pendown()
turtle.write("Cool Colorful Shapes", 
  font = ("Times", 18, "bold"))
turtle.hideturtle()

turtle.done() 

```

# CH04　選擇

```
4.1 AdditionQuiz.py
import random 

# Generate random numbers
number1 = random.randint(0, 9)
number2 = random.randint(0, 9)

# Prompt the user to enter an answer
answer = eval(input("What is " + str(number1) + " + " 
    + str(number2) + "? "))
    
# Display result    
print(number1, "+", number2, "=", answer, 
    "is", number1 + number2 == answer)
```

```
4.2 SimpleIfDemo.py
number = eval(input("Enter an integer: "))

if number % 5 == 0 :
   print("HiFive");

if number % 2 == 0 :
   print("HiEven");
```

```
4.3 GuessBirthday.py
day = 0 # birth day to be determined
  
# Prompt the user to answer the first question
question1 = "Is your birthday in Set1?\n" + \
    " 1  3  5  7\n" + \
    " 9 11 13 15\n" + \
    "17 19 21 23\n" + \
    "25 27 29 31" + \
    "\nEnter 0 for No and 1 for Yes: " 
answer = eval(input(question1))
  
if answer == 1:
   day += 1
 
# Prompt the user to answer the second question
question2 = "Is your birthday in Set2?\n" + \
    " 2  3  6  7\n" + \
    "10 11 14 15\n" + \
    "18 19 22 23\n" + \
    "26 27 30 31" + \
    "\nEnter 0 for No and 1 for Yes: " 
answer = eval(input(question2))
  
if answer == 1:
   day += 2
 
# Prompt the user to answer the third question
question3 = "Is your birthday in Set3?\n" + \
    " 4  5  6  7\n" + \
    "12 13 14 15\n" + \
    "20 21 22 23\n" + \
    "28 29 30 31" + \
    "\nEnter 0 for No and 1 for Yes: " 
answer = eval(input(question3))
  
if answer == 1:
   day += 4
  
# Prompt the user to answer the fourth question
question4 = "Is your birthday in Set4?\n" + \
    " 8  9 10 11\n" + \
    "12 13 14 15\n" + \
    "24 25 26 27\n" + \
    "28 29 30 31" + \
    "\nEnter 0 for No and 1 for Yes: " 
answer = eval(input(question4))
  
if answer == 1:
    day += 8
  
# Prompt the user to answer the fifth question
question5 = "Is your birthday in Set5?\n" + \
    "16 17 18 19\n" + \
    "20 21 22 23\n" + \
    "24 25 26 27\n" + \
    "28 29 30 31" + \
    "\nEnter 0 for No and 1 for Yes: " 
answer = eval(input(question5))
  
if answer == 1:
    day += 16

print("\nYour birthday is" + str(day) + "!")

```

```
4.4 SubtractionQuiz.py
import random

# 1. Generate two random single-digit integers
number1 = random.randint(0, 9)
number2 = random.randint(0, 9)

# 2. If number1 < number2, swap number1 with number2
if number1 < number2:
    number1, number2 = number2, number1 # Simultaneous assignment

# 4. Prompt the student to answer "what is number1 - number2?"
answer = eval(input("What is " + str(number1) + " - " + 
    str(number2) + "? "))

# 4. Grade the answer and display the result
if number1 - number2 == answer:
    print("You are correct!")
else:
    print("Your answer is wrong.\n", number1, "-",
        number2, "is", number1 - number2)
```

```
4.5 ChineseZodiac.py
year = eval(input("Enter a year: "))
zodiacYear = year % 12 
if zodiacYear == 0:
    print("monkey")
elif zodiacYear == 1:
    print("rooster")
elif zodiacYear == 2:
    print("dog")
elif zodiacYear == 3:
    print("pig")
elif zodiacYear == 4: 
    print("rat")
elif zodiacYear == 5: 
    print("ox")
elif zodiacYear == 6:
    print("tiger")
elif zodiacYear == 7:
    print("rabbit")
elif zodiacYear == 8:
    print("dragon")
elif zodiacYear == 9:
    print("snake")
elif zodiacYear == 10:
    print("horse")
else: 
    print("sheep")

```

```
4.6 ComputeBMI.py
# Prompt the user to enter weight in pounds
weight = eval(input("Enter weight in pounds: "))
    
# Prompt the user to enter height in inches
height = eval(input("Enter height in inches: "))
    
KILOGRAMS_PER_POUND = 0.45359237 # Constant
METERS_PER_INCH = 0.0254 # Constant 
    
# Compute BMI
weightInKilograms = weight * KILOGRAMS_PER_POUND 
heightInMeters = height * METERS_PER_INCH
bmi = weightInKilograms / (heightInMeters * heightInMeters)

# Display result
print("BMI is", format(bmi, ".2f"))
if bmi < 18.5:
    print("Underweight")
elif bmi < 25:
    print("Normal")
elif bmi < 30:
    print("Overweight")
else:
    print("Obese")
```

```
4.7 ComputeTax.py
import sys

# Prompt the user to enter filing status
status = eval(input(
    "(0-single filer, 1-married jointly,\n" +
    "2-married separately, 3-head of household)\n" +
    "Enter the filing status: "))

# Prompt the user to enter taxable income
income = eval(input("Enter the taxable income: "))

# Compute tax
tax = 0

if status == 0:  # Compute tax for single filers
    if income <= 8350:
        tax = income * 0.10
    elif income <= 33950:
        tax = 8350 * 0.10 + (income - 8350) * 0.15
    elif income <= 82250:
        tax = 8350 * 0.10 + (33950 - 8350) * 0.15 + \
            (income - 33950) * 0.25
    elif income <= 171550:
        tax = 8350 * 0.10 + (33950 - 8350) * 0.15 + \
            (82250 - 33950) * 0.25 + (income - 82250) * 0.28
    elif income <= 372950:
        tax = 8350 * 0.10 + (33950 - 8350) * 0.15 + \
            (82250 - 33950) * 0.25 + (171550 - 82250) * 0.28 + \
            (income - 171550) * 0.33
    else:
        tax = 8350 * 0.10 + (33950 - 8350) * 0.15 + \
              (82250 - 33950) * 0.25 + (171550 - 82250) * 0.28 + \
              (372950 - 171550) * 0.33 + (income - 372950) * 0.35;
elif status == 1: # Compute tax for married file jointly
    print("Left as exercise")
elif status == 2: # Compute tax for married separately
    print("Left as exercise")
elif status == 3: # Compute tax for head of household
    print("Left as exercise")
else:
    print("Error: invalid status")
    sys.exit()

# Display the result
print("Tax is", format(tax, ".2f"))

```

```
4.8 TestBooleanOperators.py
# Receive an input
number = eval(input("Enter an integer: "))

if number % 2 == 0 and number % 3 == 0:
    print(number, "is divisible by 2 and 3")

if number % 2 == 0 or number % 3 == 0:
    print(number, "is divisible by 2 or 3")

if (number % 2 == 0 or number % 3 == 0) and \
       not (number % 2 == 0 and number % 3 == 0):
    print(number, "divisible by 2 or 3, but not both")


```

```
4.9 LeapYear.py
year = eval(input("Enter a year: "))

# Check if the year is a leap year 
isLeapYear = (year % 4 == 0 and year % 100 != 0) or \
   (year % 400 == 0)

# Display the result 
print(year, "is a leap year?", isLeapYear)

```

```
4.10 Lottery.py
import random

# Generate a lottery
lottery = random.randint(0, 99)

# Prompt the user to enter a guess
guess = eval(input("Enter your lottery pick (two digits): "))

# Get digits from lottery
lotteryDigit1 = lottery // 10
lotteryDigit2 = lottery % 10

# Get digits from guess
guessDigit1 = guess // 10
guessDigit2 = guess % 10

print("The lottery number is", lottery)

# Check the guess
if guess == lottery:
    print("Exact match: you win $10,000")
elif (guessDigit2 == lotteryDigit1 and \
  guessDigit1 == lotteryDigit2):
    print("Match all digits: you win $3,000")
elif (guessDigit1 == lotteryDigit1 
        or guessDigit1 == lotteryDigit2 
        or guessDigit2 == lotteryDigit1 
        or guessDigit2 == lotteryDigit2):
    print("Match one digit: you win $1,000")
else:
    print("Sorry, no match")

```

```
4.11 PointInCircle.py
import turtle

x1, y1 = eval(input("Enter the center of a circle x, y: "))
radius = eval(input("Enter the radius of the circle: "))
x2, y2 = eval(input("Enter a point x, y: "))

# Draw the circle
turtle.penup() # Pull the pen up
turtle.goto(x1, y1 - radius)
turtle.pendown() # Pull the pen down
turtle.circle(radius)

# Draw the point
turtle.penup() # Pull the pen up
turtle.goto(x2, y2)
turtle.pendown() # Pull the pen down
turtle.begin_fill() # Begin to fill color in a shape
turtle.color("red")
turtle.circle(3) 
turtle.end_fill() # Fill the shape

# Display the status
turtle.penup() # Pull the pen up
turtle.goto(x1 - 70, y1 - radius - 20)
turtle.pendown() 

d = ((x2 - x1) * (x2 - x1) + (y2 - y1) * (y2 - y1)) ** 0.5
if d <= radius:
    turtle.write("The point is inside the circle") 
else:
    turtle.write("The point is outside the circle") 

turtle.hideturtle()

turtle.done() 
```

# CH05　迴圈

```

```

```

```

```

```

```

```

```

```

# CH06　函式
