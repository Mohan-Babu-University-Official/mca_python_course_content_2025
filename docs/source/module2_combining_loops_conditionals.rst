.. _module2_combining_loops_conditionals:

Combining Loops with Conditionals
==================================

You can combine loops with conditional statements to create more complex logic and control flow.

Basic Combination
-----------------

.. code-block:: python

   numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
   even_numbers = []

   for num in numbers:
       if num % 2 == 0:
           even_numbers.append(num)

   print(even_numbers)  # [2, 4, 6, 8, 10]

Using `continue` and `break` with Conditions
--------------------------------------------

.. code-block:: python

   # Using continue
   for i in range(10):
       if i % 2 != 0:
           continue
       print(i)  # Prints even numbers

   # Using break
   for i in range(10):
       if i == 5:
           break
       print(i)  # Prints 0, 1, 2, 3, 4

Nested Loops with Conditions
----------------------------

.. code-block:: python

   for i in range(3):
       for j in range(3):
           if i == j:
               print(f"Diagonal: ({i}, {j})")
           elif i > j:
               print(f"Lower: ({i}, {j})")
           else:
               print(f"Upper: ({i}, {j})")

Conditional Expressions in Loops
--------------------------------

.. code-block:: python

   # Ternary operator in list
   numbers = [1, 2, 3, 4, 5]
   result = ["even" if num % 2 == 0 else "odd" for num in numbers]
   print(result)  # ['odd', 'even', 'odd', 'even', 'odd']

Complex Conditions
------------------

.. code-block:: python

   grades = [85, 92, 78, 96, 88]
   for grade in grades:
       if grade >= 90:
           print(f"Grade {grade}: Excellent")
       elif grade >= 80:
           print(f"Grade {grade}: Good")
       elif grade >= 70:
           print(f"Grade {grade}: Satisfactory")
       else:
           print(f"Grade {grade}: Needs improvement")

Looping with Multiple Conditions
--------------------------------

.. code-block:: python

   students = [
       {"name": "Alice", "age": 20, "grade": 85},
       {"name": "Bob", "age": 22, "grade": 92},
       {"name": "Charlie", "age": 19, "grade": 78}
   ]

   for student in students:
       if student["age"] >= 20 and student["grade"] >= 80:
           print(f"{student['name']} qualifies for honors")
       elif student["age"] < 20 or student["grade"] < 80:
           print(f"{student['name']} needs more requirements")