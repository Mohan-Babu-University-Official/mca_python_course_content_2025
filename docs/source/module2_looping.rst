.. _module2_looping:

Looping in Python
=================

Loops allow you to execute a block of code repeatedly. Python has two main types of loops: `for` and `while`.

The `for` Loop
--------------

The `for` loop iterates over a sequence (like a list, tuple, string, or range).

.. code-block:: python

   # Iterating over a list
   fruits = ["apple", "banana", "cherry"]
   for fruit in fruits:
       print(fruit)

   # Using range()
   for i in range(5):
       print(i)

The `while` Loop
----------------

The `while` loop continues as long as a condition is true.

.. code-block:: python

   count = 0
   while count < 5:
       print(count)
       count += 1

Loop Control Statements
-----------------------

- `break` : Exits the loop prematurely
- `continue` : Skips the current iteration and continues with the next
- `pass` : Does nothing (placeholder)

.. code-block:: python

   # break example
   for i in range(10):
       if i == 5:
           break
       print(i)

   # continue example
   for i in range(10):
       if i % 2 == 0:
           continue
       print(i)

   # pass example
   for i in range(5):
       if i == 2:
           pass  # Do nothing
       print(i)

Nested Loops
------------

You can have loops inside loops.

.. code-block:: python

   for i in range(3):
       for j in range(2):
           print(f"i={i}, j={j}")

Infinite Loops
--------------

Be careful with `while` loops to avoid infinite loops.

.. code-block:: python

   # This will run forever (don't run this!)
   # while True:
   #     print("Infinite loop")