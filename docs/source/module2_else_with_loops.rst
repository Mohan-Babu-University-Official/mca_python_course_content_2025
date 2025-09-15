.. _module2_else_with_loops:

else with Loops
===============

In Python, you can use `else` with loops. The `else` block executes when the loop completes normally (not terminated by `break`).

`else` with `for` Loop
----------------------

.. code-block:: python

   for i in range(5):
       print(i)
   else:
       print("Loop completed successfully")

`else` with `while` Loop
------------------------

.. code-block:: python

   count = 0
   while count < 5:
       print(count)
       count += 1
   else:
       print("While loop completed")

`else` with `break`
-------------------

If the loop is terminated by `break`, the `else` block is not executed.

.. code-block:: python

   for i in range(10):
       if i == 5:
           print("Breaking at", i)
           break
       print(i)
   else:
       print("This won't be printed because of break")

Use Cases
---------

The `else` with loops is useful for:

- Checking if a loop completed without finding something
- Performing actions after successful iteration
- Handling cases where no `break` occurred

.. code-block:: python

   # Example: Finding an item
   numbers = [1, 3, 5, 7, 9]
   target = 4
   for num in numbers:
       if num == target:
           print("Found", target)
           break
   else:
       print(target, "not found in the list")