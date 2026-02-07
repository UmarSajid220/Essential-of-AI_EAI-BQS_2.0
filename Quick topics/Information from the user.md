_Input_ refers to any information a user gives to the program. Specifically, the Python command `input` reads in a line of input typed in by the user. It may also be used to display a message to the user, to prompt for specific input.

The following program reads in the name of the user with the `input` command. It then prints it out with the `print` command:

```python
name = input("What is your name? ")
print("Hi there, " + name)
```

The execution of this program could look like this (input from the user in red):

Sample output

What is your name? **Python** Hi there, Python

What this program prints out is partially dependent on input from the user. That means the execution of the program could also look like this:

Sample output

What is your name? **Faizan Programmer** Hi there, Faizan Programmer

The word `name` in this program is a _variable_. In the context of programming, a variable is a location for storing some _value_, such as a string or a number. This value can be used later, and it can also be changed.

### Naming variables

In principle, variables can be named quite freely, within certain limits specified in the Python language.

It is a common international programming practice to name variables in English, but you may come across code where variables are named in other languages, such as the native language of the programmer. The name of the variable has no direct effect on its content, so the name, in that sense, does not matter. However, it can often be helpful in understanding how code functions if variables are named logically and in English.