# Module

!!! Question "What is module?"

    In Python, a module is a file containing Python code (functions, classes, variables, or executable statements) that can be imported and reused in other programs. Modules help in organizing code logically, improving maintainability, and promoting reusability.

!!! Abstract "Key Features and types of modules"

    **Key Features:**

    1. **Reusability** – Write once, use multiple times.
    2. **Namespace Separation** – Avoid naming conflicts.
    3. **Organization** – Break large programs into manageable files.

    **Types of Modules:**

    1. **Built-in Modules** – Pre-installed with Python (e.g., ```math```, ```os```, ```sys```).
    2. **User-defined Modules** – Created by users.
    3. **Third-party Modules** – Installed via pip (e.g., numpy, requests).

## User-defined Modules
User-defined modules are Python files created by programmers to organize and reuse their own code.

!!! tip "How to create?"

    1. Create a new Python file (with ```.py``` extension)
    2. Write your functions, classes, or variables in this file
    3. Save it in the same directory as your main script or in Python's path

!!! example "Step-by-Step Example"

    **1. Create a Module (```mymodule.py```)**

       ```py 
       # mymodule.py
       def greet(name):
           return f"Hello, {name}!"

       PI = 3.14159
       ```
    
    **2. Import and Use the Module**

      ```py 
      # main.py
      import mymodule

      print(mymodule.greet("Alice"))  # Output: Hello, Alice!
      print(mymodule.PI)              # Output: 3.14159
      ```

      **Alternative Import methods**

      ```py 
      # Import specific attributes
      from mymodule import greet, PI
      print(greet("Bob"))  # No need for 'mymodule.' prefix

      # Import with an alias
      import mymodule as mm
      print(mm.greet("Charlie"))

      # Import everything (not recommended)
      from mymodule import *
      print(greet("Dave"))
      ```



