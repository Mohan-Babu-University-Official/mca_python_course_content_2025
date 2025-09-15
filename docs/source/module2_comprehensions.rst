.. _advanced_comprehensions:

List and Dictionary Comprehensions
==================================

Comprehensions provide a concise way to create lists and dictionaries from iterables.

List Comprehensions
-------------------

List comprehensions create lists in a single line.

.. code-block:: python

   # Basic list comprehension
   squares = [x**2 for x in range(10)]
   print(squares)  # [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

   # With condition
   even_squares = [x**2 for x in range(10) if x % 2 == 0]
   print(even_squares)  # [0, 4, 16, 36, 64]

   # Nested list comprehension
   matrix = [[i*j for j in range(3)] for i in range(3)]
   print(matrix)  # [[0, 0, 0], [0, 1, 2], [0, 2, 4]]

Dictionary Comprehensions
-------------------------

Dictionary comprehensions create dictionaries.

.. code-block:: python

   # Basic dictionary comprehension
   squares_dict = {x: x**2 for x in range(5)}
   print(squares_dict)  # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

   # With condition
   even_squares_dict = {x: x**2 for x in range(10) if x % 2 == 0}
   print(even_squares_dict)  # {0: 0, 2: 4, 4: 16, 6: 36, 8: 64}

   # From two lists
   keys = ['a', 'b', 'c']
   values = [1, 2, 3]
   my_dict = {k: v for k, v in zip(keys, values)}
   print(my_dict)  # {'a': 1, 'b': 2, 'c': 3}

Set Comprehensions
------------------

You can also create sets using comprehensions.

.. code-block:: python

   # Set comprehension
   squares_set = {x**2 for x in range(10)}
   print(squares_set)  # {0, 1, 4, 9, 16, 25, 36, 49, 64, 81}

Advantages of Comprehensions
----------------------------

- More concise than traditional loops
- Often faster than equivalent loop code
- Can be more readable for simple operations

Equivalent Code
---------------

List comprehension:

.. code-block:: python

   squares = [x**2 for x in range(10)]

Equivalent with loop:

.. code-block:: python

   squares = []
   for x in range(10):
       squares.append(x**2)