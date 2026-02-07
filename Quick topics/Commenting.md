Any line beginning with the pound sign `#`, also known as a hash or a number sign, is a comment. This means that any text on that line following the `#` symbol will not in any way affect how the program functions. Python will simply ignore it.

Comments are used for explaining how a program works, to both the programmer themselves, and others reading the program code. In this program a comment explains the calculation performed in the code:

```python
print("Hours in a year:")
# there are 365 days in a year and 24 hours in each day
print(365*24)
