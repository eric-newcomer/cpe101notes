## 3.6: Calculations with Boolean Variables
### Assume: a, b, and c are Boolean Variables
* x = (a and b) or (not(a) and c)

### Rules for Boolean Calculations
### DeMorgan Rules 1, 2, and 3
#### 1)
      not(not a) = a
#### 2)
      not(a and b) = (not a) or (not b)
#### 3)
      not (a or b) = (not a) and (not b)
### Example
      a = x > 10
      b = y > 20
      not ((x > 10) and (y > 20))
      = (not(x > 10) or (not(y>20))
      = (x <= 10) or (y <= 20)
#### Proof:
* Check all possibilities

      a=1,b=1
      a=0,b=1
      a=1,b=0
      a=0,b=0

# Chapter 4: Iterations - Loops (while and for loops)
## 4.1: Iterations and Loops
### while statement
      def main():
        print('  k  k*k  k**3')
        k = 1
        while k <= 10: #once statement is false, the print statement will be executed
          k2 = k*k
          k3 = k**3
          print(k, k2, k3)
          k = k + 1
        print('Finished')
#### Format:
      while "condition":
        "statements"
### Flow Diagram
* Used to visualize a program
      k = 1
        |
        |
        |
      k <= 10 --------> True
        |                |
        |                |
        |                |
        False          k2 = k*k
                      k3 = k**3
                      print(k = k+1)  

### Problem 2:
* need a variable to count the numbers that have been processed, count = 0
* a) use a helper variable - Flag - valid
      count = 0
      valid = True

      while valid:
        k = int(input('Enter a number'))
        if k > 0:
          square = k*k
          print(k, square)
          count = count + 1
        else:
          valid = False
      print(count)

* b) endless loop + break statement
      count = 0
      while True:
        k = int(input('Number'))
        if k < 1:
          break #-------------> Typing break will exit the while loop
      print('Processed ', count, ' numbers.')
* break statement: jump out of the surrounding while or for loop

* Note: break is often used inside an if statement, but the program won't jump out of the surrounding while statement.

#### Example
      k = -1
      while k<50 or k>100:
        k = int(input('Enter a number: '))
* Note: valid input would be 50<=k and k <=100
* Invalid would be k<50 or k>100
