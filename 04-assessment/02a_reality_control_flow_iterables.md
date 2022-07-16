# Dealing with Reality: Control Flow and Iterables
## Practice Problem Solutions

### Q1

```python
def different(a, b):
    '''
    Tell if a and b are different values.
    >>> different(3, 3.0)
    False
    >>> different(3, '3')
    True
    >>> different('apple', 'potato')
    True
    '''
    return a != b
```

### Q2

The language here was a little vague -- you may have opted for the `<=`/`>=` comparison operators.

```python
balance = 3000

if balance < 3000:
    print('Your balance is under $3,000')
elif balance <= 10000:
    print('Your balance is between $3,000 and $10,000')
else:
    print('Your balance is over $10,000.')
```

This would also be a valid solution:
```python
balance = 3000

if balance < 3000:
    print('Your balance is under $3,000')
elif balance >= 3000 and balance <= 10000:
    print('Your balance is between $3,000 and $10,000')
else:
    print('Your balance is over $10,000.')
```

And so would this.
```python
balance = 3000

if balance < 3000:
    print('Your balance is under $3,000')
elif 3000 <= balance <= 10000:
    print('Your balance is between $3,000 and $10,000')
else:
    print('Your balance is over $10,000.')
```

### Q3
```python
books = ['War and Peace', 'Pride and Prejudice', 'Mockingjay', 'Three Musketeers', 'The Adventures of Robinson Crusoe', 'Yevgeniy Onegin']

# an empty list
books[0:0]

# the last item
books[-1]

# the last three items
books[-3:]

# remove 'Pride and Prejudice'
books.remove('Pride and Prejudice')

# Insert Harry Potter and the Chamber of Secrets after Mockingjay
# If you did not remove Pride and Prejudice, the index would be 3, not 2
books.insert(2, 'Harry Potter and the Chamber of Secrets')
```

### Q4
Here, we have to write functions to get the first, second, and third items in a list. Then, we can use those functions as the `key`s for `sorted()`.

```python
people = [('Mark', 'Harrison', 56), ('Ken', 'Wolseley', 23), ('Emily', 'Robinson', 77)]

def get_first_item(lst):
    return lst[0]

def get_second_item(lst):
    return lst[1]

def get_third_item(lst):
    return lst[2]

by_first_name = sorted(people, key=get_first_item)

by_last_name = sorted(people, key=get_second_item)

by_age = sorted(people, key=get_third_item)

```

### Q5
One possible solution:

```python
def dict_intersect(d1, d2):
    '''Return the set of keys found in both d1 and d2.
    >>> dict_intersect({'a': 'A', 'b': 'B', 'c': 'C'}, {'a': 'alpha', 'b': 'beta'})
    {'a', 'b'}
    >>> dict_intersect({'a': 1, 'b': 2}, {'c': 3, 'd': 2})
    set()
    '''
    d1_keys = set(d1.keys())
    d2_keys = set(d2.keys())
    return d1_keys.intersection(d2_keys)
```

### Q6
```python
dividends = [100, 37.5, -12]
divisors = [8, 0, -3]

for x, y in zip(dividends, divisors):
    if y == 0:
        continue
    else:
        print(x/y)
```