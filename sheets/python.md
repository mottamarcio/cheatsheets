## PYTHON

**Basic Syntax:**

  * **Hello World:**

```python
print("Hello, world!")
```

  * **Variables:**

```python
age: int = 30
name: str = "John Doe"
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
      * Membership: `in`, `not in` (check if an element exists in a sequence)
      * Identity: `is`, `is not` (check if two variables refer to the same object)

  * **Control Flow:**

      * `if-elif-else` statement

      ```python
      if age >= 18:
          print("You are an adult")
      elif age >= 13:
          print("You are a teenager")
      else:
          print("You are a child")
      ```

      * `for` loop

      ```python
      for i in range(5):  # iterates 5 times, i = 0, 1, 2, 3, 4
          print(i)

      fruits = ["apple", "banana", "cherry"]
      for fruit in fruits:
          print(fruit)
      ```

      * `while` loop

      ```python
      count = 0
      while count < 5:
          print(count)
          count += 1
      ```

      * `break` and `continue` statements

      ```python
      for i in range(10):
          if i == 5:
              break  # exit the loop when i is 5
          if i % 2 == 0:
              continue  # skip even numbers
          print(i) 
      ```

**Collections:**

  * **Lists:**

    ```python
    my_list: list[int] = [1, 2, 3, 4, 5]
    my_list.append(6)  # Add an element
    my_list.remove(3)  # Remove an element
    print(my_list[0])  # Access an element by index
    ```

  * **Tuples:** (immutable - cannot be changed after creation)

    ```python
    my_tuple: tuple[str, int, float] = ("apple", 1, 3.14)
    print(my_tuple[0])  # Access an element by index
    ```

  * **Sets:** (unordered, unique elements)

    ```python
    my_set: set[int] = {1, 2, 3}
    my_set.add(4)  # Add an element
    my_set.remove(2)  # Remove an element
    ```

**Dictionaries**

Dictionaries store data in key-value pairs. Keys must be unique and immutable (like strings or numbers), while values can be of any data type.

```python
my_dict: dict[str, int] = {"apple": 1, "banana": 2, "cherry": 3} 
```

*   **Accessing Values:**
    ```python
    print(my_dict["banana"])  # Output: 2
    ```

*   **Modifying Values:**
    ```python
    my_dict["apple"] = 5 
    ```

*   **Adding New Key-Value Pairs:**
    ```python
    my_dict["orange"] = 4
    ```

*   **`del` keyword:** Removes a key-value pair
    ```python
    del my_dict["banana"]  
    ```

*   **`pop()` method:** Removes a key-value pair and returns the value.
    ```python
    removed_value = my_dict.pop("cherry") 
    print(removed_value)  # Output: 3
    ```

*   **`copy()` method:** Creates a shallow copy of the dictionary.
    ```python
    new_dict = my_dict.copy()
    ```

*   **`clear()` method:** Removes all items from the dictionary.
    ```python
    my_dict.clear()
    ```

*   **`keys()` method:** Returns a view object of all keys.
    ```python
    print(my_dict.keys()) 
    ```

*   **`values()` method:** Returns a view object of all values.
    ```python
    print(my_dict.values()) 
    ```

*   **`items()` method:** Returns a view object of all key-value pairs (as tuples).
    ```python
    print(my_dict.items())
    ```

*   **Checking for Key Existence:**
    ```python
    if "apple" in my_dict:
        print("Apple is in the dictionary")
    ```

*   **Iterating through a Dictionary:**
    ```python
    for key in my_dict:
        print(key, my_dict[key]) 
    ```

    ```python
    for key, value in my_dict.items():
        print(key, value)
    ```

**Important Notes:**

*   Trying to access a key that doesn't exist will raise a `KeyError`.
*   Dictionaries are unordered, meaning the items don't have a specific order.

I hope this helps make your cheat sheet even more comprehensive! Let me know if you have any other questions or want to add more to it.


**Intermediate Concepts:**

  * **Functions:**

    ```python
    def add(x: int, y: int) -> int:
        """This function adds two numbers and returns the sum."""
        return x + y

    result: int = add(5, 3)
    print(result)  # Output: 8
    ```

  * **List Comprehensions:**

    ```python
    squares: list[int] = [x**2 for x in range(10)]
    ```

  * **String Formatting:**

    ```python
    name: str = "John"
    age: int = 30
    print(f"My name is {name} and I am {age} years old.")
    ```

  * **File Handling:**

    ```python
    with open("myfile.txt", "r") as f:
        content: str = f.read()
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
      def __init__(self, name: str):
          self.name: str = name

      def bark(self) -> None:
          print("Woof!")

    my_dog: Dog = Dog("Buddy")
    my_dog.bark()  # Output: Woof!
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

    say_hello()
    ```

  * **Generators:**

    ```python
    def my_generator(n: int) -> int:
      for i in range(n):
          yield i**2

    for i in my_generator(5):
        print(i)
    ```

  * **Exceptions:**

    ```python
    try:
      # Code that might raise an exception
      result: int = 10 / 0  # This will raise a ZeroDivisionError
    except ValueError:
      # Handle ValueError
      print("ValueError occurred")
    except ZeroDivisionError:
      # Handle ZeroDivisionError
      print("Cannot divide by zero")
    except Exception as e:
      # Handle other exceptions
      print(f"An error occurred: {e}")
    finally:
      # Code that always executes
      print("This will always execute")
    ```

  * **Lambda Functions:**

    ```python
    add = lambda x: int, y: int: x + y  # type hint for lambda functions
    print(add(5, 3))  # Output: 8
    ```

**Tips and Tricks:**

  * Use name convention: **snake_case** for variables, functions and methods; **SCREAMING_SNAKE_CASE** for constants ; **PascalCase** for classes.
  * Use meaningful variable names.
  * Write comments to explain your code.
  * Use a code editor with syntax highlighting and autocompletion.
  * Use the `help()` function to get information about a function or module.
  * Read the official Python documentation.
  * Use type hints to improve code readability and maintainability.

**Resources:**

  * **Official Python website:** [https://www.python.org/](https://www.google.com/url?sa=E&source=gmail&q=https://www.python.org/)
  * **Python documentation:** [https://docs.python.org/3/](https://www.google.com/url?sa=E&source=gmail&q=https://docs.python.org/3/)
  * **Learn Python the Hard Way:** [https://learnpythonthehardway.org/](https://www.google.com/url?sa=E&source=gmail&q=https://learnpythonthehardway.org/)
  * **Codecademy:** [https://www.codecademy.com/learn/learn-python-3](https://www.google.com/url?sa=E&source=gmail&q=https://www.codecademy.com/learn/learn-python-3)
  * **Real Python:** [https://realpython.com/](https://www.google.com/url?sa=E&source=gmail&q=https://realpython.com/)
