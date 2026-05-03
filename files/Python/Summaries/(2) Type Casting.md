---
title: Python
---
> roadmap.sh: [Typecasting](https://www.programiz.com/python-programming/type-conversion-and-casting)

**Type conversion** = the process of converting one data type to another

There are 2 types in Python:
- **Implicit conversion** (automatic type conversion)
- **Explicit conversion** (manual type conversion)

### Implicit Type Conversion
---
In certain situations, Python automatically converts one data type to another.

**Converting `int` to `float`**
- Integer is a smaller data type than floating-point numbers

```python
num1 = 123
num2 = 1.23

sum = num1 + num2

print(“Value:”, sum)
print(“Data Type:”, type(sum))
```

```zsh
# Output
Value: 124.23
Data Type: <class: ‘float’>
```

- We created two variables, `num1` and `num2` of type `int` and `float`
- Then we added these variables and stored the result in `sum`
- The `sum` variable has value **124.23** and is of the `float` data type

Python always **converts smaller data types to larger data types** to avoid data loss

We get `TypeError` if we try to add `str` and `int` (e.g. `‘12’ + 23`) 

### Explicit Type Conversion
---
Users convert