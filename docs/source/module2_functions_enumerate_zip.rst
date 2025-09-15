.. _advanced_enumerate_zip:

Functions: enumerate() and zip()
================================

Python provides built-in functions like `enumerate()` and `zip()` that are useful when working with sequences.

The `enumerate()` Function
--------------------------

`enumerate()` adds a counter to an iterable and returns it as an enumerate object.

.. code-block:: python

   fruits = ["apple", "banana", "cherry"]
   for index, fruit in enumerate(fruits):
       print(f"Index {index}: {fruit}")

You can start the counter from a different number:

.. code-block:: python

   for index, fruit in enumerate(fruits, start=1):
       print(f"Index {index}: {fruit}")

The `zip()` Function
--------------------

`zip()` takes two or more iterables and returns an iterator of tuples.

.. code-block:: python

   names = ["Alice", "Bob", "Charlie"]
   ages = [25, 30, 35]
   for name, age in zip(names, ages):
       print(f"{name} is {age} years old.")

If the iterables have different lengths, `zip()` stops at the shortest one.

.. code-block:: python

   names = ["Alice", "Bob", "Charlie", "David"]
   ages = [25, 30]
   for name, age in zip(names, ages):
       print(f"{name} is {age} years old.")
   # Output: Alice is 25, Bob is 30

Using `zip()` with `enumerate()`
---------------------------------

You can combine both functions:

.. code-block:: python

   names = ["Alice", "Bob", "Charlie"]
   ages = [25, 30, 35]
   for index, (name, age) in enumerate(zip(names, ages)):
       print(f"Person {index+1}: {name}, {age} years old.")

Unzipping
---------

You can "unzip" using the `*` operator:

.. code-block:: python

   pairs = [("Alice", 25), ("Bob", 30), ("Charlie", 35)]
   names, ages = zip(*pairs)
   print(names)  # ('Alice', 'Bob', 'Charlie')
   print(ages)   # (25, 30, 35)