## What is a Sequence?
```python
#List: modifiable, versatile, general purpose
programming_languages = ["bash", "Python", "HTML", "CSS", "Javascript", "SQL"]

#Tuple: not modifiable, best for things with a fixed size
gps_coordinates = (33.848673, -84.373313)

#Range: lists of numeric values
numbers_from_zero_to_a_million = range(1000000)
```
### To Creat a List
- Assign a list at least one variable
- seperate by commas
- square brackets [] on each end

Example:
```python
my_favorite_people = ["Eddie", "Ella and Eli", "Sisters", "Parents"]
```
In this list, the indexes are as follows:

- 0 is Eddie
- 1 is Ella and Eli
- 2 is Sisters
- 3 is Parents

The initial index is zero. Therefore:

```python
first_item = my_favorite_people[0]

print("The first person I love is: ", my_favorite_people[0])
#will be the same as
print(first_item)
#You can print directly from the list, as the first example, or creat variables from the list.
```

IndexError will occur if you try to use an index that is outside of the range. This can be handled with try/except.

Special notes:
- To access the last item: use -1
- To print the entire list, just print(my_favorite_people)
- To print some of the list, *slice* it by using : print(my_favorite_people[1:3])
    - the first number (starting) will be included
    - the second number (ending) will **NOT** be included
    - if you don't have a starting index ([:2]), it will start at the beginning
    - if you don't have an ending index ([2:]), it will go to the end
    - you *can* use negative indexes with splicing
-


**Iteration**- using a loop to access the sequence's items 