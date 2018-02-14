# Chapter 6: Strings (continued)
### Type string is a built-in data type. A string is an **immutable** sequence of characters.
      isInstance(value, type):
      |
      |
      |
      |
      def f(p):
        if isInstance(p, str)
          pass
        elif isInstance(p, int)
* there is no char type
* conversion function
* + concatenation , *

### escape characters
* \n ---> n gets a new meaning
* \t  
* \%
* \' ---> removes a special meaning
      'Is\'nt'
      "Is'nt"

## 6.1: How does a computer store characters?
### For each character, a corresponding number is stored. There is a mapping between characters and numbers
* Mapping is reversible
* for each character is a unique number is necessary
* You must specify character set outside of US

### ASCII-Code (American Standard Code for International Exchange)
      65 ---> A
      50 ---> 2
      A->Z ---> 65->90
      a->z ---> 97->122
      48->57 ---> 0->9
* established in 1960
* all printable char 32-127
* non-printable 0-31 ---> used for data communication
#### Extended ASCII code (outside US)
* 0 to 255 ---> some characters
* western Europe
* Greek
#### Problem: different ASCII codes use different numbers
#### Why 32-127? (Because it's 7 bits)
* 8 bits = 1 byte
#### Chinese use Unicode! (because there's over 100k characters)

## 6.2: Unicode - Python - ord - chr
### Python uses Unicode to stores characters
* 100,000 char are mapped to numbers
* the first 127 characters are identical to the ASCII-Code

### Built-in Function: ord and chr
      chr(65) ---> 'A'
      ord('A') ---> 65
### print the Euro-Symbol
      str = '$ - ' + chr(8364) ---> '$ - €'

## Application of ord and chr
### 1) Check whether a string contains '@'
* iterate over all elements (similar to list)
      found = False
      for c in my_str:
        if c == '@'
          found = True
          break
        else:
          print('Not here')
      print(found)
* simple solution
      found = '@' in my_str

### 2) Return index of first element whose value is equal to 'x'
      first = -1 #Not found

      for k in range(len(my_str)):
        if my_str[k] == 'x'
          first = k
          break
      print(first)

### 3) Find capital letters within the String
      count = 0
      for c in my_str:
        if ord('A') <= ord(c) <= ord('Z'):
          count += 1
      print(count)

### 4) Count the number of digits
      if ord('0') <= ord(c) <= ord('9'):
        str = '7'
        k = ord(str) - ord('0')
        k = int(str)
