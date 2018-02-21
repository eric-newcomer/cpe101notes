# Chapter 6 continued
## 2nd Midterm Topics:
#### Loops
#### Lists
#### Lists and 2D-arrays:
      a[3][2]
* a is a list of a list

#### Strings

# Convert a string to a list and vice versa
### Common to strings and Lists
* they are sequences
* they iterate over all elements
* slice operator
* many common methods --> index, find, ...

### String is immutable, all elements are strings
### String to list:
      mylist = list("Hello")
      >>> ['H', 'e', 'l', 'l', 'o']

### List to string:
      mystr = ''.join(mylist)
      >>> 'Hello'

      mystr = '--'.join(mylist)
      >>> 'H--e--l--l--o'
      # '--' is the separator

# Reverse a String
      'H' 'e' 'l' 'l' 'o'
       0   1   2   3   4
       0             len-1
           k    len-1-k

### Function:

      def reverse_str(str):
          lst = list(str)
          l = len(lst)
          for k in range(l//2):
              tmp = lst[l-1-k]
              lst[l-1-k] = lst[k]
              lst[k] = tmp
          rstr = ''.join(lst)
          return rstr

### Swap two values
We want x = 5 to become x = 7

We want y = 7 to become y = 5

      tmp = 5
      x = 7
      y = tmp

Shortcut:

      x,y = y,x #shortcut

## Reverse a String Function (better):

      for k in range(l//2):
          lst[k], lst[l-1-k] = lst[l-1-k], lst[k]

## Reverse Method
### applicable to lists
l1 is a list

      l1.reverse()
      >>> reverses the elements of list l1
      >>> no return value

      l1 = ['1', '2']
      l1.reverse()
      >>> ['2', '1']

## Simple Solution: reverse_str
      def reverse_str(str):
          lst = list(str)
          lst.reverse()
          return ''.join(lst)

# Chapter 7: Structured Data Types
## (Programmer Defined Data Types)
### We want to create variables that describe:
* a point in 2D, 3D, and n-D
* a car
* a state in the U.S.
* a student

### Each of these items have many properties that belong together.
### We need a data type to store these values.
## 7.1: A point in 2D, to be continued...
