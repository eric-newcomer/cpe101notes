# Chapter 7 continued (Structured Data Types)
## 7.5 Functions using Structured Data Types
      import geometry
      import math

      def distance(p1, p2):
          dx = p2.x - p1.x
          dy = p2.y - p1.y
          return math.sqrt(dx**2 + dy**2)

      def main():
          p1 = geometry.Point(1.0, 2.0)
          p2 = geometry.Point(3.0, 5.0)
          d = distance(p1, p2)
          print('Distance {0:6.3f}'.format(d))

* move function
      def move(p, a, b):
          p.x = p.x + a
          p.y = p.y + b
* call:
      myp = Point(3.0, 4.0)
      move(myp, 3.0, 2.1)

* Shift Function
      def getShifted(p, x, y):
          np = Point(p.x+x, p.y+y)
          return np
* Call: mp => x is 3.0, y is 4.0
      mynp = getShifted(myp, 2.0, 2.1)
      # mynp => x is 5.0, y is 6.1

## 7.6 Equality for Structured Data Types
### Epsilon Function
      def epsilon_equal(x, y, epsilon = 0.001):
          return x-epsilon < y < x+epsilon


      check_x = epsilon_equal(x, y, 0.000001)

### Note that: p1 == p2 is equal to p1.\__eq__(p2)

## When are two objects of type Rectangle equal?
Rectangle has three attributes
* position
* length
* width

### Problem:
point1 == rectangle

rectangle == point

### Point:
      if not isInstance(other, Point):
          return False

### Rectangle:
      if not isInstance(other, Rectangle):
          return False

# Chapter 8: I/O - Files
### A program can
read data:
* from standard keyboard input
* from a file

write data:
* to standard console output
* to a file

redirection:
* standard input becomes a file/network/etc
* standard output becomes a file, printer, network
