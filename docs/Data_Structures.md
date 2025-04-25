# Data Structures

## String methods
Python provides many built-in methods for string manupulation. Here are some of the most commonly used string methods:

!!! info "Lists of string methods"

    === "Case Conversion Methods"

        - ```str.lower()``` - returns a lowercase version of the string
        - ```str.upper()``` - returns an uppercase version of the string
        - ```str.capitalize()``` - capitalizes the first character
        - ```str.title()``` - capitalizes the first letter of each word
        - ```str.swapcase()``` - swaps uppercase to lowercase and vice versa


    === "Search and Replace Methods"

        - ```str.find(sub)``` - returns lowest index where sub is found
        - ```str.rfind(sub)``` - returns highest index where sub is found
        - ```str.index(sub)``` - ike find() but raises ValueError if not found
        - ```str.rindex(sub)``` - like rfind() but raises ValueError if not found
        - ```str.replace(old, new)``` - replaces occurrences of old with new
        - ```str.count(sub)``` - counts occurrences of substring


    === "Validation Methods"

        - ```str.isalpha()``` - checks if all characters are alphabetic
        - ```str.isdigit()``` - checks if all characters are digits
        - ```str.isalnum()``` - checks if alphanumeric characters only
        - ```str.isspace()``` - checks if all characters are whitespace
        - ```str.islower()``` - checks if all characters are lowercase
        - ```str.isupper()``` - checks if all characters are uppercase
        - ```str.startswith(prefix)``` - checks if string starts with prefix
        - ```str.endswith(suffix)``` - checks if string ends with suffix


    === "Formatting Methods"

        - ```str.strip()``` - removes leading/trailing whitespace
        - ```str.lstrip()``` - removes leading whitespace
        - ```str.rstrip()``` - removes trailing whitespace
        - ```str.center(width)``` - centers string in given width
        - ```str.ljust(width)``` - left-justifies string in given width
        - ```str.rjust(width)``` - right-justifies string in given width
        - ```str.zfill(width)``` - pads with zeros on left to fill width
        - ```str.expandtabs(tabsize)``` - replaces tabs with spaces

        
    === "Splitting and Joining"

        - ```str.split(sep)``` - splits string by separator into list
        - ```str.rsplit(sep)``` - splits from right side
        - ```str.splitlines()``` - splits at line boundaries
        - ```str.join(iterable)``` - joins elements with string as separator
        - ```str.partition(sep)``` - splits into 3 parts around first sep
        - ```str.rpartition(sep)``` - splits into 3 parts around last sep

    === "Length finding"

        - ```len(variable)``` - returns the length of the string variable

!!! Example 

    === "1"
        ```py
        name = "John"
        result = len(name)
        print(result)
        ```
        Output:
        ```
        4
        ```


    === "2"
        ```py
        name = "John"
        result = name.find("o")
        print(result)
        ```
        Output:
        ```
        1
        ```


    === "3"
        ```py
        name = "John Cena"
        result = name.rfind("n")
        print(result)
        ```
        Output:
        ```
        7
        ```


    === "4"
        ```py
        name = "John"
        result = name.upper()
        print(result)
        ```
        Output:
        ```
        JOHN
        ```


    === "5"
        ```py
        name = "John234"
        result = name.isdigit()
        print(result)
        ```
        Output:
        ```
        False
        ```
        ```py
        name = "123"
        result = name.isdigit()
        print(result)
        ```
        Output:
        ```
        True
        ```


    === "6"
        ```py
        name = "John"
        result = name.isalpha()
        print(result)
        ```
        Output:
        ```
        True
        ```


    === "7"
        ```py
        phone_number = "012-3456789"
        result = phone_number.replace("-", " ")
        print(result)
        ```
        Output:
        ```
        012 3456789
        ```


!!! Tip "To view more string methods"

    === "Direct from Python"
        ```py
        print(help(str))
        ```

    === "From website"
        Full reference at [Python Docs](https://docs.python.org/3/library/stdtypes.html#string-methods)


## String Indexing
This allows us to access individual characters or elements in a string or sequence using their position and indexing operator:

!!! info

    Python supports both positive indexing (left to right) and negative indexing (right to left).

!!! example

    === "Positive Indexing"

        Basically, it starts at ```0``` for the first character and increases by ```1``` for each subsequent character:

        ```py 
        text = "Python"
        print(text[0])
        print(text[1])
        print(text[5])
        ```
        Output:
        ```
        P
        y
        n
        ```


    === "Negative Indexing"

        Basically, it starts at ```-1``` for the last character and decreases by ```1``` for each preceding character:

        ```py 
        text = "Python"
        print(text[-1])
        print(text[-2])
        print(text[-6])
        ```
        Output:
        ```
        n
        o
        P
        ```


    === "String Slicing (Extracting Substrings)"

        You can extract a substring using the syntax:
        ```string[start:end:step]```

        - ```start``` → Index to begin (inclusive, default ```0```)
        - ```end``` → Index to stop (exclusive, default ```len(string)```)
        - ```step``` → Step size (default ```1```)

        ```py 
        text = "Python Programming"

        # Get first 6 characters
        print(text[0:6])
        
        # Get from index 7 to end
        print(text[7:])
        
        # Get every 2nd character
        print(text[::2])

        # Reverse a string
        print(text[::-1])
        ```
        Output:
        ```
        Python
        Programming
        Pto rgamn
        gnimmargorP nohtyP
        ```


## Format Specifiers
Format specifiers in Python are used to control how values are formatted based on waht flags are inserted. They allow you to specify things like alignment, padding, precision, and type representation. Python provides several ways to use format specifiers:

!!! info "Common Format Specifier"

    The general syntax is:
    
    ```[fill][align][sign][#][0][width][grouping][.precision][type]```

    where,

    - Fill: Character to pad with (default is space)
    - Align: ```<``` (left), ```>``` (right), ```^``` (center), ```=```(pad after sign)
    - Sign: ```+``` (show sign for both + and -), ```-``` (only for -), space (leading space for +)
    - Width: Minimum field width
    - Precision: For floating point, number of digits after decimal
    - Type:
        * d, i: integer
        * f, F: float
        * e, E: scientific notation
        * g, G: general format (auto switches between f and e)
        * %: percentage
        * x, X: hexadecimal
        * o: octal
        * b: binary
        * c: character (unicode code point)


!!! example

    Format specifiers provide powerful control over how values are displayed in Python strings.

    === "Number formatting"

        ```py 
        print(f"{1234:10d}")      # '      1234' (right-aligned, width 10)
        print(f"{1234:<10d}")     # '1234      ' (left-aligned)
        print(f"{1234:^10d}")     # '   1234   ' (centered)
        print(f"{1234:010d}")     # '0000001234' (zero-padded)
        print(f"{1234:,d}")       # '1,234' (with thousands separator)
        print(f"Binary: {10:b}")          # Output: Binary: 1010
        ```
        Output:
        ```
              1234
        1234      
           1234   
        0000001234
        1,234
        1010
        ```
        


    === "Float formatting"

        ```py 
        print(f"{3.14159:.2f}")   # '3.14' (2 decimal places)
        print(f"{3.14159:10.2f}") # '      3.14' (width 10, 2 decimals)
        print(f"{3.14159:e}")     # '3.141590e+00' (scientific notation)
        ```
        Output:
        ```
        3.14
              3.14
        3.141590e+00
        ```


    === "String formatting"

        ```py 
        print(f"{'hello':10s}")   # 'hello     ' (left-aligned, width 10)
        print(f"{'hello':>10s}")  # '     hello' (right-aligned)
        print(f"{'hello':^10s}")  # '  hello   ' (centered)
        print(f"{'hello':.2s}")   # 'he' (truncated to 2 chars)
        ```
        Output:
        ```
        hello     
             hello
          hello   
        he
        ```

## Lists, sets and tuples

Python offers several built-in collection (1) types, each with different characteristics. Here's a comparison of lists, sets, and tuples:
{ .annotate }

1. **Collection**: a single "variable" used to store multiple values :material-content-save-all-outline:

!!! example "Comparisons with examples"

    === "Lists"

        - **Mutable** (can be changed after creation)
        - **Ordered** (maintains insertion order)
        - **Allows duplicates**
        - Syntax: ```[]``` or ```list()```

        ```py 
        # Creating a list
        fruits = ['apple', 'banana', 'cherry']
        numbers = list(range(5))

        # Common operations
        fruits.append('orange')       # Add item
        fruits.remove('banana')       # Remove item
        fruits[1] = 'blueberry'       # Modify item
        print(fruits[0])              # Access item
        print(fruits)                 # Access list
        print(fruits[0:1])            # Print list within a range
        print(fruits[::2])            # Print list with a step
        print(fruits[::-1])           # Print list backwards

        print()

        # Iterate over a for loop (To print every element)
        for fruit in fruits:
            print(fruit)
        ```
        Output:
        ```
        apple
        ['apple', 'blueberry', 'orange']
        ['apple', 'blueberry']
        ['apple', 'orange']
        ['orange', 'blueberry', 'apple']

        apple
        blueberry
        orange
        ```
        

    === "Tuples"

        - **Immutable** (cannot be changed after creation)
        - **Ordered** (maintains insertion order)
        - **Allows duplicates**
        - Syntax: ```()``` or ```tuple()```

        ```py 
        # Creating a tuple
        colors = ('red', 'green', 'blue')
        coordinates = tuple([1, 2, 3])

        # Common operations
        print(colors[1])              # Access item (green)
        print(colors.count('red'))    # Count occurrences
        print(len(colors))            # Get length
        print('red' in colors)        # Find if element exists
        print(colors.index("blue"))   # Find index for element

        print()

        # Iterate over a for loop (To print every element)
        for color in colors:
            print(color)

        # Tuples are often used for fixed data (Example Scenario)
        point = (3, 4)  # x, y coordinates
        ```
        Output:
        ```
        green
        1
        3
        True
        2

        red 
        green 
        blue
        ```


    === "Sets"

        - **Mutable** (can add/remove items)
        - **Unordered** (no index positions)
        - **Allows duplicates** (automatically removes duplicates)
        - Syntax: ```{}``` or ```set()```

        ```py 
        # Creating a set
        unique_numbers = {1, 2, 3, 3, 4}  # {1, 2, 3, 4}
        letters = set('hello')            # {'h', 'e', 'l', 'o'}

        # Common operations
        unique_numbers.add(5)      # Add item
        unique_numbers.remove(2)   # Remove item
        letters.add('p')           # Add item
        letters.remove('e')   # Remove item

        print(unique_numbers)
        print(letters)
        ```
        Output:
        ```
        {1, 3, 4, 5}
        {'p', 'l', 'h', 'o'}
        ```

!!! tip

    **Key Differences**:

    | Feature      | List         | Tuple        | Set          |
    |--------------|--------------|--------------|--------------|
    | Mutability   | Mutable      | Immutable    | Mutable      |
    | Order        | Ordered      | Ordered      | Unordered    |
    | Duplicates   | Allowed      | Allowed      | Not allowed  |
    | Syntax       | `[]`        | `()`        | `{}`        |
    | Use Case     | Dynamic data | Fixed data   | Unique items |

    **When to use each collection cases**: 

    - Use **lists** when you need an ordered collection that may change
    - Use **tuples** for fixed data that shouldn't change (like coordinates)
    - Use **sets** when you need to ensure uniqueness or perform set operations

    **To access more methods and attributes avalaible to collection**:
    
    ```py
    fruits = ['apple', 'orange', 'banana', 'coconut']
    print(dir(fruits))                        # Lists
    print(help(fruits))                       # Description 
    ```

!!! Danger "Additional Information"

    All three **(list, tuple and set)** support iteration and can be converted between each other:

    ```py
    my_list = [1, 2, 3]
    my_tuple = tuple(my_list)
    my_set = set(my_list)
    ```


## 2D Collections
In Python, you can create two-dimensional (2D) collections using various data structures. Here are the common ways to implement 2D collections:

!!! info 

    2D collections are fundamental for many applications like game boards, image processing, spreadsheets, and more. You can have different forms of 2D collection with **lists, tuples and sets**, for example lists made of lists, lists made of tuples, etc. Choose the implementation that best fits your specific use case.


!!! example

    === "1"

        ```py 
        fruits = ["apple", "orange", "banana", "coconut"]
        vegetables = ["celery", "carrots", "potatoes"]
        meats = ["chicken", "fish", "turkey"]

        groceries = [fruits, vegetables, meats]

        # print the whole 2D collection
        print(groceries)

        print()

        # print an entire row
        print(groceries[0])

        print()

        # print elements of the 2D collection
        print(groceries[0][0])

        print()

        # Single loop printing (iterating the rows)
        for collection in groceries:
            print(collection)

        print()

        # Nested loop printing (iterating the elements)
        for collection in groceries:
            for food in collection:
                print(food, end=" ")
            print()
        ```
        Output:
        ```
        [['apple', 'orange', 'banana', 'coconut'], ['celery', 'carrots', 'potatoes'], ['chicken', 'fish', 'turkey']]

        ['apple', 'orange', 'banana', 'coconut']

        apple

        ['apple', 'orange', 'banana', 'coconut']
        ['celery', 'carrots', 'potatoes']
        ['chicken', 'fish', 'turkey']

        apple orange banana coconut
        celery carrots potatoes
        chicken fish coconut
        ```

        Another way of declaring it:

        ```py
        groceries = [["apple", "orange", "banana", "coconut"],
                     ["celery", "carrots", "potatoes"],    
                     ["chicken", "fish", "turkey"]]
        ```


    === "2"

        ```py 
        num_pad =((1, 2, 3),
                  (4, 5, 6),
                  (7, 8, 9),
                  ("*", 0, "#"))
        
        for row in num_pad:
            for num in row:
                print(num, end=" ")
            print()
        ```
        Output:
        ```
        1 2 3
        4 5 6
        7 8 9
        * 0 #
        ```


    === "3"

        ```py 
        # Creating a 2D list (matrix)
        matrix = [
            [1, 2, 3],
            [4, 5, 6],
            [7, 8, 9]
        ]

        # Accessing elements
        print(matrix[0][1])  # Output: 2 (first row, second column)

        # Modifying elements
        matrix[1][2] = 10  # Changes 6 to 10

        # Iterating through the matrix
        for row in matrix:
            for element in row:
                print(element, end=' ')
            print()
        ```
        Output:
        ```
        2
        1 2 3
        4 5 10
        7 8 9
        ``` 


## Dictionaries
Dictionaries are one of Python's most powerful and commonly used data structures. They store data as key-value pairs, providing fast lookups and flexible data organization. They are mutable, unordered and does not allow duplicates. The keys of the dictionaries must be hashable (strings, numbers, tuples, but not lists). There is a specific way of defining dictionaries in Python: 

!!! info "Common Use Cases"

    1. **Counting occurrences** (word frequency, etc.)
    2. **Fast lookups** by key (much faster than lists for large datasets)
    3. **Structured data** (like JSON objects)
    4. **Memoization** (caching function results)
    5. **Implementing graphs** (adjacency lists)


!!! example

    === "Creating Dictionaries"

        ```py
        # Empty dictionary
        empty_dict = {}

        # Dictionary with initial values
        person = {
            "name": "Alice",
            "age": 30,
            "city": "New York"
        }

        # Using dict() constructor
        person = dict(name="Alice", age=30, city="New York")

        # Dictionary with mixed key types
        mixed_dict = {
            "name": "Bob",
            42: "The Answer",
            (1, 2): "Tuple as key"
        }
        ```
    
    
    === "Accessing Values"

        ```py
        # Using square bracket notation
        print(person["name"])  # Output: Alice

        # Using get() method (safer, returns None if key doesn't exist)
        print(person.get("age"))  # Output: 30
        print(person.get("country"))  # Output: None
        print(person.get("country", "USA"))  # Default value if key doesn't exist which in this case is USA
        ```

    
    === "Adding/Updating Items"

        ```py
        # Adding new key-value pair
        person["occupation"] = "Engineer"

        # Updating existing value
        person["age"] = 31

        # Update multiple items at once
        person.update({"age": 32, "country": "USA"})
        ```


    === "Removing Items"

        ```py
        # Using del
        del person["city"]

        # Using pop() - removes and returns value
        age = person.pop("age")

        # Using popitem() - removes and returns last inserted item (Python 3.7+)
        last_item = person.popitem()

        # Clear all items
        person.clear()
        ```

    
    === "Other Dictionary Methods"

        ```py
        # Get all keys
        keys = person.keys()  # Returns a view object

        # Get all values
        values = person.values()  # Returns a view object

        # Get all key-value pairs
        items = person.items()  # Returns a view object

        # Check if key exists
        if "name" in person:
            print("Name exists")

        # Dictionary length
        num_items = len(person)
        ```


    === "Default Dictionaries"

        ```py
        from collections import defaultdict

        # Automatically initializes missing keys
        word_counts = defaultdict(int)
        for word in ["apple", "banana", "apple"]:
            word_counts[word] += 1
        # Result: defaultdict(<class 'int'>, {'apple': 2, 'banana': 1})
        ```

        
    === "Other Examples (in full)"

        ```py 
        # Dictionary Basics
        capitals = {"USA": "Washington",
                    "India": "New Delhi",
                    "China": "Beijing",  
                    "Russia": "Moscow"}

        # Accessing values
        print(capitals.get("USA"))  # Washington
        print(capitals.get("India"))  # New Delhi

        # Adding new key-value pair
        capitals.update({"Germany": "Berlin"})
        print(capitals)  # Includes Germany: Berlin

        # Updating existing value
        capitals.update({"USA": "Detroit"})
        print(capitals)  # USA now maps to Detroit

        # Removing a key-value pair
        capitals.pop("China")
        print(capitals)  # China removed

        # Working with keys
        # Get all keys
        keys = capitals.keys()
        print(keys)  # dict_keys(['USA', 'India', 'Russia', 'Germany'])

        # Iterate through keys
        for key in capitals.keys():
            print(key)

        # Working with values
        # Get all values
        values = capitals.values()
        print(values)  # dict_values(['Detroit', 'New Delhi', 'Moscow', 'Berlin'])

        # Iterate through values
        for value in capitals.values():
            print(value)

        # Working with items (key-value pairs)
        # Get all items
        items = capitals.items()
        print(items)  # dict_items([('USA', 'Detroit'), ('India', 'New Delhi'), ...])

        # Iterate through items
        for key, value in capitals.items():
            print(f"{key}: {value}")
        ```
        Output:
        ```
        Washington
        New Delhi
        {'USA': 'Washington', 'India': 'New Delhi', 'China': 'Beijing', 'Russia': 'Moscow', 'Germany': 'Berlin'}
        {'USA': 'Detroit', 'India': 'New Delhi', 'China': 'Beijing', 'Russia': 'Moscow', 'Germany': 'Berlin'}
        {'USA': 'Detroit', 'India': 'New Delhi', 'Russia': 'Moscow', 'Germany': 'Berlin'}
        dict_keys(['USA', 'India', 'Russia', 'Germany'])
        USA
        India
        Russia
        Germany
        dict_values(['Detroit', 'New Delhi', 'Moscow', 'Berlin'])
        Detroit
        New Delhi
        Moscow
        Berlin
        dict_items([('USA', 'Detroit'), ('India', 'New Delhi'), ('Russia', 'Moscow'), ('Germany', 'Berlin')])
        USA: Detroit
        India: New Delhi
        Russia: Moscow
        Germany: Berlin
        ```
        

!!! Tip 

    **To display lists of all the attributes and methods for dictionaries:**

    ```py
    capitals = {"USA": "Washington",
                "India": "New Delhi",
                "China": : "Beijing",
                "Russia": "Moscow"}

    print(dir(capitals))
    ```

    **To display the in-depth description of attributes and methods for dictionaries:**

    ```py
    capitals = {"USA": "Washington",
                "India": "New Delhi",
                "China": : "Beijing",
                "Russia": "Moscow"}

    print(help(capitals))
    ```

   
































