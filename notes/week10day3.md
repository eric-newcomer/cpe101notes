# Final Exam Info
## Exam will have questions that use Python 2

Python2 ---> Python3

print 'A', ---> print('A', end='')

# Project 6 Notes
      python3 spot_blur.py filename rowc colc radius [reach]

* either 5 or 6 command line arguments
* use sys.argv
      if not 4 < len(sys.argv) < 6:
          print("Error message")
          return

      filename, rowc, colc, radius, reach = getParameter(sys.argv[1:])


      def getParameter(argList):
          filename = argList[0]
          row_center = int(argList[1])

      width, height, color_depth, image = readImage(fin)

      image = [ [...], [...], [...], [...]... ]
      #each sublist describes a row; they are each a Pixel
      height = len(image)

      px = image[r][c]

## Blurring an image
### Blur completely:
for each pixel, replace the values of (r, g, b) by the average of the color components in the surrounding boxes

      r = (r[row-1, col-1] + r[row-1][col] + r[row-1][col+1] + r[row][col-1])

      reach = 1

      def fullyBlurredPixel(image, r, c, reach):
          cols = [0, 0, 0]
          count = 0
          for y in range(r-reach, r+reach+1):
              if 0 <= y < len(image): #height
                  for x in range(c-reach, c+reach+1):
                      if 0 <= x < len(image[0]):
                          count += 1
                          cols[0]=cols[0]+image[y][x].r
                          cols[1]=cols[1]+image[y][x].g
                          cols[2]=cols[2]+image[y][x].b
          return Pixel(int(cols[0])/count), int(cols[1]/count)

      def weigh():
          
