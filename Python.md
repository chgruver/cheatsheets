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
print(players[:4]) # prints the first 4 elements in the list
print(players[2:]) # prints all the elements from index 2 to the end
print(players[-3:]) # same as previous example
```

slices can also be used in for loops line a standard list

when working with lists use slices to copy a list
```python
my_foods = ['pizza', 'falafel', 'carrot cake']
friend_foods = my_foods[:] # copies my_foods into freind_foods

friend_foods.append('cannoli') # adds cannoli to friend_foods list
my_foods.append('ice cream') # adds ice cream to my_foods list

my_foods = ['pizza', 'falafel', 'carrot cake']
friend_foods = my_foods # both variables point to the same list
friend_foods.append('cannoli')
my_foods.append('ice cream')
# both variables point ot the list:
# ['pizza;, 'falafel', 'carrot cake', 'cannoli', 'ice cream']
```
## Tuples

Tuples are immutable lists

```python
dimensions = (200, 50)
print(dimensions[0])
print(dimensions[1])
my_tuple = (3,) # a one element tuple
```

## Conditionals

```python
car = 'bmw'
car == 'bmw' # evaluates to True

# conditionals are case sensitive
car = 'Audi'
car == 'audi' # evaluates to False
car.lower() == 'audi' # converts car to lower case to evaluate True

# Numerical Conditionals
age = 21
age == 21 # True
age == 19 # False
age != 21 # False
age != 19 # True
age < 21 # False
age <= 21 # True
age > 21 # False
age >= 21 # True 
```

Other conditional keywords include ```and```, ```or```, ```in```, and ```not```

## Dictionaries

```python
my_dictionary = { key: value, key2: value2, etc...}
```

THe ```del``` keyword is used to remove a key value pair from a my_dictionary

```python
del my_dictionary['key_to_remove']
```
