# Project 5 Notes (help with JSON):
## What is a dictionary?
Review - A list is a sequence of elements, elements are accessible by indices

      l = [1231, 1257, 2357]
      l[1] = 1257

A dictionary is a container where elements are accessible via keys; a dictionary contains key-value pairs

      d = {'Bob':1231, 'Joe':1257, 'Eve':2357}
      #d is a dictionary with 3 elements
      #get Joe's phone number
      d['Joe'] = 1257

Keys must be unique

A dictionary is like a list where the indices may be any object; A dictionary is a map

'Bob' => 1231,
'Joe' => 1257,
'Eve' => 2357

      d = dict()
      d = {}
      d['Bob'] = 1231
      d['Joe'] = 1257
      d['Eve'] = 2357

      d['Joe']['place']

Earthquake:

A dictionary with the following keys
* 'type'
* 'metadata'
* 'features'
* 'bbox'

The value of element with key 'feature' is __a list of dictionaries.__

__Each dictionary describes an Earthquake.__

      d['properties']['mag'] => value of the magnitude

Feature is a dictionary that describes an Earthquake.
It has the following keys:
* 'type'
* 'properties'
* 'geometry' => is itself a dictionary

To extract magnitude:

if f is a feature:

      f['properties']['mag'] => mag
      f['geometry']['coordinates'][0] => longitude
      f['geometry']['coordinates'][0] => latitude

## Project function:

      def add_new_quakes(quakes, new_quakes_dict):
          newQuakes = False
          list_of_quakes = new_quakes_dict['features']

          for feature in list_of_quakes:
              #f is feature - dictionary
              quake = quake_from_feature(f)
              if not quake in quakes:
                  newQuakes = True
                  quakes.append(quake)
          return newQuakes
