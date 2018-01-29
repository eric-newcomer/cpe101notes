# Monday, 1/29/18: Chapter 4 continued

## Ch. 4.2: Formatted Output
* Numbers are printed
* Numbers are separated by a space
      print (k, k2, k3)
* Format String
      print('%3d%5d%6d' % (k, k2, k3))
  * % isn't modulus in this case; it is a string format operator
  * another way:
        line = '%3d%5d%6d' % (k, k2, k3)
        print(line)

#### %3d: format specifier
* % --> beginning of format specifier
* 3 --> use 3 columns and write right aligned
* d --> create a string for an int

#### Avoid new line:
* end='' --> used to avoid starting a new line  
      print('k=%2d' % k, end=' ')


#### Using floating point Numbers
* Use an 'f' instead of a 'd'
      print('k=%4.1f sq=%6.2 k**3=%8.3f' % (k, k2, k3))

#### %6.2f
* 6 --> total width
* 2 --> number of decimals
* f --> print a floating point value
* %6.2d --> ERROR
* 6.4e+03 --> 6.4 x 10^3
  * can be capital 'E' or lowercase 'e'

#### String 's':
* %s --> print a string value
* %10s --> print a string right aligned
* %-10s --> print a string left aligned

## Ch. 4.3: for loops
* k is variable name
* 'for' and 'in' are Python keywords
* range() is a builtin function
      for k in range(1, 6):
* return an object that produces a list of numbers:
      range(start, end):
        start, start+1, start+2, ... , end
* Each number of the sequence is assigned to k and then the body is executed
      range(1, 6):
        k=1, k=2, k=3, ...
      range(6):
        k=0, k=1, k=2, ...
* range(start, end, step)
      range(1, 6, 2) --> 1, 3, 5
      range(1, 7, 2) --> 1, 3, 5
      range(1, 16, 3) --> 1, 4, 7, 10
* body of loop is executed for each number that is returned by range
* range(1, 2, 0.1) --> ERROR --> step can only be an int
