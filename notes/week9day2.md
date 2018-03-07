# Chapter 8: I/O Continued:
## Writing to a file:
      fin = open('numbers.txt', 'r') #read a file
      fout = open('results.txt', 'w') #write a file

## Splitting Lines
### Method split() - splits a string into parts and returns a list containing all parts

# Chapter 10: Sorting

### Problem: A list of elements is given
      l = [e1, e2, e3, e4,...en]
      #Examples:
      l = [5, 2, 6, 3]
      l = ['A', 'B', '3', 'a']

      #Sort the elements in ascending or descending order
      #You must make it possible for two elements to be compared
      #e2 < e3 => True or False?
### Two different solutions
1) the elements within the list are reordered and no new list is created

      l.sort()
      l.sort(reverse=True)

2) New list is created, where the elements of the 'old' list are ordered; the original list is NOT modified.

      newl = sorted(l)
      newl = sorted(l, reverse = True)

## 10.1: Sorting Strings
### Strings are sorted __alphabetically__ using ASCII code
      ' ' < '0' < '1' < ... < 'A' < 'B' < ... < 'a' < 'b' < ...

Example 1)

      l = ['A', 'B', '3', 'a']
      l.sort()
      l = ['3', 'A', 'B', 'a']

      l = ['A', 'Ab', 'Z', 'Aa', '1a']
      l.sort()
      l = ['1a', 'A', 'Aa', 'Ab', 'Z']
* Look at the first character
* if the first character is the same, look at the second character

Example 2)

      l = ['100', '2', '80', '500', '1', '10']
      l.sort()
      l = ['1', '10', '100', '2', '500', '80']

## 10.2: Sorting - Parameter key
### Sort strings, ignoring case
* 'A' and 'a' are the same
* 'B' and 'a' ==> 'a' < 'B' returns True

      l = ['A', 'B', '3', 'a']
      l.sort(key=str.lower())
      #don't compare elements using e1 < e2
      #instead: str.lower(e1) < str.lower(e2)
      str.lower('a') < str.lower('B')

### Example:
* __Sort a list of strings according to the length of the strings__
      l.sort(key=len)


* __Sort a list of int strings by value__
      c = ['100', '2', '80', '500']
      c.sort(key=int)
      c = ['2', '80', '100', '500']

* __IMPORTANT: Function int must be applicable to all elements in list__

## 10.3: List of Lists and Structured Data Types
      l = [[3, 4, 7], [1, 5, 4], ...]
      #sort using the value at a given index
      #of the inner list

      l = [e1, e2, e3, e4, ..., en]
      #all elements are of type Point,
      #Rectangle, or Earthquakes

__Use a certain attribute for comparison__

__all elements must have this attribute__

# You have to
      import module operator
      attrgetter(name of an atrribute)
      itemgetter(index)

      l.sort(key = attrgetter('x')) #or 'r' or 'mag'

      l.sort(key = itemgetter(1))
