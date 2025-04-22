# Control Flow

## If-Else-Elif 
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
