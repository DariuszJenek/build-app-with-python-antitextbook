# Operators

Python has the following major operators:

`<, >, =, ==, >=, <=, !=, *, +, -, **, +=, -=, /=, *=, in, and, not, is.`

## Operator priority
When expressions containing more than one operators are evaluated, the operator priority is followed, it is just like the BODMAS (PEMDAS for Americans) rule of maths. Usage of `()` can override priority. 

```python
>>> 3 * 2 + 20 - 46
-20
>>> 3 * (2 + 20 - 46)
-72 
```

## Assignment

`=` is the assignment operator. 

```python
>>> a = 1 # creates a new integer object of value 1
	  # and stores the address in variable a.
>>> a = 2 # creates a new integer object of value 2
	  # and stores the address in variable a.
>>> b = a # stores the address of variable a inside
 	  # variable b, they point to the same object.
```

## Multiply

```python
>>> a = 12
>>> a * 12
144
>>> a = "ab_"
>>> a * 2 # when * is used with strings,
          # it returns a new string twice.
ab_ab_
```

## Exercise:
1. Take two numbers from the user and print their multiplication.
1. Take three numbers from the user and print their multiplication.

## Add

```python
>>> a = 1
>>> a + 1
2
>>> a = 'py'
>>> a + 'thon' # concatenates 'thon' to 'py' and creates a new string.
python
>>> a # we did not reassign a, so it's value is unchanged.
py
```

## Exercise:
1. Take two strings from a variable and print their concatenation.
1. Take two numbers from the user and add them (you need to use the int() to convert the input to integer)
1. Take three numbers from the user and print their addition.

## Equality
`==` is the equality operator, it returns true if both operands have the same value.

```python
>>> a = 1 # creates variable a with value 1.
>>> b = 1 # creates variable a with value 1
>>> a == b # checks if a and b are equal.
True
```

> Note: It is a classic mistake to use `==` when you really want to use `=` or vice versa. 

## Division

`27/7` divides 27 by 7 and returns a floating point result

`27//7` divides 27 by 7 and returns an integer result.

```python
>>> 27/7 
3.85714
>>> 27//7
3
>>> 27%7 
1
```

## Power

`**` is the operator for calculating power.

```python	
>>> a = 2
>>> a**3
8
```

## Shortcut operators

Consider that you have to create a variable `a = 3`. If you want to add `4` to the variable `a`.

You can do the following: 

1. `a = a + 4`. But this tends to be verbose.
1. `a += 4`: Another way to do exactly the same calculation.

`+=` is a shortcut operator. There are other shortcut operators like: `+=, -=, /=, *=`. No spaces are allowed between -=, +=.

In other languages, you can use `++` or `--`, but they are not available in Python.

```python
>>> a = 10
>>> a += 10
>>> a = a + 10 # same as a += 10
>>> a *= 10
>>> a /= 10
```

## Membership test

The `in` operator tests if the element on the left hand side is present in the right hand side sequence (list, tuple, set).

```python
>>> a = [1,2,3] # also works on set and tuples.
>>> 3 in a
True
```

## Boolean operators

Read the [docs](http://docs.python.org/3/library/stdtypes.html#boolean-operations-and-or-not)

### not

Read the [docs](http://docs.python.org/3/library/stdtypes.html#truth-value-testing)
`not` converts True to False and vice versa.

```python
>>> not True
False
>>> not False
True
```

#### False like values
Variables of any data type when they are null or have no value, they are False like values. 
The negation of a False like value is True

```python
>>> not '' # empty string is False like.
True
>>> not 0 # 0 is False like.
True
>>> not dict() # empty dict is False like.
True
>>> not list() # empty list is False like.
True
```

#### True like 
Variables of any data type when have _some_ value, any value, they are True like values.
The negation of a True like value is False

```python
>>> not 'dd'
False
>>> not 1 # non zero is True like.
False
>>> not -1 # non zero is True like.
False
>>> not [1,2,3] # list having any value is True like.
False
```

### or

OR is true when either of the operand is true.

```python
>>> True or False
True
>>> False or False
False
```

### and

AND is true when both the operands are true.

```python
>>> True and False
False
>>> False and False
False
>>> True and True
True
```

### Comparision Operators

Read the [docs](https://docs.python.org/3/library/stdtypes.html#comparisons)

There are eight comparison operations in Python. They all have the same priority (which is higher than that of the Boolean operations). Comparisons can be chained arbitrarily; for example, x < y <= z is equivalent to x < y and y <= z, except that y is evaluated only once (but in both cases  y <= z is not evaluated at all if x < y is found to be false).

This table summarizes the comparison operations:

|Operation |	Meaning|
|------|------|
|< |	strictly less than|
|<= |	less than or equal|
|> 	|strictly greater than|
|>= |	greater than or equal|
|== |	equal|
|!= |	not equal|
|is |	object identity|
|is not |	negated object identity|

##### Links

|[Next](04-list-set-dict.md) | [Previous](03-01-understanding-variables.md) |  [Index](../SUMMARY.md)
| ----| ----| ----| 
