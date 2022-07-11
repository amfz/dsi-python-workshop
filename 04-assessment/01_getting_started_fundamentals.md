# Getting Started: Python Fundamentals
## Practice Problems

1. What types are involved in the following expressions? What data type will each expression evaluate to?
  - `8 * 2.5`
  - `9 / 2`
  - `9 // -2`
  - `1.5 * 2 >= 7 - 3`

2. Which of these expressions results in an error? Why does each error occur?

```python

 ((((5 * 4 ** 7))))

84 *= 0.5 / 7

(-(-(-(-5 * (4 + 3)))))

5 * 3 = weight

73 / -----------5
```

3. Following the function design recipe, define:
  * a function that converts Fahrenheit into Celsius
  * a function that converts kilometers into miles. (There are 1.6 kilometers in a mile.)

4. What value is printed in the below code?

```python
answer = 3

def answer_to_everything():
    '''Return the answer to life, the universe, and everything'''
    answer = 42
    return answer
    
answer_to_everything()

print(answer)
```

5. Complete the examples in the docstring below, then write the body of the function.

```python
def repeat(string, num):
    ''' Return string repeated num times.
    >>> repeat('yes', 4)
    'yesyesyesyes'
    >>> repeat('no', 0)
    # your expected output here
    >>> repeat('yesnomaybe', 3)
    # your expected output here
    '''
    # your code here
    return
```

6. Complete the function below. You can assume that `number` will always be a string with 10 digits and that the first 3 digits will always be the area code.

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
    # your code here
    return
```