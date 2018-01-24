# Week Three: Day 2

## 3.2-4: Conditionals - Problems
### Problem 1:
#### Write function named max2 that returns max of two numbers.
      def max2(a, b):
        if a >= b:
          max = a
        else:
          max = b
        return max
### Problem 2:
#### Write function named max3 that returns the max of three numbers. 'A'
      def max3(a, b, c):
        if a > b:
          if a > c:     #Nested if-else statement
            max = a
        elif b > c:
          max = b
        else:
          max = c
        return max
#### Another way 'B':
      def max3(a, b, c):
        if a > b:
          max = a
        else:
          max = b
        if c > max:
          max = c
        return max
#### Another way 'C':
      def max3(a, b, c):
        max = max2(a, b)
        max = max2(max, c)
        return max
#### Another way 'D':
      def max3(a, b, c):
        return max2(max2(a, b), c)
#### Another way 'E':
      def max3(a, b, c):
        if (a >= b) and (a >= c):
          max = a
        elif (b >= a) and (b >= c):
          max = b
        else:
          max = c
        return max
## 3.3 Chained Conditionals
      if cond-1:
        block-1
      elif cond-2:
        block-2
      elif cond-3:
        block-3
      else:
        block-n
* conditions are checked one after another
* order of conditions is very important

## 3.4 Range Checking
### Check whether a number is between 10 and 20?
* Assume that the boundaries are included

      if 10 <= x <= 20:

      if not((x<10) or (x>20)):

## 3.5 Check for Equality
### What is the meaning of x == y?

      int:
        x = 5
        y = 5
        x == y --> true

      str:
        x = 'abc'
        y = 'abc'
        x == y --> true

      bool:
        x = True
        y = True
        x == y --> True
