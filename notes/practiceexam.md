### 1. Create a list named mylist containing values 0, 2, 4, 6...100 in three different ways
a) For loop (no list comprehension)

      mylist = []
      for i in range(0, 101, 2):
          mylist.append(i)

b) while loop

      mylist = []
      i = 0
      while i <= 100:
          mylist.append(i)
          i += 2

c) List comprehenion

      mylist = [i for i in range(0, 101, 2)]

d) What are the values of the following?

      len(mylist)
      >>> 51

      mylist[-2]
      >>> 98

      mylist[1:3]
      >>> 2, 4

      mylist[:2]
      >>> 0, 2

### 2. Create a function named smallest that takes one parameter, being a list of lists of int values. It returns the smallest value contained in the list of lists. If there are no values, then None is returned.

      def smallest(m):
            minimum = None
            for innerlist in m:
                for item in innerlist:
                    if minimum == None:
                        minimum = item
                    else:
                        if item < minimum:
                            minimum = item
            return minimum

### 3. Write a function named createlists having parameter of type int. The function returns a list of lists containing integer values. First list contains value 1, second contains 1 and 2, third contains 1, 2, 3 and so on. Parameter specifies the number of lists. If parameter is none or 0, an empty list is created.

      def createlists(n):
            if n == 0:
                return []
            alist = []
            for i in range(n):
                blist = []
                for k in range(i+1):
                    blist.append(k+1)
                alist.append(blist)
            return alist
