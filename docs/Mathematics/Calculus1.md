# Calculus 1
Python is a powerful tool for performing calculus operations, both symbolically (using libraries like SymPy) and numerically (using libraries like NumPy and SciPy).

!!! Info

    **Symbolic Calculus with SymPy:**

    SymPy is a Python library for symbolic mathematics that can perform calculus operations like differentiation, integration, limits, and series expansions. To install the SymPy module:

    ```py
    pip install sympy
    ```

    **Numerical Calculus with NumPy/SciPy:**

    For numerical computations, we can use NumPy and SciPy. To install the modules:

    ```py
    pip install numpy scipy
    ```

## Limits 
Limits are fundamental in calculus, and Python provides excellent tools for computing them both symbolically (using SymPy) and numerically (using NumPy/SciPy). Here's how to work with limits in Python:

### Hole in a graph 
A hole in a graph occurs when a rational function has a common factor in its numerator and denominator that cancels out, creating a single point where the function is undefined. These are also called "removable discontinuities". For example, 

!!! example

    **Given the equation:**

    $$ y = \frac{3(x - 2)}{(x - 2)} $$

    **To solve this in python:**

    ```py
    x = 2
    h = 0.00001
    

    ```




























