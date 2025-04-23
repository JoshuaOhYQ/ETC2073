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