# 5.4: Map | Filter | Pattern | List Comprehension
## Map Pattern:
### A list is given; apply an operation (expression) on each element of the list - get a new value for each element of the given list; put all new values into a new list

### Example Map Pattern:
### list of temperatures in fahrenheit; create a list of " " celsius.
      def f2c(f): #mapping
        return 5/9*(f-32)

      def mapf2c(flist):
        clist = []
        for fItem in clist:
          cItem = f2c(fItem)
          clist.append(cItem)
        return clist

### Simpler: List Comprehension
### Form: [{expression}{iterate over all elements}]
      clist1 = mapf2c(flist)

      clist2 = [f2c(x) for x in flist]
### List Comprehension
      [expression for <item> on <list>]

### Example: Square nums from 1 to 100:
      sq = [k*k for k in range (1, 101)]

### List Comprehension for Filter Pattern:
      [expression for <item> in <list> if <condition>]

      *Get all values between 10 and 20: 10 < x < 20*
      positive = [x for x in mylist if 10<x<20]

      *Get all square values between 10 and 20*
      sq = [x*x for x in mylist if 10<x<20]

# 5.5: Tuples
## Tuples are similar to lists, however once created, they can't be modified; tuples are immutable
      t = (1, 2, 3) == t = 1, 2, 3
      *t is of type tuple*
      x = t[2]
      t[2] = 144
### Note:
      t = 5     t = (5) --> creates int
      t = 5, t = (5,)   --> creates tuple
      t_tuple = 5,

### Example:
      ax^2 + 6x + c = 0

      def solve(a, b, c):
        d = math.sqrt(b*b-4*a*c)
        x1 = 0.5*(b+a)/a
        x2 = 0.5*(-b-a)/a
        return x1, x2
### Calling solve():
      s = solve(3, 4, 5)
      # s[0] = x1
      # s[1] = x2

      # shortcut
      s1, s2 = solve(3, 4, 5)
      *first element of tuple is assigned to s1, 2nd element
      is assigned to s2*

### Application:
      def assertListAlmostEqual(l1, l2):
        for el1, el2 in zip(l1, l2):
          self.assertAlmostEqual(el1, el2)


      mylen = min(len(l1), len(l2))
      for k in range(mylen):
        el1 = l1[n]
        el2 = l2[k]
-------------
# Chapter 6: Strings
## Typical Problems --> Making a password
