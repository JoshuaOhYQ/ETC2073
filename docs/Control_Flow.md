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





