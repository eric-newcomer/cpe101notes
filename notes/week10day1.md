# Final Exam: Monday (3/19), 7:10pm-10pm

# Chapter 9: Exception Handling
## How to handle program errors (not programming/syntax errors)
The program is correct, but sometimes errors occur when the program is executed

Earthquake Example:
* web server down
* no internet connection

Access to a file:
* wrong filename
* file does not exist
* no permission to read a file

## "try/except" mechanism
### General Situation
* a rule or an assumption
  * Every line contains a number
* Exceptions to the rule
  * some lines are empty or do not contain a valid number   

### Exception handling provides a flexible mechanism to detect an error at one place and deal with an error at another place

## Implementation
      try:
          '''
          code according to rule
          '''
      except:
          '''
          code to handle the error
          '''
* two blocks of code
* When no error occurs, only block 1 is executed
* If an error occurs in block 1, the program continues with block 2, which must handle the problem.

      fin = open('numbers.txt', 'r')

      mysum = 0.0
      line_number = 0
      numbers_found = 0

      for line in fin:
          line_number += 1
          try:
              number = float(line)
              mysum = mysum + number
              numbers_found += 1
          except:
              print('Line {0}: no number'.format(line_number))
      fin.close()

      print('Sum = {0:.3f}'.format(mysum))
      print('{0} numbers found'.format(numbers_found))
      print('{0} lines found'.format(line_number))

## 9.2: Opening a file
If function open is called to open a file an exception occurs when:
* the file doesn't exist
* file can't be used for some other reason


      filename = 'numbers.txt'
      while True:
          try:
              fin = open(filename, 'r')
              break
          except:
              print('Cannot open '+ filename)
              filename = input('Eater file').strip()
Different Types of exceptions for different errors:
* FileNotFoundError
* PermissionError

      try:
          fobj = open('fie.txt', 'r')
      except FileNotFoundError:
          print('File not found')
      except PermissionError:
          print('No permission')
      finally:
          print('Always executed!')

## 9.3: Raising Exception
We can't create our own exception but we can create built-in exception

      def calculate(a, b):
          c = a + (1/b)

          #restrictions: b not 0, b not 1, and the
          #value of c must be <=100
b = 0 --> ZeroDivisionError

b = 1 --> Value Error

c > 100 --> Overflow Error

      def calculate(a, b):
          if b == 0:
              raise ZeroDivisionError()
          if b == 1:
              raise ValueError()
          c = a + (1/b)
          if c > 100:
              raise OverflowError()
          else:
              return c 
