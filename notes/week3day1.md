# Week Three: Day 1

## Local Variables

### State Diagram:

used to visualize the state of a program

L7: main --> [x --> 2]

After line 3:

      x --> 2
      a=2
      b=4
      c=12

After line 8:
      x=2
      y=12


## BOOLEAN LOGIC AND CONDITIONALS
use relational operators to assign boolean values

### Example 1:
      x = 2
      y = 5
      a = (x == y)


      a = (x != y) not equal
      x > y greater than
      x >= y greater than or equal to
      x < y less than
      x <= y less than or equal to
      WRONG: x =< y or x => y

## BOOLEAN OPERATORS
### 3 basic operators
      logical AND: and #java is &&
      logical OR: or #java is ||
      negation NOT: not #java is !
#### Example:
    c = a and b
    c is true, only if a and b are true
    c = a or b
    c is true, if either a or b is true

Example Problem from Slides: check if number is greater than 10 and if it is even.
  result = (k > 10) and (k%2 == 0)

## CONDITIONALS
### if condition example:
    if x >= 1:
      print('Big')
    else:
      print('Small')
