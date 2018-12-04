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

```

```

```

```

```

# CH04　選擇

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
