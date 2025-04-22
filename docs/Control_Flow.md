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

    
