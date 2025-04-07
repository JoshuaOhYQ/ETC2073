# Basic Python

## Printing
If you want to print or output something in python, there is different ways of doing it whether it is printing a statement or printing a defined variable(1):
{ .annotate }

1. A variable is a named storage location that holds a value! ✋

!!! example

    === "Printing a statement"

        ``` py
        print("Hello world")
        print("The world is amazing!")
        ```
        Output: 
        ```
        Hello world
        The world is amazing!
        ```

    === "Printing a variable"

        ``` py
        name = "Joshua"
        age = 19
        print(name)
        print(age)
        ```
        Output: 
        ```
        Joshua 
        19
        ```
        
    === "Printing a statement with variables"

        ``` py
        name = "Joshua"
        age = 19
        print(f"Hi there, I am {name} and I am {age} years old!")
        ```
        Output: 
        ```
        Hi there, I am Joshua and I am 19 years old!
        ```

## Comments
If you want to add notes or references for the block or line of code you have just written, you can use comments: 

!!! example

    To insert a comment simply use # follow by the comments u want to add! - 
    ``` py
    #To insert comments 
    print("Hello world") #This will output a statement 
    print("This is an amazing world") #This will output a statement 
    ```
    Output:
    ```
    Hello world 
    This is an amazing world
    ```
    When the code is ran, comments will be ignored as it will not be part of the code! 

## Data types
There are four different data types in python, which are **integers, strings, boolen & float**. If you declare a variable, a specific data type is assigned to it depending on the value of the variable:

!!! example

    === "String"
    
        ``` py
        first_name = "Kid"
        food = "Burger"
        print(first_name)
        print(f"Hello {first_name}")
        print("Your favourite food is {food}")
        ```
        Output: 
        ```
        Kid
        Hello Kid
        Your favourite food is Burger
        ```

    === "Integers"

        ``` py
        age = 18
        quantity = 9
        print(f"You are {age} years old")
        print(f"You bought {quantity} items")
        ```
        Output: 
        ```
        You are 18 years old 
        You bought 9 items 
        ```
        
    === "Float"

        ``` py
        price = 10.99
        gpa = 3.99
        print(f"The price of the item is ${price}")
        print(f"Your GPA is {gpa}")
        ```
        Output: 
        ```
        The price of the item is $10.99
        Your GPA is 3.99
        ```
        
    === "Boolean"

        ``` py
        is_student = True

        if is_student:
            print("You are a student!")
        else: 
            print("You are not a student!")
        ```
        Output: 
        ```
        You are a student!
        ```


