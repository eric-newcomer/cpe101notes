# Wednesday: 1/31/18 - Chapter 4 continued
## 4.1.1: Nested Loops
* A table is printed row by row
* Each table is printed from left to right
* Pseudocode:
      for all rows r
        for all columns in rows
          print column c
        create a new line

* Code:
      rows =
      cols =
      for r in range(1, rows+1):
        for c in range(1, columns+1):
          print('%3d' % c)
        print()

* Single Loop:
      for k in range(1, columns*rows+1):
        print('%3d' % k)

* 3 Nested Loops:
      for h in range(24):
        for m in range(60):
          for s in range(60):
            print('%02d:%02d:%02d' % (h, m, s))

* Single Loop Version of above code:
      s = 0
      m = 0
      h = 0
      for k in range(86400): #86400 is = to 24*60*60
        s = s + 1
        if s == 60:
          s = 0
          m = m + 1
          if m == 60:
            m = 0
            h = h + 1
        print('%02d:%02d:%02d' % (h, m, s))

* Single again:
      for k in range(86400):
        h = k//3600
        rem = h%3600
        m = rem//60
        s = rem % 60
        print('%02d:%02d:%02d' % (h, m, s))

## 4.5: Square Root
### Heron's Method:
      Iteration: xsub(n+1) = (1/2) * (xsub(n) + x/(xsub(n)))
* For each positive initial value x, the following holds:
      lim as n --> infinity of xsub(n) = sqrt(x)
