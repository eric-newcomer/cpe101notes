# 5.2.6: Slices [:] - Slice Operators
      n = [10, 21, 13, 74, 5, 6, 7, 8...]

      sublist = n[2:5] --> [13, 74, 5]
* create a list containing values with index 2, 3, and 4
* Special Cases:
      na = n[:5]
      nb = n[4:] --> all elements starting with n[4]
      nc = n[:] --> copy of the complete list

# 5.3 Lists of Lists:
## Nested Lists | Arrays | Tables | Matrices
### A list is a sequence of elements
      l = [3, 4, 5]
### A value can also be a list
      m = [[2, 4, 6], [3, 5, 7]]
* m is a list with two elements
* each element is a list

      a = m[0] --> reference to the first element of list m
      b = a[1] --> 4

### Direct access of values in nested lists
      b = m[0][1] --> first brackets are outer list,
      second is inner list, aka second element of first
      list contained in list m

      m[1][2] = g

* list of list represents 2D arrays or tables

### Matrices      
      m = {2 4 6} --> 2x3 array
          {3 5 7}

      n = [[2, 4, 6], [3, 5, 7], [8, 10, 12]]

          {2  4  6}
      n = {3  5  7}
          {8 10 12}

## display_array function

      def displayarray(m):
          # assume m is a list of lists containing int values
          for r in range(len(m)):
              for c in range(len(m[r])): --> number of elements in row r
                  print('%4d' % m[r][c], end='')
              print()

* Another solution

      def displayarray(m):
          for row in n: --> row is a list
              for element in row: --> element is an int
                  print('%4d' % element, end='')
              print()

* Yet another solution:

      def displayarray(m):
          for r in range(len(m)):
              row = m[r]
              for element in row:
                  print('%4d' % element, end='')
              print()

## create_array function
      def create_array(rows, cols):
          m = []  --> outer list
          count = 1
          for r in range(rows):
              n = []
              for c in range(cols):
                  n.append(count)
                  count += 1
              m.append(n)
          return m
* call this function:
      my_array = create_array(4, 5)
