### Problem 01
Please write a program which asks the user for a number of days. The program then prints out the number of seconds in the amount of days given.

The program should function as follows:

Sample output

```
How many days? **1** 
Seconds in that many days: 86400
```
Another example:

Sample output

```
How many days? **7** 
Seconds in that many days: 604800
```

### Problem 02
This program asks the user for three numbers. The program then prints out their product, that is, the numbers multiplied by each other. There is, however, something wrong with the program - it doesn't work quite right, as you can see if you run it. Please fix it.

An example of the expected execution of the program:

Sample output

Please type in the first number: **2** 
Please type in the second number: **3** 
Please type in the third number: **5** 
The product is 30

```python
# Fix the code

number = int(input("Please type in the first number: "))
number = int(input("Please type in the second number: "))
number = int(input("Please type in the third number: "))

product = number * number * number
  
print("The product is", product)
```

### Problem 03
Please write a program which asks the user for two numbers. The program will then print out the sum and the product of the two numbers.

The program should function as follows:

Sample output

Number 1: **3** 
Number 2: **7** 
The sum of the numbers: 10 
The product of the numbers: 21

### Problem 04
Please write a program which asks the user for four numbers. The program then prints out the sum and the mean of the numbers.

The program should function as follows:

Sample output

Number 1: **2** 
Number 2: **1** 
Number 3: **6** 
Number 4: **7** 
The sum of the numbers is 16 and the mean is 4.0

### Problem 05
Please write a program which estimates a user's typical food expenditure.

The program asks the user how many times a week they eat at the student cafeteria. Then it asks for the price of a typical student lunch, and for money spent on groceries during the week.

Based on this information the program calculates the user's typical food expenditure both weekly and daily.

The program should function as follows:

Sample output

How many times a week do you eat at the student cafeteria? **4** 
The price of a typical student lunch? **2.5** 
How much money do you spend on groceries in a week? **28.5**

Average food expenditure: Daily: 5.5 euros Weekly: 38.5 euros


### Problem 06
Please write a program which asks for the number of students on a course and the desired group size. The program will then print out the number of groups formed from the students on the course. If the division is not even, one of the groups may have fewer members than specified.

If you can't get your code working as expected, it is absolutely okay to move on and come back to this exercise later. The topic of the next section is conditional statements. This exercise can also be solved using a conditional construction.

Sample output

How many students on the course? **8** 
Desired group size? **4** 
Number of groups formed: 2

Sample output

How many students on the course? **11** 
Desired group size? **3** 
Number of groups formed: 4

Hint: the integer division operator `//` could come in handy here.