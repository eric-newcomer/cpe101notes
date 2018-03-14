# Final: 7-10pm, 038-0121 Math Science Building
## Contents of Final:
* Able to formulate and read boolean expressions
      x = 5
      y = 7
      x == 4 #True or False


* Practice Boolean tables (tables with and/or statements)
* Control Structures:

  for

  while

  for k in range(10)

        while condition:

            break

  if, if/else, if/elif/else

* Function
      def f(a, b, c):
          l = [a, b, c, d]
          return a, b, c, d

      #call
      mya, myb, myc, myd = f(7, 3, 5)
      mylist = f(7,...)

* Problem: Algorithm - Search

* Structured Data Types

  point in 2D, 3D

  Rectangle

* Exception Handling
* Data Types

  int, float, str, boolean, list, tuples => indexing

* Find errors in code that is given

* A function provides parameters => effect?

# Chapter 8: I/O Files
## 8.6: Redirection of I/O
Create an Image File:
* Image is made up of tiny squares called pixels
* You can number the pixels like a grid, with width : 0->width-1 and height: 0->height-1
* image of (80, 120) last pizel is 79, 119
* Each pixel stores a certain color; often the RGB model is used
* a color is specified by its red green and blue parts
* Each value(r, g, b) is between 0 and 255 (255 is the color depth)

(255, 0, 0) red

(0, 255, 0) green

(0, 0, 255) blue

(255, 255, 0) yellow

To define an image:
* color depth
* width
* height
* sequence of (r, g, b) values

## PPM: portable pix map
Header:
* 3 lines
      P3
      <width> <height>
      color depth
      255 0 0  0 0 255  0 200 0

# Project 6
      python3 encode.py simple.ppm
      # gives you new file: simple_encoded.ppm
      #   pixels are mapped

## Problems:
Command Line Arguments
* use sys.argv
* check length of the list
* extract 'simple' from the filename

Create simple_encoded.ppm to string

      parts = filename.split('.')
      parts[0] + '\_encoded.ppm'

Write functions:
      def getHeader(fin):
          read 3 lines
          return width, height, color depth

      def printHeaderData(fout, width, height, col):
          write the header = 3 lines

Read the pixels:

      def readPixels():
          col = 0
          row = 0
          colors =[] #empty list for colors

          read a line
          split the line into parts; each part is a number
          Append the numbers to "colors"
          when len(colors) == 3 => new pixel is found
          create a pixel object
          Encode it and write it
          increment col by 1 (col += 1)
          if col == width - 1
          col = 0
          row += 1
