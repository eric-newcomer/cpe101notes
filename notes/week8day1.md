# Chapter 7: Structured Data Types (Programmer Defined Data Types)
## Create variables to describe:
* a point in two dimensions

* a car

* a state in the US

### A point in two dimensions
Create a cartesian coordinate system (x, y)

P1 is (4.0, 1.5), P2 is (0.0, 25), and P3 is (-1.5, 1.5)

Create variables that describe p1, p2, and p3

We need a datatype that stores two values in one variable

### State Diagram
p1 has an x=> 4.0 and y=> 1.5
### Steps (User Defined Data Type)
1) Define a template (data structure class) to describe a point in 2D, template is called Point

2) Use the template definition to create variable of type point  

## 7.1.1: Class Point
      class Point:
          """A point in 2d"""

          def __init__(self, a, b):
              self.x = a
              self.y = b


      def main():
          p1 = Point(4.0, 1.5)
          p2 = Point(0.0, 2.5)
          p3 = Point(-1.5, 1.5)

          print("x value of p1:", p1.x)
          print("y value of p1:", p1.y)


1) Keyword 'class' indicates the beginning of a class definition

2) Documentation Statement

3) Empty line (for readability)

4) Beginning of the initialization method (called when objects of type Point are created; not called explicitly)

    self.x and self.y are attributes of type Point

main) create objects of type Point (method __init__ is called initially)

rest of main) access attributes with dot notation

## 7.2: Class State
Describe a state using:
* name (string)
* population (int)
* size (float)

### State.py
      class State:
          """State described by name, population, and size"""

          def __init__(self, name, population, size):
              self.name = name
              self.population = population
              self.size = size
### StateObjects.py
      from state import State

      def main():
          tex = State(Texas, 27862596, 268581)
          print('State:', tex.name)
          density = tex.population/tex.size
          print('Density:', int(density))

      # can also do:

      def main():
        tex = State(population=27862596, name="Texas", size=268581)
        ...

### 7.3: Class Rectangle
only rectangles where sides are parallel to x and y

      class Rectangle:
          """A rectangle defined by lower left corner and length and width"""

### rectangle.py
          def __init__(self, corner, length, width):
              self.corner = corner
              self.length = length
              self.width = width
### rect_objects.py
          import geometry
          import rectangle

          def main():
              corner = geometry.Point(1.0, 2.0)

              r1 = rectangle.Rectangle(corner, 3.0, 4.0)
              r2 = rectangle.Rectangle(corner, 3.5, 4.5)
              r3 = rectangle.Rectangle(geometry.Point(2.1, 3.2), 2.1, 3.1)

              area1 = r1.length*r1.width
              area3 = r3.length*r3.width
