# 5.2.3: Removing an Element
* Method pop(index) removes element at position index from the list
      numbers = [10, 20, 30]
      x = numbers.pop(1) --> [10, 30]
      numbers.pop(1) --> [10]
      numbers.pop(1) --> Error
numbers.pop() --> removes the last element

# 5.2.4: Inserting an Element
      colors = ['red', 'green']
      colors.insert(1, 'blue') --> ['red', 'blue', 'green']

# 5.2.3: List Reference and Copying List
* 1) numbers = [10, 20, 30]
* 2) my_numbers = numbers
* 3) my_numbers.append(40)
      THERE IS ONLY ONE LIST
      my_numbers refers to numbers !!

## Function list creates a copy of a list
      numbers = [10, 20, 30]
      my_numbers = list(numbers)
      my_numbers.append(40)

      def copylist(l1):
        l2 = []
        for element in l1:
          l2.append(element)
        return l2

      my_numbers = copylist(numbers)

# 5.2.4: Finding Elements
      l1 = [2, 10, 3, 5, 10, 7]
* is 10 in the list?
      if 10 in l1:
        print('10 is in list')
      else:
        print('10 is not in list')    
* return the first index of value 10
      i1 = l1.index(10)
      print(i1)
      
#### index(value, startIndex)
* how often is 10 in the list

      # get all indices with value 10
