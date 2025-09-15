.. _module2_exception_handling:

Basic Exception Handling: try-except
====================================

Exception handling allows your program to handle errors gracefully instead of crashing.

The `try-except` Block
-----------------------

.. code-block:: python

   try:
       # Code that might raise an exception
       result = 10 / 0
   except ZeroDivisionError:
       print("Cannot divide by zero!")

Catching Multiple Exceptions
----------------------------

.. code-block:: python

   try:
       num = int(input("Enter a number: "))
       result = 10 / num
       print(f"Result: {result}")
   except ValueError:
       print("Please enter a valid number")
   except ZeroDivisionError:
       print("Cannot divide by zero")

The `else` Clause
-----------------

The `else` block executes if no exception occurs.

.. code-block:: python

   try:
       num = int(input("Enter a number: "))
       result = 10 / num
   except ValueError:
       print("Invalid input")
   except ZeroDivisionError:
       print("Cannot divide by zero")
   else:
       print(f"Result: {result}")

The `finally` Clause
--------------------

The `finally` block always executes, regardless of whether an exception occurred.

.. code-block:: python

   try:
       file = open("example.txt", "r")
       content = file.read()
       print(content)
   except FileNotFoundError:
       print("File not found")
   finally:
       file.close()  # This always runs

Common Exceptions
-----------------

- `ValueError` : Invalid value for a data type
- `TypeError` : Operation on incompatible types
- `IndexError` : Accessing invalid index
- `KeyError` : Accessing non-existent dictionary key
- `FileNotFoundError` : File not found
- `ZeroDivisionError` : Division by zero

Raising Exceptions
------------------

You can raise exceptions manually.

.. code-block:: python

   def check_age(age):
       if age < 0:
           raise ValueError("Age cannot be negative")
       return age

   try:
       check_age(-5)
   except ValueError as e:
       print(e)

Best Practices
--------------

- Catch specific exceptions rather than using bare `except`
- Use `finally` for cleanup operations
- Don't overuse exception handling for normal flow control
- Provide meaningful error messages