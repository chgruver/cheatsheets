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

numbers = list(range(1, 6))
print(numbers) # [1, 2, 3, 4, 5]

digits = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]
min(digits) # >> 0
max(digits) # >> 9
sum(digits) # >> 45
```

## For Loops

Python uses indention for blocks of code such as for loops.

```python
for item in item_list:
    # do stuff

for value in range(start, end):
    # range goes from start to (end - 1)
```

## Slices

```python
players = ['charles', 'martina', 'michael', 'florence', 'eli']
print(players[0:3]) # prints the first three elements in the list
print(players[1:4]) # prints the elements from index 1 to index 4
# 'martina', 'michael', 'florence'

```
