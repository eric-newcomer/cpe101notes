# Chapter 4.6 Performance
## Module time
      t = time.time()
* get current time in sec since Jan. 1, 1970
      s_time = time.time()
      # Call function
      e_time = time.time()
      d = e_time - s_time
* Find maximum by setting max initially to zero
      max = 0
* You could also set the first value as the minimum or maximum and compare the value with each following value

# Chapter 5: The data type 'list'
### A list is an ordered sequence of values
* elements of list tend to be of the same type (strings, ints, floats)
* elements of a list that are different types --> complicated

### A *list* is a built-in data type to store a sequence of values of any type
### A *sequence* is an ordered collection of items
      my_list = [element_1, element_2, element_3, ..., element_n]

      print(my_list[2]) # prints element_3

## 5.2 List Operations and Functions
### Example list
* list of elements of type string
      colors = ['green', 'blue', 'red']

* create an empty list and add elements afterwards
      colors = []
      colors.append('green') #added to end of list

      colors.append('blue')

* .append() adds an element at the end of list

### Create a list with many elements
      squares = []
      for k in range(1, 101):
        squares.append(k*k)
*output would be [1, 4, 9, 16, ....*]

### Get the number of elements with len()
      len(squares) --> 100

## 5.2.2 Access all elements of a list / Traverse a List
### Print all elements of squares
#### A)
      for k in range(len(squares)):
        print (squares[k])
#### B)
      for item in squares:
        print(item)
* Meaning:
#### Assign first element of the list to item and execute the body, then assign the second element of list to item and execute body...

### Write a function to calculate the mean of a list of floats
      def mean(times):
        tsum = 0

        for item in times:
          tsum = tsum + item

        tmean = tsum / len(times)
        return tmean

### Better Way:
      def mean(times):
        if len(times) == 0;
          return 'None'
        else:
          return sum(times)/len(times)

### Access the last element:
      times[len(times) - 1]
