.. _module1_operators_expressions_comments:

Operators, Expression Evaluation, and Comments
========================================================

1. Operator Types in Python
---------------------------

Arithmetic Operators
~~~~~~~~~~~~~~~~~~~~

- Used for mathematical operations.

- ``+`` (Addition), ``-`` (Subtraction), ``*`` (Multiplication), ``/``
  (Division), ``//`` (Floor Division), ``%`` (Modulus), ``**``
  (Exponentiation)

- Example:

  .. code:: python

     a = 10
     b = 3
     print(a + b)  # 13
     print(a / b)  # 3.333...
     print(a // b) # 3
     print(a ** b) # 1000

Relational (Comparison) Operators
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Compare values and return ``True`` or ``False``.

- ``==``, ``!=``, ``>``, ``<``, ``>=``, ``<=``

- Example:

  .. code:: python

     print(5 > 2)   # True
     print(5 == 2)  # False

Logical Operators
~~~~~~~~~~~~~~~~~

- Combine conditional statements.

- ``and``, ``or``, ``not``

- Example:

  .. code:: python

     x = 5
     print(x > 2 and x < 10)  # True
     print(not(x == 5))       # False

Bitwise Operators
~~~~~~~~~~~~~~~~~

- Perform operations on binary representations.

- ``&`` (AND), ``|`` (OR), ``^`` (XOR), ``~`` (NOT), ``<<`` (Left
  Shift), ``>>`` (Right Shift)

- Example:

  .. code:: python

     a = 5  # 0101
     b = 3  # 0011
     print(a & b)  # 1
     print(a | b)  # 7
     print(a ^ b)  # 6
     print(~a)     # -6
     print(a << 1) # 10
     print(a >> 1) # 2

Assignment Operators
~~~~~~~~~~~~~~~~~~~~

- Assign values to variables.

- ``=``, ``+=``, ``-=``, ``*=``, ``/=``, ``//=``, ``%=``, ``**=``,
  ``&=``, ``|=``, ``^=``, ``>>=``, ``<<=``

- Example:

  .. code:: python

     x = 10
     x += 5  # x = x + 5
     print(x)  # 15

Membership Operators
~~~~~~~~~~~~~~~~~~~~

- Test membership in a sequence (like list, string, tuple).

- ``in``, ``not in``

- Example:

  .. code:: python

     nums = [1, 2, 3]
     print(2 in nums)      # True
     print(4 not in nums)  # True

Identity Operators
~~~~~~~~~~~~~~~~~~

- Compare memory locations of two objects.

- ``is``, ``is not``

- Example:

  .. code:: python

     a = [1, 2]
     b = a
     c = [1, 2]
     print(a is b)      # True
     print(a is c)      # False
     print(a == c)      # True

--------------

2. Expression Evaluation, Precedence & Associativity
----------------------------------------------------

- **Precedence:** Determines the order in which operators are evaluated
  in an expression.
- **Associativity:** Determines the direction (left-to-right or
  right-to-left) in which operators of the same precedence are
  evaluated.
- **Parentheses ``()``** can be used to override the default precedence
  and make expressions clearer.

Operator Precedence Table in Python
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. csv-table:: Python Operator Precedence
   :header: "Precedence Level", "Operators", "Description", "Associativity"
   :widths: 15, 40, 30, 15

   "1 (Highest)", "``()``", "Parentheses (grouping)", "Left-to-right"
   "2", "``**``", "Exponentiation", "Right-to-left"
   "3", "``+x``, ``-x``, ``~x``", "Unary plus, minus, bitwise NOT", "Right-to-left"
   "4", "``*``, ``/``, ``//``, ``%``", "Multiplication, division, modulus", "Left-to-right"
   "5", "``+``, ``-``", "Addition, subtraction", "Left-to-right"
   "6", "``<<``, ``>>``", "Bitwise shift", "Left-to-right"
   "7", "``&``", "Bitwise AND", "Left-to-right"
   "8", "``^``", "Bitwise XOR", "Left-to-right"
   "9", "``|``", "Bitwise OR", "Left-to-right"
   "10", "``==``, ``!=``, ``>``, ``<``, ``>=``, ``<=``, ``is``, ``is not``, ``in``, ``not in``", "Comparisons, identity, membership", "Left-to-right"
   "11", "``not``", "Logical NOT", "Right-to-left"
   "12", "``and``", "Logical AND", "Left-to-right"
   "13", "``or``", "Logical OR", "Left-to-right"
   "14 (Lowest)", "``=``, ``+=``, ``-=``, ``*=``, ``/=``, ``//=``, ``%=``, ``**=``, ``&=``, ``|=``, ``^=``, ``>>=``, ``<<=``", "Assignment operators", "Right-to-left"

Examples
~~~~~~~~

.. code:: python

   result = 2 + 3 * 4      # Multiplication has higher precedence: 2 + (3 * 4) = 14
   result = (2 + 3) * 4    # Parentheses change the order: (2 + 3) * 4 = 20
   result = 2 ** 3 ** 2    # Exponentiation is right-to-left: 2 ** (3 ** 2) = 512
   result = 10 - 4 + 2     # Addition and subtraction are left-to-right: (10 - 4) + 2 = 8

- **Tip:** When in doubt, use parentheses to clarify the intended order
  of evaluation.

--------------

3. Comments in Python
---------------------

Single-line Comments
~~~~~~~~~~~~~~~~~~~~

- Start with ``#``.

- Example:

  .. code:: python

     # This is a single-line comment
     print("Hello")  # This is an inline comment

Multi-line Comments
~~~~~~~~~~~~~~~~~~~

- Use multiple ``#`` lines or triple quotes (``'''`` or ``"""``).

- Example:

  .. code:: python

     # This is a
     # multi-line comment

     '''
     This is also a
     multi-line comment
     '''

- **Tip:** Use comments to explain code logic, especially for complex
  sections.

Docstrings
~~~~~~~~~~

- Use triple quotes (``'''`` or ``"""``) to create docstrings for
  modules, classes, and functions.

- Example:

  .. code:: python

     def add(a, b):
         """
         Adds two numbers.
         """
         return a + b

--------------

*Prepared by Zaid Kamil.*
