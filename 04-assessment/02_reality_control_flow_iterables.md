# Dealing with Reality: Control Flow and Iterables
## Practice Problems

### Q1
Write a function named `different` that takes two arguments, `a` and `b`. If `a` and `b` are different values, the function should return `True`. Otherwise it should return `False`.

<details>
    <summary>Q1 Hint</summary>
    <p>You can write this function with only one line of code -- the <code>return</code> statement -- in the body.
    </p>
</details>

### Q2
Write a conditional that prints different messages if a bank account balance is:
 * below $3,000
 * between $3,000 and $10,000
 * over $10,000

 <details>
    <summary>Q2 Hint</summary>
    <p>
    You can check if a value <code>x</code> is between two other values with a condition like <code>5 <= x <= 10</code>, but you can also solve this problem by strategically ordering conditions.
    </p>
</details>

### Q3
Create a list, `books`, containing the following items: `'War and Peace', 'Pride and Prejudice', 'Mockingjay', 'Three Musketeers', 'The Adventures of Robinson Crusoe', 'Yevgeniy Onegin'`.

    * Using slicing or indexing, create the following:
      - An empty list
      - The last item of `books`
      - List of three items: 'Three Musketeers', 'The Adventures of Robinson Crusoe', 'Yevgeniy Onegin'.
   
    * Using list methods:
      - Remove 'Pride and Prejudice' from the list.
      - Insert 'Harry Potter and the Chamber of Secrets' after 'Mockingjay'.

 <details>
    <summary>Q3 Hints</summary>
    <ul>
    <li>Try using the same number as the starting index and ending index of a slice</li>
    <li>Useful list methods include <code>remove()</code> and <code>insert()</code></li>
    </ul>
    </p>
</details>

### Q4
Given the list `people`, sort it by people's first name, last name and age. Store the sorted lists as `by_first_name`, `by_last_name`, and `by_age`, respectively.  
`people = [('Mark', 'Harrison', 56), ('Ken', 'Wolseley', 23), ('Emily', 'Robinson', 77)]`

 <details>
    <summary>Q4 Hint 1</summary>
    <p> We want our sorting function to return a new list, rather than modifying in place.
    </p>
</details>

 <details>
    <summary>Q4 Hint 2</summary>
    <p><code>sorted()</code> accepts a <code>key</code> argument. This argument is the name of a function to use when sorting list elements.
    </p>
</details>

### Q5
Write a function called `dict_intersect` that takes two dictionaries, `d1` and `d2`, as arguments and returns a set that contains only the keys found in both of the original dictionaries.
```python
def dict_intersect(d1, d2):
    '''Return the set of keys found in both d1 and d2.
    >>> dict_intersect({'a': 'A', 'b': 'B', 'c': 'C'}, {'a': 'alpha', 'b': 'beta'})
    {'a', 'b'}
    >>> dict_intersect({'a': 1, 'b': 2}, {'c': 3, 'd': 2})
    set()
    '''
    return
```

 <details>
    <summary>Q5 Hint 1</summary>
    <p>
    Let's break this down into steps. We need to:
     <ul>
     <li>get the keys in <code>d1</code></li>
     <li>get the keys in <code>d2</code></li>
     <li>convert them both to sets</li>
     <li>and find their intersection</li>
     </ul>
    </p>
</details>

 <details>
    <summary>Q5 Hint 2</summary>
    <p>
    Some useful functions and methods are <code>keys()</code>, <code>set()</code>, and <code>intersection()</code>.
    </p>
</details>

### Q6
Write a loop that iterates over the two lists below simultaneously. For each pair of values, print the first number divided by the second. When the program encounters a zero divisor, it should skip the pair without printing anything.  

```python
dividends = [100, 37.5, -12]
divisors = [8, 0, -3]
```
 <details>
    <summary>Q6 Hint 1</summary>
    <p>
    We can exit a loop early with <code>break</code>.
    </p>
</details>

 <details>
    <summary>Q6 Hint 2</summary>
    <p>
    Remember that we can bundle two lists pairwise with <code>zip()</code>.
    </p>
</details>