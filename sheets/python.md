## PYTHON

**Basic Syntax:**

  * **Hello World:**

```python
print("Hello, world!")
```

  * **Variables:**

```python
age = 30
name = "John Doe"
```

  * **Data Types:**

      * `int`: Integer (e.g., 10, -5)
      * `float`: Floating-point number (e.g., 3.14, -2.5)
      * `str`: String (e.g., "Hello", 'Python')
      * `bool`: Boolean (True or False)
      * `list`: Ordered, mutable sequence (e.g., [1, 2, 3])
      * `tuple`: Ordered, immutable sequence (e.g., (1, 2, 3))
      * `dict`: Key-value pairs (e.g., {"name": "John", "age": 30})
      * `set`: Unordered collection of unique elements (e.g., {1, 2, 3})

  * **Operators:**

      * Arithmetic: `+`, `-`, `*`, `/`, `//` (floor division), `%` (modulo), `**` (exponentiation)
      * Comparison: `==`, `!=`, `>`, `<`, `>=`, `<=`
      * Logical: `and`, `or`, `not`
      * Assignment: `=`, `+=`, `-=`, `*=`, `/=`, etc.

  * **Control Flow:**

      * `if-elif-else` statement
      * `for` loop
      * `while` loop
      * `break` and `continue` statements

**Intermediate Concepts:**

  * **Functions:**

```python
def add(x, y):
  return x + y
```

  * **List Comprehensions:**

```python
squares = [x**2 for x in range(10)]
```

  * **String Formatting:**

```python
name = "John"
age = 30
print(f"My name is {name} and I am {age} years old.")
```

  * **File Handling:**

```python
with open("myfile.txt", "r") as f:
  content = f.read()
```

  * **Modules and Packages:**

```python
import math
from datetime import datetime
```

**Advanced Concepts:**

  * **Classes and Objects:**

```python
class Dog:
  def __init__(self, name):
    self.name = name

  def bark(self):
    print("Woof!")
```

  * **Decorators:**

```python
def my_decorator(func):
  def wrapper():
    print("Something is happening before the function is called.")
    func()
    print("Something is happening after the function is called.")
  return wrapper

@my_decorator
def say_hello():
  print("Hello!")
```

  * **Generators:**

```python
def my_generator(n):
  for i in range(n):
    yield i**2
```

  * **Exceptions:**

```python
try:
  # Code that might raise an exception
except ValueError:
  # Handle ValueError
except Exception as e:
  # Handle other exceptions
finally:
  # Code that always executes
```

  * **Lambda Functions:**

```python
add = lambda x, y: x + y
```

**Tips and Tricks:**

  * Use meaningful variable names.
  * Write comments to explain your code.
  * Use a code editor with syntax highlighting and autocompletion.
  * Use the `help()` function to get information about a function or module.
  * Read the official Python documentation.

**Resources:**

  * **Official Python website:** [https://www.python.org/](https://www.google.com/url?sa=E&source=gmail&q=https://www.python.org/)
  * **Python documentation:** [https://docs.python.org/3/](https://www.google.com/url?sa=E&source=gmail&q=https://docs.python.org/3/)
  * **Learn Python the Hard Way:** [https://learnpythonthehardway.org/](https://www.google.com/url?sa=E&source=gmail&q=https://learnpythonthehardway.org/)
  * **Codecademy:** [https://www.codecademy.com/learn/learn-python-3](https://www.google.com/url?sa=E&source=gmail&q=https://www.codecademy.com/learn/learn-python-3)
  * **Real Python:** [https://realpython.com/](https://www.google.com/url?sa=E&source=gmail&q=https://realpython.com/)
