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
        Full reference at Python Docs:
        https://docs.python.org/3/library/stdtypes.html#string-methods































