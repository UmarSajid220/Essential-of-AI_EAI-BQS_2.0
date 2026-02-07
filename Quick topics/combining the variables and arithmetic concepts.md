## Using variables

Let's have a look at a program which calculates the sum of three numbers given by the user:

```python
number1 = int(input("First number: "))
number2 = int(input("Second number: "))
number3 = int(input("Third number: "))

sum = number1 + number2 + number3
print(f"The sum of the numbers: {sum}")
```

An example execution of the program:

Sample output

First number: **5** Second number: **21** Third number: **7** The sum of the numbers: 33

The program uses four different variables, but two would easily suffice in this case:

```python
sum = 0

number = int(input("First number: "))
sum = sum + number

number = int(input("Second number: "))
sum = sum + number

number = int(input("Third number: "))
sum = sum + number

print(f"The sum of the numbers: {sum}")
```

Now all inputs from the user are read into the one and the same variable `number`. The value of the variable `sum` is _increased_ by the value of the variable `number` each time the user inputs a new number.

Let's take a closer look at this command:

```python
sum = sum + number
```

Here, the value of the variable `sum` and the value of the variable `number` are added together, and the result is stored back in the variable `sum`. For example, if before the command the value of `sum` is 3 and the value of `number` is 2, after the command is executed, the value of `sum` is 5.

Increasing the value of a variable is a very common operation. As such, there is a commonly used shorthand notation which achieves the same result as the explicit summing up above:

```python
sum += number
```

This allows us to write the above program a little more concisely:

```python
sum = 0

number = int(input("First number: "))
sum += number

number = int(input("Second number: "))
sum += number

number = int(input("Third number: "))
sum += number

print(f"The sum of the numbers: {sum}")
```

In fact, we don't necessarily need the variable `number` at all. The inputs from the user can also be processed like this:

```python
sum = 0

sum += int(input("First number: "))
sum += int(input("Second number: "))
sum += int(input("Third number: "))

print(f"The sum of the numbers: {sum}")
```

Of course, it will depend on the context how many variables are needed. If it is required to remember each value the user inputs, it will not be possible to "reuse" the same variable to read different values from the user. Consider the following:

```python
number1 = int(input("First number: "))
number2 = int(input("Second number: "))

print(f"{number1} + {number2} = {number1+number2}")
```

Sample output

First number: **2** Second number: **3** 2 + 3 = 5

On the other hand, the above program does not have a named variable for storing the sum of the two values.

"Reusing" a variable only makes sense when there is a need to temporarily store things of a similar type and purpose, for example when summing numbers.

In the following example the variable `data` is used to first store the name of the user, and then their age. This is not at all sensible.

```python
data = input("What is your name? ")
print("Hi " + data + "!")

data = int(input("What is your age? "))
# program continues...
```

A better idea is to use separate variables, with _descriptive_ names:

```python
name = input("What is your name? ")
print("Hi " + name + "!")

age = int(input("What is your age? "))
# program continues...
```


And of course... the [[Problems to solve by combining the variables and arithmetic operations]]