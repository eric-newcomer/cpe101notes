# Chapter 10: Sorting
## Sorting the Elements of a List
Problem: Sort the elements of a given list in ascending order.

      m = [7, 9, 3, 6, 8]
      m.sort()
      # result: m = [3, 6, 7, 8, 9]

## 10.4: Sorting Algorithms
Write a function that sorts the elements of a list of integer values

      l1 = [7, 9, 3, 6, 8]

### Selecting Sort:
1) Find the smallest element and swap it with the first element

      min-index = 0, 2
      min-value = 7, 3

2) Find the smallest element starting with the second element

      min-index = 1, 2, 3
      min-value = 9, 7, 6

3) Start at third element

      min-index = 2
      min-value = 7
      # Swap element with itself

4) Start at fourth element

      min-index = 3 -> 4
      min-value = 9 -> 8

with n elements, there are (n-1) steps

      def selection_sort(list):
          for m in range(len(list) - 1):
              min_index = m
              for n in range(m+1, len(list)):
                  if list[n] < list[min_index]:
                      min_index = n

              temp = list[m]
              list[m] = list[min_index]
              list[min_index] = temp

              #Shortcut
              list[m], list[min_index] = list[min_index], list[m]

Find the minimum in a sublist

### Questions:
* What happens if numbers are the same?
__The program will run as normal__
* Runtime will increase exponentially.
__If you have a list with twice the elements, it will take four times as long.__

## 10.5: Performance
### 2 Approaches:
* Theoretical: count the number of comparisons for a list with n Elements
* Experiment: Sort a list with 1000 and 2000 elements and calculate the cpu-time
      l = [0] * 1000
      #Generate a list with random numbers
      #Use module random to create lists containing random numbers

Create a list of int-values:

      m = [0]
      for k in range(1000):
          m.append(random.randint(0, 1000))

List Comprehension:

      m = [ random.randint() for k in range(1000)]

### Improvements:
experiments with

10, 100, 1000, 10000, ...

100, 200, 400, 8000

1) need variable count and factor

2) Code

      lists = []
      count = 10
      factor = 10
      for k in range(5):
          lists.append([random.randint(0, 10000) for k in range(count)])
          count = count * factor
