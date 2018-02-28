### Announcement: Final will be on March 19th 7:10-10pm
# Chapter 7 continued
## 7.3-2
      class Point:
          """A point in 2d"""

          def __init__(self, x, y):
              self.x = x
              self.y = y


      class Rectangle:
          """A rectangle defined by lower left corner and length and width

          def __init__(self, corner, length, width):
              self.corner = corner
              self.length = length
              self.width = width

## 7.4: Unittests for Structured Data Types
* test if initialization method works correctly
* we want to test method \__init__
      import unittest
      import geometry

      class TestPoint(unittest.TestCase):

          def test_init_method(self):
              p = geometry.Point(3.1, 2.7)
              self.assertAlmostEqual(p.x, 3.1)
              self.assertAlmostEqual(p.y, 2.7)

### TestCase for Rectangle
* How do you find x attribute of lower left corner?
      c = r.corner
      myx = c.x
      # OR
      myx = r.corner.x

* Example:
      import unittest
      import geometry

      class TestPoint(unittest.TestCase):
          def test_init_rectangle(self):
              myCorner = geometry.Point(3.1, 2.7)
              myRect = geometry.Rectangle(myCorner, 5.0, 6.0)

## 7.5: Functions using Structured Data Types
### Calculate distance between two points, p1 and p2:
      import math

      def distance(p1, p2):
          dx = p2x - p1x
          dy = p2y - p1y
          d = math.sqrt(dx**2+dy**2)
          return d

### Test function for distance function
      import unittest
      import geometry
      import distance

      class TestCases(unittest.TestCase):

          def test_distance_1(self):
              x1 = 1.2
              y1 = 2.3
              p1 = geometry.Point(x1, y1)
              p2 = geomtry.Point(x1+3, y1+4)
              found = distance(p1, p2)
              self.assertAlmostEqual(found, 5)

## 7.6: Equality for Structured Data Types
### State Diagram
* p1 is created with point x=2 and y=1 with unique serial number
* p2 is created with point x=2 and y=1 but with different serial number than p1
* THEREFORE: p1 is NOT EQUAL to p2
#### id(obj)
* return the identity (serial number) of an object.
* Guaranteed to be unique among simultaneously existing objects

### Conditions for Points to be Equal
Requirements:

* Condition 1: if p1 == p2 is True then p2==p1 should be True
* Condition 2: if p1==p2 and p2==p3, then p1==p3 is False

#### Don't compare floating point values for equality
## To modify the default meaning of p1==p2 for objects of type Point, add a method \__eq__ which compares two objects of type Point with each other
### Method \__eq__ should return either True or False
### If method \__eq__ is not implemented, Python uses the default behavior

### If method \__eq\__ is implemented then p1==p2 invokes method \__eq__ and the return value is assigned to the expression

### Epsilon Function
      def epsilon_equal(x, y, epsilon = 0.000001):
          return x-epsilon < y < x + epsilon
