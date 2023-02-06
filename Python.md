# Python Cheat Sheet

## Lists

```python
# To create lists
list_name = [] # empty list
list_name = [1, 2, 3, 4, 'etc.'] # list with 5 items

# to add to lists
list_name.append(6) # adds 6 to the end of the list
list_name.insert(3, 42) # places 42 at position 3 in the list

# removing items from a list
del list_name[1] 
# removes the second element (position 1) in the list

popped_item = list_name.pop() 
# this places the last item in the list into the variable popped_item
pop_first = list_name.pop(0)
# this places the item at index 0 into the variable pop_first

# removing from a list by value
list_name.remove('etc.') 
# removes the value 'etc.' from the list

# Sorting a list
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.sort() # places the cars list into alphabetical order the argument reverse=True reverses the sort order

cars = ['bmw', 'audi', 'toyota', 'subaru']
print(sorted(cars)) 
# original list is untouched but prints out the list sorted

cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.reverse() # reverses the order of the list

cars = ['bmw', 'audi', 'toyota', 'subaru']
len(cars) # produces the length of the list cars

```
