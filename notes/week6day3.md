# Chap 6.1-1: How does a computer store characters?
## Mapping:
### 'A' --> ord('A') --> 65
### 65 --> chr(65) --> 'A'

### Count the number of vowels in a given string?
* Use the membership operator
      vowels = 'aeiouAEIOU'
      count = 0
      for c in my_str:
          if c in vowels:
              count += 1
      print(count)

### Convert all small numbers in a given string to capital letters
* One way
      delta = ord('a') - ord('A')
      cstr = ''
      for c in my_str:
          if ord('a') <= ord(c) <= ord('z'):
              c = chr(ord(c) - delta)
          cstr += c
      print('6 convert upper: ', cstr)

* Another Way
      clist = []
      for c in my_str:
          if ord('a') <= ord(c) <= ord('z'):
              clist.append(chr(ord(c) - 32))
          else:
              clist.append(c)  
      ustr = ''.join(clist) #join is a string method

# 6.3 String Function Methods
## 1) '@' contained in my_str
      found = '@' in my_str

      k = my_str.find('@')
      #return index of first occurrence

      found = my_str.find('@') >= 0

      found = my_str.index('@') >= 0 #error of '@' is not found

## 6.3-3: String Functions
### str.find(sub[, start[, end]])
* return the lowest index in the string where substring *sub* is found within the slice s[start:end]
      position = str1.find('abc')
* str.index(sub[, start[,end]])
      position = str1.index('abc')
* str.isupper(sub[, start[, end]])
      value = str1.isupper()
