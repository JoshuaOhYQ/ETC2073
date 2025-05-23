# Control Flow

## If-Else-Elif 
For the program to make a decision on whether to execute the code or not, we can use the if, else if (elif) and else statements! If statements do some code (IF some condition is **True**), else it will do something else:

!!! example

    === "Integers and Float"

        ``` py
        age = int(input("Enter your age: "))

        if age >= 100:
            print("You are too old to sign up!")

        elif age >= 18;
            print("You are now signed up!")

        elif age <= 0:
            print("You haven't been borned yet!)

        else:
            print("You are too young to sign up!")
        ```
        Output (if the input = 100):
        ```
        Enter your age: 100
        You are too old to sign up!
        ```
        Output (if the input = 30):
        ```
        Enter your age: 30
        You are now signed up!
        ```
        

    === "String"

        ``` py
        response = input("Would you like some food (Y/N)?: ")

        if response == "Y":
            print("Have some food!")

        else:
            print("No food for you!")
        ```
        Output (if the input = N): 
        ```
        Would you like some food (Y/N): N
        No food for you!
        ```
        
    === "Booleans"

        ``` py
        for_sale = True

        if for_sale:
            print("This item is for sale!")

        else:
            print("This item is not for sale!")
        ```
        Output: 
        ```
        This item is for sale!
        ```

!!! Warning

    The decision must be written in order from **top to bottom**, as Python will read the code line by line and will priotize the decision on top first!



    

## Logical Operators
For the program to evaluate multiple conditions at once, the operators of **or, and, not** can be used! Here's how can we use them: 

!!! notes

    Here is the general definition for the logical operators **OR, AND, NOT**:

    | **Operator**     | **Description**                          |
    | ----------- | ------------------------------------ |
    | OR           | at least one condition must be True  |
    | AND       | both conditions must be True|
    | NOT    | Inverts the condition, for example not False, not True |


!!! example

    === "OR"

        ``` py
        temp = 25
        is_raining = False

        if temp > 35 or temp < 0 or is_raining:
            print("The outdoor event is cancelled")
        else:
            print("The outdoor event is still scheduled")

        ```
        Output:
        ```
        The outdoor event is still scheduled
        ```

        Similary, if we change the **is_raining** boolean value :material-weather-lightning-rainy:: 

        ``` py
        temp = 25
        is_raining = True

        if temp > 35 or temp < 0 or is_raining:
            print("The outdoor event is cancelled")
        else:
            print("The outdoor event is still scheduled")

        ```
        Output:
        ```
        The outdoor event is cancelled
        ```


    === "AND"

        ``` py
        temp = 30
        is_sunny = True

        if temp >= 28 and is_sunny:
            print("It is HOT outside")
            print("It is SUNNY")

        elif temp <= 0 and is_sunny: 
            print("It is COLD outside")
            print("It is SUNNY")
        ```
        Output: 
        ```
        It is HOT outside
        It is SUNNY
        ```

        Similary, if we change the **temp** value :material-thermometer-lines:: 

        ``` py
        temp = -3
        is_sunny = True

        if temp >= 28 and is_sunny:
            print("It is HOT outside")
            print("It is SUNNY")

        elif temp <= 0 and is_sunny: 
            print("It is COLD outside")
            print("It is SUNNY")
        ```
        Output: 
        ```
        It is COLD outside
        It is SUNNY
        ```
        
    === "NOT"

        ``` py
        temp = -3
        is_sunny = False

        if temp >= 28 and not is_sunny:
            print("It is HOT outside")
            print("It is CLOUDY")

        elif temp <= 0 and not is_sunny: 
            print("It is COLD outside")
            print("It is CLOUDY")
        ```
        Output: 
        ```
        It is COLD outside
        It is CLOUDY
        ```


## Conditional Expressions
This is also known as the ternary operator. It is a one-line shortcut for the if-else statement. So, instead of writing multiple lines of if-else codes, we can reduce the lines of codes with this expression! This allow Python to print or assign one of two values based on a condition:

!!! notes

    The formula is:
    ```py
    X if condition else Y
    ```

!!! example

    ```py
    num = 5 
    result = "Even" if num % 2 == 0 else "Odd"

    print(result)
    ```
    Output:
    ```
    Odd
    ```


## While Loops
Loops allow us to execute a block of code repeatedly as long as a specified condition is met. If we use a while loop, Python will execute some code indented within the while loop, **WHILE** some condition remains true:

!!! example

    === "1"

        ``` py
        name = input("Enter your name: ")
        
        while name == "":
            print("You did not enter your name!")
            name = input("Enter your name: ")

        print(f"Hello {name}")   
        ```
        Output:
        ```
        Enter your name:
        You did not enter your name!
        Enter your name:
        You did not enter your name!
        Enter your name: John
        Hello John
        ```


    === "2"

        ``` py
        age = int(input("Enter your age: "))

        while age < 0:
            print("Age can't be negative")
            age = int(input("Enter your age: "))
        
        print(f"You are {age} years old")
        ```
        Output: 
        ```
        Enter your age: -1
        Age can't be negative
        Enter your age: 21
        You are 21 years old
        ```

        
    === "3"

        ``` py
        food = input("Enter a food you like (q to quit): ")

        while not food == "q":
            print(f"You like {food}")
            food = input("Enter another food you like (q to quit): ")
        
        print("bye")
        ```
        Output: 
        ```
        Enter a food you like (q to quit): pizza
        You like pizza
        Enter another food you like (q to quit): hotdog
        You like hotdog
        Enter another food you like (q to quit): q
        bye
        ```

!!! Warning

    Make sure the code has some way to exit out of the loop to prevent **infinite loop**!

!!! Notes

    Loops help automate repetitive tasks, making code more efficient and concise, but must be carefully used to prevent infinite loops!


## For Loops
Besides while loops, there is also for loops. It is used when the number of iterations is known in advance. When a for loop is used, Python execute a block of code a fixed number of times. You can iterate over a range, string, sequence, etc:

!!! example

    === "Range Function"

        ``` py
        for x in range(1, 11):
            print(x) 
        ```
        Output:
        ```
        1
        2
        3
        4
        5
        6
        7
        8
        9
        10
        ```

        What if we want it to print backwards:


        ``` py
        for x in reversed(range(1, 11)):
            print(x) 

        print("Happy New Year")
        ```
        Output:
        ```
        10
        9
        8
        7
        6
        5
        4
        3
        2
        1
        Happy New Year
        ```
        
        What if we want to increase the step for counting x:

        ``` py
        for x in range(1, 11, 2):
            print(x) 
        ```
        Output:
        ```
        1
        3
        5
        7
        9
        ```


    === "String"

        ``` py
        credit_card = "1234-5678-9012-3456"

        for x in credit_card:
            print(x)
        ```
        Output: 
        ```
        1
        2
        3
        4
        -
        5
        6
        7
        8
        -
        9
        0
        1
        2
        -
        3
        4
        5
        6
        ```

## Continue-Break
```continue``` and ```break``` are loop control statements used to modify the flow of loops (```for``` and ```while```):

!!! example

    === "break"

        This statement stops the loop immediately and exits it, even if the loop condition is still true. Basically it is used to terminate a loop prematurely:

        ``` py
        for x in range(1, 21):
            if x == 13:
                break
            else:
                print(x)
        ```
        Output:
        ```
        1
        2
        3
        4
        5
        6
        7
        8
        9
        10
        11
        12
        ```


    === "continue"

        This statement skips the current iteration and moves to the next one. Basically, it is used to skip specific values without exiting the loop entirely:

        ``` py
        for x in range(1, 21):
            if x == 13:
                continue
            else:
                print(x)
        ```
        Output: 
        ```
        1
        2
        3
        4
        5
        6
        7
        8
        9
        10
        11
        12
        14
        15
        16
        17
        18
        19
        20
        ```

## Nested loops
Nested loop is a loop inside another loop. It is used when you need to perform repetitive tasks within repetitive tasks, such as working with multi-dimensional data, for example matrices, tables, grids, etc. Python reads nested loop on a specific format:

!!! notes
    - The **outer loop** runs once, triggering the **inner loop** to complete all its iterations.
    - This repeats until the outer loop finishes.
    - In simple words, **inner loop** completes all iterations for each **outer loop** iteration.
    - Total runs = (Outer loop iterations) × (Inner loop iterations)
    - We can have different format of nested loops, for example while loop inside of a while loop, for loop inside of a for loop, while loop inside of a for loop, etc. 

!!! example

    === "1"

        ``` py
        for x in range(1, 10):
            for y in range(1, 10):
                print(y, end="")
            print()
        ```
        Output:
        ```
        123456789
        123456789
        123456789
        ```


    === "2"

        ``` py
        rows = int(input("Enter the # of rows: "))
        columns = int(input("Enter the # of columns: "))
        symbol = input("Enter a symbol to use: ")

        for x in range(rows):
            for y in range(columns):
                print(symbol, end="")
            print()
        ```
        Output: 
        ```
        Enter the # of rows: 4
        Enter the # of columns: 10
        Enter a symbol to use: $
        $$$$$$$$$$
        $$$$$$$$$$
        $$$$$$$$$$
        $$$$$$$$$$
        ```


    === "3"

        ``` py
        i = 1
        while <= 3:
            j = 1
            while j <= 2:
                print(i, j)
                j += 1
            i += 1
        ```
        Output: 
        ```
        1 1
        1 2
        2 1
        2 2
        3 1
        3 2
        ```

!!! Warning

    Avoid using too many nested loops (e.g., 3+ levels) as it can slow down your program and increase complexity!


## Match-case statement 
```Match-case statement``` provides pattern matching capabilities similar to switch-case statements in other languages. It is an alternative to using many ```elif``` statements. It executes some code if a value matches a ```case```. 

!!! success "key features"

    - More powerful than traditional switch-case statements
    - Can match patterns, not just values
    - Supports destructuring of data structures
    - Can include conditions (guards) in patterns
    - Works with custom classes
    - The _ acts as a wildcard/catch-all pattern

!!! Info "Basic Syntax"

    ```py
    match subject:
        case pattern1:
            # handle pattern1
        case pattern2:
            # handle pattern2
        case _:
            # default case
    ```

!!! example 

    === "Simple value matching"

        ```py
        def http_status(status):
            match status:
                case 200:
                    return "OK"
                case 404:
                    return "Not found"
                case 500:
                    return "Server error"
                case _:
                    return "Unknown status"
        ```

    === "Pattern matching with types"

        ```py
        def check_type(value):
            match value:
                case int():
                    print("Got an integer")
                case str():
                    print("Got a string")
                case list():
                    print("Got a list")
                case _:
                    print("Unknown type")
        ```

    === "Matching sequences and collections"

        ```py
        def process_list(lst):
            match lst:
                case [first, second, *rest]:
                    print(f"First: {first}, Second: {second}, Rest: {rest}")
                case [single]:
                    print(f"Single element: {single}")
                case []:
                    print("Empty list")
        ```

    === "Matching dictionaries"

        ```py
        def process_dict(d):
            match d:
                case {"name": name, "age": age}:
                    print(f"Name: {name}, Age: {age}")
                case {"user": user}:
                    print(f"User: {user}")
                case _:
                    print("Unknown dictionary format")
        ```

    === "Matching with conditions (guards)"

        ```py
        def check_number(n):
            match n:
                case x if x < 0:
                    print("Negative")
                case 0:
                    print("Zero")
                case x if x > 0:
                    print("Positive")
        ```

    === "Matching class objects"

        ```py
        class Point:
            def __init__(self, x, y):
                self.x = x
                self.y = y

        def check_point(p):
            match p:
                case Point(x=0, y=0):
                    print("Origin")
                case Point(x=0, y=y):
                    print(f"On Y axis at {y}")
                case Point(x=x, y=0):
                    print(f"On X axis at {x}")
                case Point(x=x, y=y):
                    print(f"Point at ({x}, {y})")
                case _:
                    print("Not a point")
        ```
        

## Function 
A function in Python is a reusable block of code that performs a specific task. Functions help in organizing code, improving readability, and avoiding repetition.

!!! info 

    - Use the ```def``` keyword to define a function.
    - place ```()``` after the function name to invoke it. 
    - Parameters specify what input a function expects to receive and they allow functions to work with different input values each time they're called. There are different types of parameters which we will go through in the next section!
    - The ```return``` statement is used in functions to specify the value that the function should output or "give back" when it's called and end a function.
    - Not all functions need a return statement (functions without one return ```None``` by default)


!!! example

    === "Basic function"

        ``` py
        def happy_birthday():
            print("Happy birthday to you!")
            print("You are old!")
            print("Happy birthday to you!")
            print()

        happy_birthday()
        happy_birthday()
        happy_birthday()


        ```
        Output:
        ```
        Happy birthday to you!
        You are old!
        Happy birthday to you!

        Happy birthday to you!
        You are old!
        Happy birthday to you!

        Happy birthday to you!
        You are old!
        Happy birthday to you!
        ```


    === "Function with parameter"

        ``` py
        def happy_birthday(name):
            print(f"Happy birthday to {name}!")
            print("You are old!")
            print("Happy birthday to you!")
            print()

        happy_birthday("John")
        happy_birthday("Josh")
        happy_birthday("Steve")
        ```
        Output: 
        ```
        Happy birthday to John!
        You are old!
        Happy birthday to you!

        Happy birthday to Josh!
        You are old!
        Happy birthday to you!

        Happy birthday to Steve!
        You are old!
        Happy birthday to you!
        ```


    === "Function with multiple parameters"

        ``` py
        def happy_birthday(name, age):
            print(f"Happy birthday to {name}!")
            print(f"You are {age} years old!")
            print("Happy birthday to you!")
            print()

        happy_birthday("John", 20)
        happy_birthday("Josh", 30)
        happy_birthday("Steve", 40)
        ```
        Output: 
        ```
        Happy birthday to John!
        You are 20 years old!
        Happy birthday to you!

        Happy birthday to Josh!
        You are 30 years old!
        Happy birthday to you!

        Happy birthday to Steve!
        You are 40 years old!
        Happy birthday to you!

        ```


    === "Function with return statement"

        **Working with float/integers:**

        ``` py
        def add(x, y):
            z = x + y
            return z

        def subtract(x, y):
            z = x - y
            return z

        def multiply(x, y):
            z = x * y
            return z

        def divide(x, y):
            z = x / y
            return z

        print(add(1, 2))
        print(subtract(1, 2))
        print(multiply(1, 2))
        print(divide(1, 2))
        ```
        Output: 
        ```
        3
        -1
        2
        0.5
        ```

        **Working with strings:**

        ``` py
        def create_name(first, last):
            first = first.capitalize()
            last = last.capitalize()
            return first + " " + last
        
        full_name = create_name("john", "cena")
        print(full_name)
        ```
        Output: 
        ```
        John Cena
        ```

## Positional Arguments 
Positional arguments are the most basic type of arguments in Python functions. They are called "positional" because their meaning is determined by their position in the function call. Positional arguments must be passed in the exact order that the function parameters are defined.

!!! tip "Key Characteristics"

    1. **Order matters:** The first argument corresponds to the first parameter, second to second, etc.
    2. **Required by default:** You must provide values for all positional arguments unless they have default values.

!!! example 

    ```py 
    def greet(name, greeting):
    print(f"{greeting}, {name}!")

    greet("Alice", "Hello")  # Correct order
    # Output: Hello, Alice!

    greet("Hello", "Alice")  # Wrong order - logical error
    # Output: Alice, Hello!
    ```
    Output:
    ```
    Hello, Alice!
    Alice, Hello!
    ```
    

## Default Arguments 
Default arguments in Python allow you to specify default values for function parameters. If the caller doesn't provide a value for that parameter, the default value is used instead.

!!! Question "Why Default Arguments?!?"

    Default arguments make your functions more flexible, reduces number of arguments while maintaining backward compatibility with existing calls!

!!! info "Key Points About Default Arguments"

    1. **Order matters:** Parameters with default arguments must come after non-default parameters.

        ```py
        # Correct
        def func(a, b=1):
            pass

        # Wrong
        def func(a=1, b):
            pass
        ```

    2. **Mutable defaults are dangerous:** Default arguments are evaluated only once when the function is defined, not each time it's called. This can cause issues with mutable defaults.
    
        ```py
        def append_to(element, lst=[]):
            lst.append(element)
            return lst

        print(append_to(1))  # [1]
        print(append_to(2))  # [1, 2] - probably not what you wanted!
        ```

        Better approach:
        ```py
        def append_to(element, lst=None):
            if lst is None:
                lst = []
            lst.append(element)
            return lst
        ```

    3. **Default arguments can be any expression**

    4. **Overriding defaults:** You can override defaults by passing a different value.


!!! example

    === "1"

        ```py 
        def net_price(list_price, discount=0, tax=0.05):
            return list_price * (1 - discount) * (1 + tax)

        print(net_price(500))         # using default arg.
        print(net_price(500, 0.1))    # overriding defaults
        print(net_price(500, 0.1, 0)) # overriding defaults
        ```
        Output:
        ```
        525.0
        472.5
        450.0
        ```


    === "2.1" 

        ```py
        import time 

        def count(end, start=0):
            for x  in range(start, end+1):
                print(x)
                time.sleep(1) 
            print("Done!")           

        count(10)                       # using default arg.
        ```
        Output:
        ```
        0
        1
        2
        3
        4
        5
        6
        7
        8
        9
        10
        Done!
        ```

    
    === "2.2"

        ```py
        import time 

        def count(end, start=0):
            for x  in range(start, end+1):
                print(x)
                time.sleep(1) 
            print("Done!")

        count(30, 15)            # overriding defaults
        ```
        Output:
        ```
        15
        16
        17
        18
        19
        20
        21
        22
        23
        24
        25
        26
        27
        28
        29
        30
        Done!
        ```


## Keyword Arguments
Keyword arguments (also called named arguments) allow you to pass arguments to a function by explicitly specifying the parameter names and preceded by an identifier. Unlike positional arguments, the order doesn't matter when using keyword arguments.

!!! Sucess "Key Features"

    1. **Clarity:** Makes code more readable by showing what each argument represents
    2. **Flexibility:** Allows you to specify arguments in any order
    3. **Default values:** Often used with parameters that have default values
    4. **Combination with positional args:** Can be mixed with positional arguments (positional args must come first) 
       
       ```py
       def register_user(name, email, phone=None, country="US"):
            print(f"Registering {name} ({email}), Phone: {phone}, Country: {country}")

       # Valid calls
       register_user("Alice", "alice@example.com")  # positional
       register_user("Bob", "bob@example.com", country="UK")  # mixed
       register_user(name="Charlie", email="charlie@example.com")  # keyword
       ```

!!! example

    === "Self-Written"

        **Example 1:**

        ```py
        def hello(greeting, title, first, last):
            print(f"{greeting} {title}{first} {last}")
        
        hello(greeting="Hello", last="Squarepants", first="Spongebob", title="Mr.")
        ```
        Output:
        ```
        Hello Mr.Spongebob Squarepants
        ```

        **Example 2:**

        ```py
        def describe_pet(animal_type, pet_name):
            print(f"I have a {animal_type} named {pet_name}.")

        # Using keyword arguments (order doesn't matter)
        describe_pet(pet_name="Whiskers", animal_type="cat")
        describe_pet(animal_type="dog", pet_name="Rover")
        ```
        Output:
        ```
        I have a cat named Whiskers.
        I have a dog named Rover.
        ```


    === "Built-in"

        **End Keyword argument:**

        ```py
        for x in range(1, 11):
            print(x, end=" ")        # end is a built in keyword arg. in print function
        ```
        Output:
        ```
        1 2 3 4 5 6 7 8 9 10 
        ```

        **Seperate Keyword argument:**

        ```py
            print("1", "2", "3", "4", "5", sep="-")        # sep is a built in keyword arg. in print function
        ```
        Output:
        ```
        1-2-3-4-5
        ```

!!! abstract "Other Details"

    === "Forced keyword arguments"

        **You can force arguments to be keyword-only by using ``*`` in the parameter list:**

        ```py
        def create_profile(name, *, age, occupation):
            print(f"{name}, {age}, {occupation}")

        create_profile("Alice", age=30, occupation="Engineer")  # Valid
        create_profile("Bob", 25, "Teacher")  # Error: age and occupation must be keyword args
        ```

    === "Common Use Cases"

        - Functions with many parameters:

           ```py 
           def draw_rectangle(x, y, width, height, *, fill_color="black", border_color="gray", border_width=1):
                 # implementation
           ```

        - APIs where parameter names are meaningful:
           
           ```py 
           requests.get(url, params=None, headers=None, timeout=None)
           ```

        - Functions where most parameters are optional:

           ```py
           def format_text(text, *, bold=False, italic=False, color="black"):
                # implementation
           ```


## Arbitary Arguments (Args-Kwargs)
Python provides two ways to handle an arbitrary (variable) number of arguments in functions:

!!! example 

    === "Arbitrary Positional Arguments (```*args```)"

        - Allow you to pass multiple non-key arguments
        - Collects extra positional arguments into a tuple

        ```py
        def sum_numbers(*args):
            total = 0
            for num in args:
                total += num
            return total

        print(sum_numbers(1, 2, 3))        # Output: 6
        print(sum_numbers(10, 20, 30, 40)) # Output: 100
        ```
        Output:
        ```
        6
        100
        ```

        **Features:**

        - The ```*args``` parameter must come after regular parameters
        - You can name it anything (the ```*``` is what matters), but ```args``` is convention
        - Useful when you don't know how many arguments might be passed




    === "Arbitrary Keyword Arguments (```**kwargs```)"

        - Allow you to pass multiple keyword-arguments
        - Collects extra keyword arguments into a dictionary

        ```py
        def print_user_info(**kwargs):
            for key, value in kwargs.items():
                print(f"{key}: {value}")

        print_user_info(name="Alice", age=25, occupation="Engineer")
        # Output:
        # name: Alice
        # age: 25
        # occupation: Engineer
        ```
        Output:
        ```
        name: Alice
        age: 25
        occupation: Engineer
        ```

        **Features:**

        - The ```**kwargs``` parameter must come after all other parameters
        - You can name it anything (the ```**``` is what matters), but ```kwargs``` is convention
        - Useful for functions that need to handle named parameters flexibly

    
    === "Combining Both"

        **Example 1:**

        ```py 
        def process_data(name, age, *scores, **properties):
            print(f"Name: {name}")
            print(f"Age: {age}")
            print(f"Scores: {scores}")
            print(f"Properties: {properties}")

        process_data("Bob", 30, 85, 92, 78, department="IT", role="Developer")
        ```
        Output:
        ```
        Name: Bob
        Age: 30
        Scores: (85, 92, 78)
        Properties: {'department': 'IT', 'role': 'Developer'}
        ```

        **Example 2:**

        ```py 
        def shipping_label(*args, **kwargs):
            for arg in args:
                print(arg,end=" ")
            print()

            if "apt" in kwargs:
                print(f"{kwargs.get('street')} {kwargs.get('apt')}")

            elif "PObox" in kwargs:
                print(f"{kwargs.get('street')}")
                print(f"{kwargs.get('PObox')}")

            else:
                print(f"{kwargs.get('street')}")

            print(f"{kwargs.get('city')} {kwargs.get('state')}, {kwargs.get('zip')}")

        shipping_label("Dr.", "Spongebob", "Squarepants",
                       street="123 Fake St.",
                       apt="#100",
                       city="Detroit",
                       state="MI",
                       zip="54321")
        ```
        Output:
        ```
        Dr Spongebob Squarepants
        123 Fake St. #100
        Detroit MI, 54321
        ```


## Recursive Functions
A recursive function is a function that calls itself in its definition. It's a powerful programming technique that can solve problems by breaking them down into smaller, similar subproblems.

!!! info "Key Characteristics"

    1. **Base case:** Should be defined in every recursive function, as having a base case helps to avoid infinite recursions.

    2. **Recursive case:** The function calls itself with a modified input that moves toward the base case. 

!!! example

    === "Factorial Function"

        ```py 
        def factorial(n):
            # Base case
            if n == 0 or n == 1:
                return 1
            # Recursive case
            else:
                return n * factorial(n - 1)

        print(factorial(5))
        # call stack:  [{'input': 5}]
        # call stack:  [{'input': 4}]
        # call stack:  [{'input': 3}]
        # call stack:  [{'input': 2}]
        # base case reached! Num is 1.
        # 120
        ```

        Output:

        ```
        120
        ```

    === "Fibonacci Sequence"

        ```py
        def fibonacci(n):
            # Base cases
            if n == 0:
                return 0
            elif n == 1:
                return 1
            # Recursive case
            else:
                return fibonacci(n - 1) + fibonacci(n - 2)

        print(fibonacci(6))
        ```

        Output:

        ```
        8
        ```


!!! Warning "Important Considerations"

    1. **Termination Condition:** Without a proper base case, the function will recurse infinitely

    2. **Stack Overflow:** Deep recursion may hit language recursion depth limits

    3. **Memory Usage:** Each recursive call adds to the call stack

    4. **Performance:** Some recursive solutions can be inefficient 


## Scope Resolution
Scope resolution in Python determines how variables are looked up and where they can be accessed. Python follows the LEGB rule for name resolution:

!!! Info "LEGB Rule (Order of Scope Resolution)" 

    1. **L (Local):** Names defined inside the current function

    2. **E (Enclosing):** Names in the local scope of enclosing functions (for nested functions)

    3. **G (Global):** Names defined at the module level

    4. **B (Built-in):** Names built into Python (eg. value of PI in math module)

!!! example "Example of LEGB"

    === "Local"

        ```py
        def my_func():
        x = 10  # Local variable
        print(x)
        ```

    === "Enclosing Scope"

        ```py
        def outer():
            x = 10  # Enclosing scope variable
        
            def inner():
                print(x)  # Accesses x from enclosing scope
            
            inner()
        ```

    === "Global Scope"

        ```py
        x = 10  # Global variable

        def my_func():
            print(x)  # Accesses global x
        ```

    === "Built-in Scope"

        ```py
        def my_func():
            print(len([1, 2, 3]))  # len is a built-in function
        ```

!!! example "Modifying Scope Behavior"

    === "Global"

        **Modify a global variable from a local scope**

        ```py
        x = 10

        def my_func():
            global x
            x = 20  # Modifies the global x
            print(x)

        my_func()
        ```

        Output:

        ```py
        20
        ```

    === "Nonlocal"

        **Modify a variable from an enclosing (non-global) scope**

        ```py
        def outer():
            x = 10
            
            def inner():
                nonlocal x
                x = 20  # Modifies outer's x
            
            inner()
            print(x)  # Prints 20

        outer()
        ```

        Output:

        ```py
        20
        ```


## If __name__ == "__main__"
This Python idiom checks if a script is being run directly (rather than imported as a module). This also prevents the code from running when the file is imported as a module, while allowing it to run when executed directly. In simple words, **sometimes we want the functionality of a program without executing the main body of code**, for example a python library (math module).

!!! tip "Key Points"

    1. **Double equals (==):** You used a single equals (=), which is assignment. You need the comparison operator ==.

    2. **Double underscores:** "name" has two underscores on each side.

    3. **Quotes around "main":** The string should be in quotes (either single or double).

!!! Abstract "How It Works"

    - When a Python script runs directly, its ```__name__``` is set to ```"__main__"```

    - When imported as a module, ```__name__``` is set to the module's name

!!! example

    === "Common Usage"

        ```py
        def main():
            # Your main program logic here
            print("This is the main function")

        if __name__ == "__main__":
            main()
        ```

    === "Multiple Modules **(without the idiom)**"

        **If we don't use ```if __name__ == "__main__"``` -**

        **script1:**

        ```py 
        def favourite_food(food):
            print(f"Your favourite food is {food}")
        
        print("This is script 1")
        favourite_food("pizza")
        print("Goodbye!")
        ```

        **script2:**

        ```py
        from script1 import *
        ```

        **Now we run script2, the output will show:**

        ```
        This is script1
        Your favourite food is pizza 
        Goodbye!
        ```

    === "Multiple Modules **(with the idiom)**"

        **If we use ```if __name__ == "__main__"``` -**

        **script1:**

        ```py 
        def favourite_food(food):
            print(f"Your favourite food is {food}")
        
        def main():
            print("This is script 1")
            favourite_food("pizza")
            print("Goodbye!")

        if __name__ == '__main__':
            main()
        ```

        **script2:**

        ```py
        from script1 import *

        def favourite_drink(drink):
            print(f"Your favourite drink is {drink}")

        print("This is script2")
        favourite_food("sushi")
        favourite_drink("coffee")
        print("Goodbye!")
        ```

        **Now we run script2, the output will show:**

        ```
        This is script2
        Your favourite food is sushi
        Your favourite drink is coffee 
        Goodbye!
        ```

!!! Success 

    It is good practice to include this idiom of ```if __name__ == "__main__```, as **it makes your code more modular, helps with readability, leaves no global variable and avoid any unintended execution** !

## Lambda function 
A lambda function (also called an anonymous function) is a small, unnamed function defined using the ```lambda``` keyword in Python. It can take any number of arguments but must consist of a single expression. Unlike regular functions defined with ```def```, lambda functions don’t have a name and are usually used in situations where you need a simple function for a short period of time.


!!! info "Key Characteristics"

    1. **Anonymous:** It doesn’t have a name (unless assigned to a variable).

    2. **Single Expression:** Can only contain one expression (no statements like if, for, etc.).

    3. **Inline Usage:** Often used where a short function is needed temporarily.

    4. It is also commonly used as **arguments** to higher-order functions such as ```map()```, ```filter()```, and ```sorted()```.
    

!!! Abstract "Basic Syntax"

    ```py
    lambda [arguments]: [expression] 
    ```

!!! example 

    === "Basic Lambda Function"

        ```py
        add = lambda x, y: x + y
        print(add(3, 5))  # Output: 8
        ```

    === "Lambda with ```map()```"

        **The ```map()``` function applies the given lambda function to each item in a list.**

        ```py
        numbers = [1, 2, 3, 4, 5] 

        squared = list(map(lambda x: x ** 2, numbers)) 

        print(squared)  # Output: [1, 4, 9, 16, 25] 
        ```

        The lambda function square each number in the original list. The ```map()``` function applies this lambda to each element, resulting in a new list where every number is squared. 

    === "Lambda with ```filter()```"

        **The ```filter()``` function creates a new list of elements for which the given lambda function returns True.**

        ```py
        numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 

        even_numbers = list(filter(lambda x: x % 2 == 0, numbers)) 

        print(even_numbers)  # Output: [2, 4, 6, 8, 10] 
        ```

        The lambda function checks if a number is even. The ```filter()``` function uses this lambda to keep only the even numbers from the original list, creating a new list containing only even numbers. 

    === "Lambda with ```sorted()```"

        **The ```sorted()``` function can use a lambda function as a key for custom sorting.**

        ```py
        students = [('Alice', 'A', 15), ('Bob', 'B', 12), ('Charlie', 'A', 20)] 

        sorted_students = sorted(students, key=lambda x: x[2]) 

        print(sorted_students) 

        # Output: [('Bob', 'B', 12), ('Alice', 'A', 15), ('Charlie', 'A', 20)] 
        ```

        The lambda function is used as the key for sorting. It tells the ```sorted()``` function to use the third element (index 2) of each tuple for comparison. As a result, the list of students is sorted based on their age (the third element in each tuple).

!!! tip "Best Practices"

    **Use lambda functions when:**

    - You need a simple function for a short period.
    - You’re passing a simple function as an argument to higher-order functions.

    **Avoid lambda functions when:**

    - The operation is complex or requires multiple expressions.
    - You need to reuse the function multiple times (define a regular function instead).




















       




