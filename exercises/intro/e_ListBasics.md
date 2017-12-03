# List Basics

## Prerequisites
- Variables and Assignments
- Package Imports

## Introduction
In programming, a common task is to create a collect of objects in your code. This can be used to efficiently manage data and other objects without having to retype them over and over. For example, consider the task of printing all numbers in a database which are greater than some cutoff number. In order to automate the saving of those "successful" numbers, some kind of collection mechanism is needed.

In Python, that mechanism is the `list` object. The `list` object is incredibly dynamic in Python, much more so than in most languages. However, the trade-off, as always, is speed. For most operations, the `list` object isn't bad. However, iterating over it is always slow.

## Tasks
1. Create a list of four integers.
	1. Add to that list the string literal `'hello'` using the `append` method. Print out the list.
	2. Create a variable and assign to it the string `'goodbye'`. Add this variable to the list.
	3. Reassign the string literal `'hello again'` to the variable which formerly held `'goodbye'`. Print out the list.

2. Index some lists.
	1. Select the third element of the list by its index. Remember that in computer programming, lists and arrays and the like are zero-indexed, meaning the first element is found at index 0, and the third therefore at index 2.
	2. Choose only the first **three** elements of one of your lists. Use slicing notation (`your_list[initial:final]`). Is the first element inclusive or exclusive? The last?
	3. Neglect to put in an initial bound. Leave only the final (`your_list[:final]`). What changes?
	4. Neglect to put both bounds in. This is an efficient way to select all elements. There *are*, in fact, instances where this is useful (and necessary).
	5. Put in a negative index and see what happens. Using `your_list[-1]` is an efficient (in programmer time) way to select the last element of a list.

3. Lists can hold practically anything.
	1. Create a blank list like this: `[]` and store it in a variable.
	2. Append the numbers `4`, `8`, `15`, `16`, and `23` into this list, all as separate elements.
	3. Create another blank list and store it in another variable.
	4. Append into your new blank list the numbers `1`, `1`, `2`, `3`, `5`, and `8`, all as separate elements.
	5. Create a final list of the previous two lists, and store it as a third variable (`list_of_lists = [list1, list2]`).
	6. Append the number `42` into the first list, but do it to the copy of the list which is stored in the list of lists. This can be done by first indexing the list of lists, and then "chaining" the append command, as follows: `list_of_lists[0].append(42)`.

4. Object Permanance for Infant Programmers
	1. Create a new list with the elements `1` and `2`. Print the list.
	2. Assign the integer literal `3` to a new variable.
	3. Append this variable into the list. Print the list.
	4. Assign the integer literal `4` to the variable which previously stored `3`. Print the list. Anything surprising?
	5. Create a new list of elements {`8`, `9`, `10`}, and store it in a new variable. Print it out. 
	6. Append this new list (via the new variable) into the original list. Print it out.
	7. Change the element `8` of the new list to `11`. Print out the original list. Anything surprising?

5. Try a list comprehension, and use it to do some math.
	1. Create a list of the numbers 0 through 4 using the `list()` function and the `range()` function. Try [this link](https://stackoverflow.com/questions/23221025/does-range-really-create-lists#23221045) if you are stuck for more information on what range really is (it's something called a "generator" object.)
	2. Say we want to double every number in the list we just made, and then assign this new list to another variable, all in one line. This is possible with a list comprehension. Try this: `new_list = [x*2 for x in old_list]`. Most people say you can't do math with lists. That's not technically true. We just did. It *is*, however, true that this method is inferior in every conceivable way to using the NumPy library and the `ndarray` object.


## References
There is an excellent introduction to lists [here](http://www.effbot.org/zone/python-list.htm).