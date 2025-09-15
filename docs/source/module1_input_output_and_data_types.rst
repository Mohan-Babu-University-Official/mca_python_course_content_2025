.. _module1_input_output_and_data_types:

Input/Output, Formatted Strings, and Data Types
=========================================================

1. Using ``input()`` and ``print()``
------------------------------------

``input()``
~~~~~~~~~~~

- Used to take user input from the keyboard.

- Always returns data as a string.

- Example:

  .. code:: python

     name = input("Enter your name: ")
     print("Hello,", name)
     city = input("Enter your city: ")
     print("You are from", city)
     age = int(input("Enter your age: "))
     print("You are", age, "years old.")
     rate = float(input("Enter your rate: "))
     print("Your rate is", rate)

- **Tip:** Convert input to other types if needed, e.g.,
  ``int(input("Enter age: "))``.

``print()``
~~~~~~~~~~~

- Used to display output to the screen.

- Can print multiple values, variables, and expressions.

- Example:

  .. code:: python

     print("Welcome to Python!")
     print("Sum:", 5 + 3)
     print("Hello", "World", "!")
     name = "Alice"
     print("Name:", name)
     name, age, city = "Alice", 22, "New York"
     print("Name:", name, "Age:", age, "City:", city)

- **Tip:** Use ``sep`` and ``end`` parameters for custom separators and
  line endings.

  .. code:: python

     print("A", "B", sep="-")  # Output: A-B
     print("Hello", end="!")   # Output: Hello!

--------------

2. Formatted Strings
--------------------

f-strings (Python 3.6+)
~~~~~~~~~~~~~~~~~~~~~~~

- Embed variables and expressions directly in strings.

- Example:

  .. code:: python

     name = "Alice"
     age = 22
     print(f"{name} is {age} years old.")

- **Tip:** f-strings are fast and readable. You can use expressions
  inside ``{}``.

``format()`` Method
~~~~~~~~~~~~~~~~~~~

- Insert values into placeholders ``{}`` in a string.

- Example:

  .. code:: python

     print("{} scored {} marks.".format("Bob", 95))
     print("{1} is {0} years old.".format(30, "Charlie"))

- **Tip:** Use positional or named placeholders for clarity.

--------------

3. The 10 Data Types
--------------------

``int`` (Integer)
~~~~~~~~~~~~~~~~~

- Whole numbers, e.g., 5, -10, 0

- Example:

  .. code:: python

     x = 10
     print(type(x))  # <class 'int'>

``float`` (Floating Point)
~~~~~~~~~~~~~~~~~~~~~~~~~~

- Numbers with decimals, e.g., 3.14, -0.5

- Example:

  .. code:: python

     y = 3.5
     print(type(y))  # <class 'float'>

``complex`` (Complex Number)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Numbers with a real and imaginary part, e.g., 2 + 3j

- Example:

  .. code:: python

     z = 1 + 2j
     print(type(z))  # <class 'complex'>

``NoneType``
~~~~~~~~~~~~

- Represents the absence of a value or a null value.

- Example:

  .. code:: python

     n = None
     print(type(n))  # <class 'NoneType'>

``str`` (String)
~~~~~~~~~~~~~~~~

- Sequence of characters, e.g., “hello”, ‘Python’

- Example:

  .. code:: python

     s = "Python"
     print(type(s))  # <class 'str'>

``bool`` (Boolean)
~~~~~~~~~~~~~~~~~~

- Logical values: ``True`` or ``False``

- Example:

  .. code:: python

     flag = True
     print(type(flag))  # <class 'bool'>

``list`` (List)
~~~~~~~~~~~~~~~

- Ordered collection of items, e.g., [1, 2, 3], [‘apple’, ‘banana’]

- Example:

  .. code:: python

     fruits = ["apple", "banana", "cherry"]
     print(type(fruits))  # <class 'list'>

``tuple`` (Tuple)
~~~~~~~~~~~~~~~~~

- Ordered collection of items, similar to a list but immutable (cannot
  be changed).

- Example:

  .. code:: python

     point = (3, 5)
     print(type(point))  # <class 'tuple'>

``set`` (Set)
~~~~~~~~~~~~~

- Unordered collection of unique items, e.g., {1, 2, 3}, {‘apple’,
  ‘banana’}

- Example:

  .. code:: python

     fruits = {"apple", "banana", "cherry"}
     print(type(fruits))  # <class 'set'>

``dict`` (Dictionary)
~~~~~~~~~~~~~~~~~~~~~

- Collection of key-value pairs, e.g., {‘name’: ‘Alice’, ‘age’: 22}

- Example:

  .. code:: python

     student = {"name": "Alice", "age": 22}
     print(type(student))  # <class 'dict'>

Other important Data Types
--------------------------

``bytes`` (Bytes)
~~~~~~~~~~~~~~~~~

- Immutable sequence of bytes, e.g., b’hello’

- Example:

  .. code:: python

     b = b"Hello"
     print(type(b))  # <class 'bytes'>

``frozenset`` (Frozen Set)
~~~~~~~~~~~~~~~~~~~~~~~~~~

- Immutable version of a set.

- Example:

  .. code:: python

     fs = frozenset([1, 2, 3])
     print(type(fs))  # <class 'frozenset'>

``OrderedDict`` (Ordered Dictionary)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Dictionary that maintains the order of items.

- Example:

  .. code:: python

     from collections import OrderedDict
     od = OrderedDict()
     od["apple"] = 1
     od["banana"] = 2
     print(type(od))  # <class 'collections.OrderedDict'>

``defaultdict`` (Default Dictionary)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Dictionary that provides a default value for a nonexistent key.

- Example:

  .. code:: python

     from collections import defaultdict
     dd = defaultdict(int)
     dd["apple"] += 1
     print(dd)  # defaultdict(<class 'int'>, {'apple': 1})

``Counter`` (Counter)
~~~~~~~~~~~~~~~~~~~~~

- Dictionary subclass for counting hashable objects.

- Example:

  .. code:: python

     from collections import Counter
     c = Counter(["apple", "banana", "apple"])
     print(c)  # Counter({'apple': 2, 'banana': 1})

``deque`` (Double-Ended Queue)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- List-like container with fast appends and pops on either end.

- Example:

  .. code:: python

     from collections import deque
     d = deque()
     d.append(1)
     d.appendleft(2)
     print(d)  # deque([2, 1])

``UserDict`` (User Dictionary)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Dictionary subclass that allows for easier subclassing.

- Example:

  .. code:: python

     from collections import UserDict
     class MyDict(UserDict):
         def __setitem__(self, key, value):
             super().__setitem__(key, value)
     d = MyDict()
     d["apple"] = 1
     print(d)  # MyDict({'apple': 1})

``UserList`` (User List)
~~~~~~~~~~~~~~~~~~~~~~~~

- List subclass that allows for easier subclassing.

- Example:

  .. code:: python

     from collections import UserList
     class MyList(UserList):
         def append(self, item):
             super().append(item)
     l = MyList()
     l.append(1)
     print(l)  # MyList([1])

--------------

4. Dynamic Typing & Type Conversions (Explicit, Implicit)
---------------------------------------------------------

**Dynamic Typing**

- Python is dynamically typed, meaning you do not need to declare variable types. The type is determined at runtime based on the value assigned.

  .. code:: python

     x = 10      # x is int
     x = "ten"   # now x is str
     print(type(x))  # <class 'str'>

**Implicit Type Conversion (Automatic)**

- Python automatically converts one data type to another when needed, usually from a “smaller” to a “larger” type (e.g., int to float).

  .. code:: python

     a = 5       # int
     b = 2.0     # float
     c = a + b   # int + float -> float
     print(c)    # 7.0
     print(type(c))  # <class 'float'>

  - **Note:** Implicit conversion only works when it is safe. For example, adding an int and a float is fine, but adding a string and an int is not.

**Explicit Type Conversion (Type Casting)**

- You can manually convert data from one type to another using functions like ``int()``, ``float()``, ``str()``, etc.

  .. code:: python

     a = "5"
     b = "2"
     c = int(a) + int(b)  # convert strings to int
     print(c)  # 7

  - **Example: Converting float to int**

    .. code:: python

       x = 3.7
       y = int(x)  # y is 3 (decimal part is truncated)
       print(y)

**Common Errors**

- **TypeError:** Occurs when you try to perform an operation on incompatible types.

  .. code:: python

     a = "5"
     b = 2
     print(a + b)  # TypeError: can only concatenate str (not "int") to str

  - **Fix:** Convert ``b`` to string or ``a`` to int:

    .. code:: python

       print(int(a) + b)  # 7
       print(a + str(b))  # "52"

- **ValueError:** Occurs when conversion is not possible.

  .. code:: python

     s = "hello"
     n = int(s)  # ValueError: invalid literal for int() with base 10: 'hello'

  - **Fix:** Ensure the string represents a valid number before conversion.

**Tip:** Always check or handle possible conversion errors using ``try``/``except`` blocks for robust code.

  .. code:: python

     s = "abc"
     try:
         n = int(s)
     except ValueError:
         print("Cannot convert to int!")

5. Extra Tips for Students
--------------------------

- Always convert input to the required type using ``int()``,
  ``float()``, etc.
- Use ``type()`` to check the data type of a variable.
- Strings can be enclosed in single or double quotes.
- Boolean values are case-sensitive: use ``True`` and ``False`` (not
  ``true``/``false``).
- Practice using ``input()`` and ``print()`` in small programs to build
  confidence.
- Use formatted strings for clean and readable output.

--------------

*Prepared by Zaid Kamil.*
