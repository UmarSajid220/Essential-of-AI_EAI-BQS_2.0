In the previous sections you've seen examples with basic arithmetics. In the following table you can see the most common arithmetic operators in Python, with examples:

|Operator|Purpose|Example|Result|
|---|---|---|---|
|`+`|Addition|`2 + 4`|`6`|
|`-`|Subtraction|`10 - 2.5`|`7.5`|
|`*`|Multiplication|`-2 * 123`|`-246`|
|`/`|Division (floating point result)|`9 / 2`|`4.5`|
|`//`|Division (integer result)|`9 // 2`|`4`|
|`%`|Modulo|`9 % 2`|`1`|
|`**`|Exponentiation|`2 ** 3`|`8`|

The order of operations is familiar from mathematics: first calculate the exponents, then multiplication and division, and finally addition and subtraction. The order can be changed with parentheses.

For example this bit of code

```python
print(2 + 3 * 3)
print((2 + 3) * 3)
```

prints out

Sample output

11 15

## Operands, operators and data types

A calculation usually consists of _operands_ and _operators_:

[![1 4 1](https://programming-26.mooc.fi/static/f717f6a68e7b1bd3b3fb9cbe2898da5b/9cb4e/1_4_1.png "1 4 1")

The data type of an operand usually determines the data type of the result: if two integers are added together, the result will also be an integer. If a floating point number is subtracted from another floating point number, the result is a floating point number. In fact, if a single one of the operands in an expression is a floating point number, the result will also be a floating point number, regardless of the other operands.

Division `/` is an exception to this rule. Its result is a floating point number, even if the operands are integers. For example `1 / 5` will result in the floating point number `0.2`.

Example:

```python
height = 172.5
weight = 68.55

# the Body Mass Index, or BMI, is calculated by dividing body mass with the square of height
# height is converted into metres in the formula
bmi = weight / (height / 100) ** 2

print(f"The BMI is {bmi}")
```

This program prints out the following:

Sample output

The BMI is 23.037177063642087

Notice Python also has an integer division operator `//`. If the operands are integers, it will produce an integer. The result is rounded down to the nearest integer. For example this program

```python
x = 3
y = 2

print(f"/ operator {x/y}")
print(f"// operator {x//y}")
```

prints out

Sample output

/ operator 1.5 // operator 1

## Numbers as input

We have already used the `input` command to read in strings from the user. The same function can be used to read in numbers, but the string produced by the function must then be converted to a numeric data type in the program code. In the previous section we cast integers as strings with the `str` function. The same basic principle applies here, but the name of the casting function will be different.

A string can be converted into an integer with the function `int`. The following program asks the user for their year of birth and stores it in the variable `input_str`. The program then creates another variable `year`, which contains the year converted into an integer. After this the calculation `2021-year` is possible, using the user-supplied value.

```python
input_str = input("Which year were you born? ")
year = int(input_str)
print(f"Your age at the end of the year 2021: {2021 - year}" )
```

Sample output

Which year were you born? **1995** Your age at the end of the year 2021: 26

Usually you do not need to create two separate variables (like `input_str` and `year` above) to read a number value from the user. Instead, reading the input with the `input` function and converting it with the `int` function can be achieved in one go:

```python
year = int(input("Which year were you born? "))
print(f"Your age at the end of the year 2021: {2021 - year}" )
```

Similarly, a string can be converted into a floating point number with the function `float`. This programs asks the user for their height and weight, and uses these to calculate their BMI:

```python
height = float(input("What is your height? "))
weight = float(input("What is your weight? "))

height = height / 100
bmi = weight / height ** 2

print(f"The BMI is {bmi}")
```

An example printout from the program:

Sample output

What is your height? **163** 
What is your weight? **74.45** 
The BMI is 28.02137829801649

And now your favorite part of [Solving arithmetic problems](Solving%20arithmetic%20problems.md) 