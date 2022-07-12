# Getting Started: Python Fundamentals
## Practice Problems

1. What types are involved in the following expressions? What data type will each expression evaluate to?
  - `8 * 2.5`: **int, float, float**
  - `9 / 2`: **int, int, float**
  - `9 // -2`: **int, int, int**
  - `1.5 * 2 >= 7 - 3`: **float, int, int, int, bool**

2. Which of these expressions results in an error? Why does each error occur?

`((((5 * 4 ** 7))))`: **Valid** -- Python accepts extraneous parentheses.

`84 *= 0.5 / 7`: **Error** -- Python thinks we are trying to assign a value to 84, which is an integer literal. We can't change its value!

`(-(-(-(-5 * (4 + 3)))))`: **Valid** -- The `-` negates the value in the parentheses.

`5 * 3 = weight` **Error** -- We cannot assign a value to an expression, even if `weight` had been defined.

`73 / -----------5`: **Valid** -- negatives cancel each other out.
```

3. Following the function design recipe, define:
  * a function that converts Fahrenheit into Celsius
  * a function that converts kilometers into miles. (Assume there are 1.6 kilometers in a mile.)

**Example answers**
```python
def f_to_c(degrees):
    '''
    Convert degrees F to degrees C.
    >>> f_to_c(50)
    10.0
    >>> f_to_c(212)
    100.0
    '''
    return (degrees - 32) * (5/9)
```
```python
def km_to_mi(km):
    '''
    Convert kilometers to miles.
    >>> km_to_mi(10)
    6.25
    >>> km_to_mi(1.6)
    1
    '''
    return km / 1.6
```


4. What value is printed in the below code? **3

```python
answer = 3

def answer_to_everything():
    '''Return the answer to life, the universe, and everything'''
    answer = 42
    return answer
    
answer_to_everything()

print(answer)
```

**Answer: 3. The `answer` variable in our function is locally scoped -- our program cannot access the value 42 from outside of the function, including when we called `print(answer)`.**

**Although we called `answer_to_everything()`, we did not assign the output to a variable.**

5. Complete the examples in the docstring below, then write the body of the function. You can assume `num` is always >= 0.

```python
def repeat(string, num):
    ''' Return string repeated num times.
    >>> repeat('yes', 4)
    'yesyesyesyes'
    >>> repeat('no', 0)
    ''
    >>> repeat('yesnomaybe', 3)
    # yesnomaybeyesnomaybeyesnomaybe
    '''
    return string * num
```

6. Complete the function below. You can assume that `number` will always be a string with 10 digits and that the first 3 digits will always be the area code.

**Your answer may vary! This is just one option that uses what was covered in the first and second sessions.**

```python
def is_416_number(number):
    ''' Check whether the number has a 416 area code.
    >>> is_416_number('(416)-555-5555')
    True
    >>> is_416_number('514 416 5555')
    False
    >>> is_416_number('4165554160')
    True
    '''
    # replace parens w/ nothing
    number = number.replace('(', '')
    number = number.replace(')', '')
    return number[:3] == '416'
```