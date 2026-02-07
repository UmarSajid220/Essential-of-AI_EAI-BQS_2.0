### Problem 01
This program already contains two integer variables, `x` and `y`:

```python
x = 27
y = 15
```

Please complete the program so that it also prints out the following:

Sample output

27 + 15 = 42 
27 - 15 = 12 
27 * 15 = 405 
27 / 15 = 1.8

The program should work correctly even if the values of the variables are changed. That is, if the first two lines are replaced with this

```python
x = 4
y = 9
```

the program should print out the following:

Sample output

4 + 9 = 13 
4 - 9 = -5 
4 * 9 = 36 
4 / 9 = 0.4444444444444444



Write the solution of this:
```python
# Write your solution here
x = 27
y = 15
```


### Problem 02
Each `print` command usually prints out a line of its own, complete with a change of line at the end. However, if the `print` command is given an additional argument `end = ""`, it will not print a line change.

For example:

```python
print("Hi ", end="")
print("there!")
```

Sample output

Hi there!

Please fix this program so that the entire calculation, complete with result, is printed out on a single line. Do not change the number of `print` commands used.

```python
# fix the given code
print(5)
print(" + ")
print(8)
print(" - ")
print(4)
print(" = ")
print(5 + 8 - 4)
```