# Module

!!! Question "What is module?"

    In Python, a module is a file containing Python code (functions, classes, variables, or executable statements) that can be imported and reused in other programs. Modules help in organizing code logically, improving maintainability, and promoting reusability.

!!! Success "Key Features and types of modules"

    **Key Features:**

    1. **Reusability** – Write once, use multiple times.
    2. **Namespace Separation** – Avoid naming conflicts.
    3. **Organization** – Break large programs into manageable files.

    **Types of Modules:**

    1. **Built-in Modules** – Pre-installed with Python (e.g., ```math```, ```os```, ```sys```).
    2. **User-defined Modules** – Created by users.
    3. **Third-party Modules** – Installed via pip (e.g., numpy, requests).

!!! Abstract "Good to know!"

    **To show all the avalaible modules:**

    ```py
    print(help("modules"))
    ```

    **To list all avalaible variables and function in a module (eg. math):**

    ```py 
    import math
    print(dir("math"))
    ```

    **To show all the descriptions of variables and function within a module (eg. math):**

    ```py 
    import math
    print(help("math"))
    ```

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


## Third-party Modules
Third-party modules are Python packages created and maintained by developers outside of Python's core development team. These modules extend Python's functionality beyond what's available in the standard library. These modules are **not included with Python** and must be installed seperately and often focused on specific domains such as data science, web development, etc with **specialized functionality**. 

!!! info "Popular Third-Party Modules"

    **Data Science & Analytics:**
    
    - ```Numpy```: Numerical computing
    - ```pandas```: Data manipulation and analysis
    - ```matplotlib```: Data visualization
    - ```scikit-learn```: Machine learning

    **Web Development:**

    - ```Django```: High-level web framework
    - ```Flask```: Micro web framework
    - ```requests```: HTTP requests
    - ```BeautifulSoup```: Web scraping

    **Others:**

    - ```Pillow```: Image processing
    - ```pygame```: Game development
    - ```openpyxl```: Excel file manipulation
    - ```selenium```: Web browser automation

    **More details about third-party modules will be discussed individually in other sections !!**

!!! note "How to Use"

    - **Installation** (using pip):
       
       ```bash
       pip install package-name
       ```

    - **Importing** in Python:
       
       ```python
       import numpy as np
       from flask import Flask
       ```


## Built-in Modules
Built-in modules are Python libraries that come pre-installed with Python, providing essential functionality without requiring additional installation. These modules are part of Python's standard library and are **pre-installed**. 

### Random module 
The ```random``` module is a built-in Python module for generating pseudo-random numbers and performing random operations. It's commonly used for simulations, games, statistical sampling, and any application requiring randomization.

!!! example 

    === "Basic Random Numbers"

        ```random()``` **- Returns float between 0.0 and 1.0**

        ```py
        import random
        print(random.random())  # e.g., 0.5488135039273248
        ```

        ```uniform(a, b)``` **- Returns float between a and b**

        ```py
        import random
        print(random.uniform(1, 10))  # e.g., 5.711324
        ```

    === "Integer Generation"

        ```randint(a, b)``` **- Random integer between a and b (inclusive)**

        ```py 
        import random
        print(random.randint(1, 6))  # Simulate dice roll (1-6)
        ```

        ```randrange(start, stop, step)``` **- Random element from range()**
        
        ```py
        import random
        print(random.randrange(0, 100, 5))  # Multiple of 5 between 0-100
        ```

        **For large ranges, ```randrange()``` is more efficient than ```randint()```!**

    === "Sequence Operations"

        ```choice(seq)``` **- Random element from non-empty sequence**

        ```py 
        import random
        colors = ['red', 'green', 'blue']
        print(random.choice(colors))  # e.g., 'green'
        ```

        ```shuffle(seq)``` **- Shuffle sequence in place**
        
        ```py
        import random
        cards = list(range(1, 11))  # [1, 2, 3,...10]
        random.shuffle(cards)
        print(cards)  # e.g., [7, 2, 9, 1,...]
        ```

        ```sample(population, k)``` **- k unique random elements**
        
        ```py
        import random
        print(random.sample(range(100), 5))  # 5 unique numbers 0-99
        ```

    === "Seeding (Reproducibility)"

        ```seed()``` **- Random integer between a and b (inclusive)**

        ```py 
        random.seed(42)  # Initialize with fixed seed
        print(random.random())  # Always 0.6394267984578837 with seed 42
        ```

    === "Statistical Distributions"

        - ```gauss(mu, sigma)``` - Gaussian distribution
        - ```expovariate(lambd)``` - Exponential distribution
        - ```betavariate(alpha, beta)``` - Beta distribution

    For the entire list you may refer to [Source: W3Schools](https://www.w3schools.com/python/module_random.asp)

### Math module
The ```math``` module is a built-in Python module that provides mathematical functions and constants. It's essential for scientific computing, data analysis, and any application requiring advanced mathematical operations.

!!! Success "Make sure you import the module!"

    ```py 
    import math
    ```

!!! example 

    === "Commonly Used Constants"

        ```py 
        math.pi       # π (pi) ≈ 3.141592653589793
        math.e        # Euler's number ≈ 2.718281828459045
        math.tau      # Tau (2π) ≈ 6.283185307179586
        math.inf      # Infinity
        math.nan      # Not a Number
        ```

    === "Number-Theoretic and Representation Functions"

        ```py
        math.ceil(x)    # Smallest integer ≥ x
        math.floor(x)   # Largest integer ≤ x
        math.trunc(x)   # Truncates x to an integer
        math.fabs(x)    # Absolute value as float
        math.factorial(x) # Factorial of x
        math.gcd(a, b)  # Greatest common divisor
        math.isfinite(x) # Check if x is finite
        math.isinf(x)    # Check if x is infinity
        math.isnan(x)    # Check if x is NaN
        ```

    === "Power and Logarithmic Functions"

        ```py
        math.pow(x, y)   # x raised to power y
        math.sqrt(x)     # Square root of x
        math.exp(x)      # e raised to power x
        math.log(x[, base]) # Logarithm of x (default base e)
        math.log10(x)    # Base-10 logarithm
        math.log2(x)     # Base-2 logarithm
        ```

    === "Trigonometric Functions"

        ```py
        math.sin(x)     # Sine of x radians
        math.cos(x)     # Cosine of x radians
        math.tan(x)     # Tangent of x radians
        math.asin(x)    # Arc sine (in radians)
        math.acos(x)    # Arc cosine (in radians)
        math.atan(x)    # Arc tangent (in radians)
        math.atan2(y, x) # atan(y / x) in radians
        math.hypot(x, y) # Euclidean distance (sqrt(x² + y²))
        ```

    === "Angular Conversion"

        ```py
        math.degrees(x)  # Convert radians to degrees
        math.radians(x)  # Convert degrees to radians
        ```

    === "Hyperbolic Functions"

        ```py
        math.sinh(x)    # Hyperbolic sine
        math.cosh(x)    # Hyperbolic cosine
        math.tanh(x)    # Hyperbolic tangent
        math.asinh(x)   # Inverse hyperbolic sine
        math.acosh(x)   # Inverse hyperbolic cosine
        math.atanh(x)   # Inverse hyperbolic tangent
        ```

    === "Special Functions"

        ```py
        math.erf(x)     # Error function
        math.erfc(x)    # Complementary error function
        math.gamma(x)   # Gamma function
        math.lgamma(x)  # Natural log of absolute value of Gamma
        ```
    For the entire list you may refer to [Source: W3Schools](https://www.w3schools.com/python/module_math.asp)

    


















