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
        
    === "Booleans"

        ``` py
        name = "Joshua"
        age = 19
        print(f"Hi there, I am {name} and I am {age} years old!")
        ```
        Output: 
        ```
        Hi there, I am Joshua and I am 19 years old!
        ```
