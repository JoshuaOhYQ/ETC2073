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
























!!! Warning

    The decision must be written in order from **top to bottom**, as Python will read the code line by line and will priotize the decision on top first!








