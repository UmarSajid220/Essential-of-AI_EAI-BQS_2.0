Variables are needed for various purposes in programming. You can use variables to store any information that will be needed later in the program's execution.

In Python programming variables are created like so:

`variable_name = ...`

Here `...` means the value stored in the variable.

For example, when you used the `input` command to read a string from the user, you stored the string in a variable and then used the variable later in your program:

```python
name = input("What is your name? ")
print("Hi, " + name)
```

Sample output

What is your name? **Ali** Hi, Ali

The value stored in a variable can also be defined using other variables:

```python
given_name = "Paul"
family_name = "Python"

name = given_name + " " + family_name

print(name)
```

Sample output

Paul Python

Here the values stored in the three variables are not obtained from user input. They remain the same every time the program is executed. This is called _hard-coding_ data into the program.

## Changing the value of a variable[](https://programming-26.mooc.fi/part-1/3-more-about-variables#changing-the-value-of-a-variable)

As implied by the name _variable_, the value stored in a variable can change. In the previous section we noticed that the new value replaces the old one.

During the execution of the following program, the variable `word` will have three different values:

```python
word = input("Please type in a word: ")
print(word)

word = input("And another word: ")
print(word)

word = "third"
print(word)
```

Sample output

Please type in a word: **first** first And another word: **second** second third

The value stored in the variable changes each time the variable is assigned a new value.

The new value of a variable can be derived from its old value. In the following example the variable `word` is first assigned a value based on user input. Then it is assigned a new value, which is the old value with three exclamation marks added to the end.

```python
word = input("Please type in a word: ")
print(word)

word = word + "!!!"
print(word)
```

Sample output

Please type in a word: **test** test test!!!

### Choosing a good name for a variable

- It is often useful to name variables according to what they are used for. For example, if the variable contains a word, the name `word` is a better choice than, say, `a`.
    
- There is no set limit to the length of a variable name in Python, but there are some other limitations. A variable name should begin with a letter, and it can only contain letters, numbers and underscores _.
    
- Lowercase and uppercase letters are different characters. The variables `name`, `Name` and `NAME` are all different variables. While this rule has a few exceptions, we will ignore those for now.
    
- It is a common programming practice in Python to use only lowercase characters in variable names. If the variable name consists of multiple words, use an underscore between the words. While this rule also has a few exceptions, we will ignore those for now.
    

## Integers

Thus far, we have only stored strings in variables, but there are also many other types of information we will want to store and access later. Let's have a look at integers first. Integers are numbers that do not have a decimal or fractional part, such as `-15`, `0` and `1`.

The following program creates the variable `age`, which contains an integer value.

```python
age = 24
print(age)
```

The program prints out just this:

Sample output

24

Notice the lack of quotation marks here. In fact, if we were to add quotation marks around the number, this would mean our variable would no longer be an integer, but a string instead. A string can contain numbers, but it is processed differently.

So, why does it matter that variables have a type, when the following program still prints out the same thing twice?

```python
number1 = 100
number2 = "100"

print(number1)
print(number2)
```

Sample output

100 100

Variable types matter because different operations affect different types of variables in different ways. Let's have a look at an example:

```python
number1 = 100
number2 = "100"

print(number1 + number1)
print(number2 + number2)
```

This prints out the following:

Sample output

200 100100

For integer values the `+` operator means addition, but for string values it means concatenation, or "stringing together".

Not all operators are available for all types of variables. While numbers can be divided using the division operator `/`, attempting to divide a string by a number causes an error:

```python
number = "100"
print(number / 2)
```

Sample output

TypeError: unsupported operand type(s) for /: 'str' and 'int'

## Combining values when printing

Similarly, the following program will not work, because `"The result is "` and `result` are of two different types:

```python
result = 10 * 25
# the following line produces an error
print("The result is " + result)
```

The program does not print out anything, but instead throws an error:

Sample output

TypeError: unsupported operand type(s) for +: 'str' and 'int'

Here, Python tells us that combining two different types of values will not work just like that. In this case, `"The result is "` is of type string, while the value stored in `result` is of type integer.

If we do want to print out a string and an integer in a single command, the integer can be cast as a string with the `str` function, and the two strings can then be combined normally. For example, this would work:

```python
result = 10 * 25
print("The result is " + str(result))
```

Sample output

The result is 250

The `print` command also has built-in functionalities that support combining different types of values. The simplest way is to add a comma between the values. All the values will be printed out regardless of their type:

```python
result = 10 * 25
print("The result is", result)
```

Sample output

The result is 250

Notice that there is an automatically added whitespace character between the values separated by a comma here.

## Printing with f-strings

What if we want to have more flexibility and control over what we print out? So called _f-strings_ are another way of formatting printouts in Python. The syntax can initially look a bit confusing, but in the end f-strings are often the simplest way of formatting text.

With f-strings the previous example would look like this:

```python
result = 10 * 25
print(f"The result is {result}")
```

Let's break this apart. In the very beginning of the string we are printing out there is the character _f_. This tells Python that what follows is an f-string. Within the string, enclosed in curly brackets, is the variable name `result`. The value it contains becomes a part of the printed string. The printout is exactly the same as in the previous examples:

Sample output

The result is 250

A single f-string can contain multiple variables. For example this code

```python
name = "Mark"
age = 37
city = "Palo Alto"
print(f"Hi {name}, you are {age} years old. You live in {city}.")
```

prints out this:

Sample output

Hi Mark, you are 37 years old. You live in Palo Alto.

It is difficult to create a printout exactly like this using the comma notation in the `print` command. For example, this program

```python
name = "Mark"
age = 37
city = "Palo Alto"
print("Hi", name, ", you are", age, "years old. You live in", city, ".")
```

prints out the following:

Sample output

Hi Mark , you are 37 years old. You live in Palo Alto .

Notice the automatically inserted whitespace between each comma-separated part of the printout. Preventing `print` from adding the extra spaces is technically possible, but not worth the trouble given that we can instead use f-strings.

In its simplicity the comma notation of the `print` command can often be useful, but it does sometimes cause more trouble than it's worth. F-strings are usually a more reliable option. In part 4 you will learn more about the handy features of f-strings when it comes to formatting printouts.

### F-strings and Python versions

If you are using an older version of Python, f-strings may not work. They were introduced in Python version 3.6. Later on during the course you will install Python on your own computer. Unfortunately, the more modern versions of Python are not always available for older operating systems. If that is the case with your computer, when there are exercises requiring the use of f-strings, you can always try them out in the in-browser exercise templates in these early parts of this course.


Now solve [Something little complex about variables](Something%20little%20complex%20about%20variables.md) 
