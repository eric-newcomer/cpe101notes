# String Functions
## Function "split"
      str1 = '21-85-731-2'
      strlist = str1.split('-')
      # ['21', '85', '731', '2']
      # returns a list of strings using '-' as delimiter

      str2 = '-21--85'--76'
      list1 = str2.split('-')
      # ['', '21', '', '85', '76']

      strword = 'Hello'
      strword.split()
      # delimiter is any whitespace
      # empty strings are removed
## 6.4: Formatted Output
      str1 = '%6d%9d' % (k, m)
              ^          ^a tuple of values
              ^format specifiers
* Different method should be used
* Replacement fields: {0}
      str1 = 'The sum of {0} and {1} is {2}'.format(3, 4, 7)
      # {0} becomes 3, {1} becomes 4, {2} becomes 7
      # The sum of 3 and 4 is 7

## Field with, Decimals, Alignment
      {0:6.2f}
         ^ ^ ^
         ^ ^ floating
         ^ ^ decimals
         ^fieldwidth

         {0} ==> {0:d}   

## Special Cases
### Alignment
* \> right
* < left

### Integer values
* x : hexadecimals
* b : binary
* fill spaces
* float exponential f --> e

# Command Line Arguments
### Module sys provides a variable argv- a variable of type list that contains the command line arguments as string
### Variable sys.argv
* len(sys.argv) >= 1
* the first element is the script name

### Program:
      import sys
      print('Program:', sys.argv[0])

      mysum = 0
      for k in range(1, len(sys.argv)):
          mysum += float(sys.argv[k])

      if len(sys.argv) == 1:
          print('No numbers.')
      else:
          print('Sum: ', mysum)

* Another solution:
      for element in sys.argv[1:]:
          mysum += float(element)
