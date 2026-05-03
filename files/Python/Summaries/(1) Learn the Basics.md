---
title: Python
---
## Basic Syntax
---
> roadmap.sh: [Python - Syntax](https://www.tutorialspoint.com/python/python_basic_syntax.htm)

The Python syntax has many similarities to *Perl*, *C* and *Java*.

### Interactive Mode Programming
---
We can invoke the **Python interpreter** from command line.

```bash
$ python3 # Opens Python Terminal Environment
```

```bash
>>> print(“Hello, World!”)
```

Here `>>>` denotes a **Python Command Prompt**.

If you’d run an older version of Python, like **Python 2.4.x**, then you need to use print statement without parenthesis:

```python
print “Hello, World!”
```

### Script Mode Programming
---
When invoking the **Python interpreter** with a script parameter, execution continues until the script is finished.

Python files use extension **`.py`** 

Running a Python script can be done in two my different ways:

```bash
$ python3 App.py
```

or when you have Python interpreter available in `/usr/bin` you can use:

```bash
$ chmod +x App.py
$ ./App.py
```

### Identifiers
---
**A identifier** = a name used to identify a variable, function, class or module.
- Identifiers use letters, underscores or numbers
- Punctuation characters such as comma, or dollar-sign are not allowed within identifiers
- Python is **a case-sensetive language** (foo ≠ Foo)

Some naming conventions for identifiers:
- Classes start with an uppercase letter
- All other identifiers start with lowercase letters
- Identifiers starting with a single leading underscore indicates the identifier is private.

### Reserved Names
---
Python keywords such as `def` or `return` are **reserved names**.

These can not be used as constants, variables or other identifier names.

### Lines and Indentation
---
Blocks of code are denoted by **line indentation**

```python
if True:
    print(“True”)
else:
    print(“False”)
```

### Multi-line Statements
---
Statements in Python typically end with a new line. 

Usage of the **line continuation character `\`** denotes that the line should continue

```python
total = item_one + \
        item_two + \
        item_three
```

Statements contained within the `[]`, `{}` or `()` brackets do not need to use the line continuation character

```python
days = [‘Monday’, ‘Tuesday’,
        ‘Wednesday’]
```

### Quotations 
---
Python accepts single `‘`, double `”` and triple `“””` or `‘’’` quotes to denote string literals

Triple quotes are used to span the string across multiple lines. 

```python
word = ‘word’

sentence = “This is a sentence”

paragraph = “””This is a paragraph. It is made up of multiple lines and sentences.”
```

### Comments
---
Python supports both:
- single-line (or end-of-line) comments
- multi-line (block comments)

[Python Comments](https://www.tutorialspoint.com/python/python_comments.htm) are very much similar to comments in PHP, BASH and Perl Programming languages

Single-line comments:

```python
# My first Python program!
print(“Hello, World!”) 
```

Multi-line comments:

```python
print()
```