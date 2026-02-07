
A program can ask for more than one input. Notice how below each `input` command stores the received value in a different variable.

```python
name = input("What is your name? ")
email = input("What is your email address? ")
nickname = input("What is your nickname? ")

print("Let's make sure we got this right")
print("Your name: " + name)
print("Your email address: " + email)
print("Your nickname: " + nickname)
```

The program could print out this, for example:

Sample output

What is your name? **Umar Sajid** What is your email address? **[umarsajid220@gmail.com](mailto:umarsajid220@gmail.com)** What is your nickname? **Omar** Let's make sure we got this right Your name: Umar Sajid Your email address: [umarsajid220@gmail.com](mailto:umarsajid220@gmail.com) Your nickname: Omar

### What if the same variable get two values
If the same variable is used to store more than one input, each new value will replace the previous one. For example:

```python
address = input("What is your address? ")
print("So you live at address " + address)

address = input("Please type in a new address: ")
print("Your address is now " + address)
```

An example execution of the program:

Sample output

What is your address? **Python Path 101, Flat 3D** So you live at address Python Path 101, Flat 3D Please type in a new address: **New Road 999** Your address is now New Road 999

This means that if the same variable is used to store two inputs in succession, there is no way to access the first input value after it has been replaced by the second:

```python
address = input("What is your address? ")
address = input("Please type in a new address: ")

print("Your address is now " + address)
```

An example of how the program's output might look like:

Sample output

What is your address? **Python Path 10** Please type in a new address: **Programmer's Walk 23** Your address is now Programmer's Walk 23

Solve the next exercises to understand it more deeply
[[Problems to understand and solve when taking multiple inputs]]