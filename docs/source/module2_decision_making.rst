.. _module2_decision_making:

Decision Making in Python
=========================

Python provides several ways to make decisions in your code using conditional statements. The most common are `if`, `if-else`, `elif`, and nested conditions.

The `if` Statement
------------------

The `if` statement executes a block of code if a condition is true.

.. code-block:: python

   age = 18
   if age >= 18:
       print("You are an adult.")

The `if-else` Statement
-----------------------

The `if-else` statement executes one block if the condition is true, and another if it's false.

.. code-block:: python

   age = 16
   if age >= 18:
       print("You are an adult.")
   else:
       print("You are a minor.")

The `elif` Statement
--------------------

The `elif` (else if) statement allows you to check multiple conditions.

.. code-block:: python

   score = 85
   if score >= 90:
       print("Grade: A")
   elif score >= 80:
       print("Grade: B")
   elif score >= 70:
       print("Grade: C")
   else:
       print("Grade: F")

Nested Conditions
-----------------

You can nest `if` statements inside other `if` statements for more complex logic.

.. code-block:: python

   age = 25
   has_license = True
   if age >= 18:
       if has_license:
           print("You can drive.")
       else:
           print("You need a license.")
   else:
       print("You are too young to drive.")



Comparison Operators
--------------------

Common comparison operators used in conditions:

- `==` : Equal to
- `!=` : Not equal to
- `>` : Greater than
- `<` : Less than
- `>=` : Greater than or equal to
- `<=` : Less than or equal to

Logical Operators
-----------------

Logical operators combine conditions:

- `and` : Both conditions must be true
- `or` : At least one condition must be true
- `not` : Negates the condition

.. code-block:: python

   age = 20
   has_ticket = True
   if age >= 18 and has_ticket:
       print("You can enter the concert.")

match case
----------
The `match` statement, introduced in Python 3.10, provides structural pattern matching, similar to switch-case in other languages but more powerful. It matches a value against patterns and executes the corresponding block.

.. code-block:: python

    n = 2
    match n:
        case 0:
            print("Zero")
        case 1 | 2 | 3:
            print("Small number")
        case _:
            print("Large number")
        

    # output: Small Number
   
Patterns can include literals, variables, sequences, and more for complex matching. Use `case _` as a default catch-all.
Note: if you have expression or complex condition, go with if-elif-else.