# NumPy Array Basics

## Prerequisites
- List Basics

## Introduction
### A Brief Introduction to Objects
It's not often thought about, but every single piece of data in Python is stored in an "object" of some kind. Integers and floats are objects, and so are strings. Integers and floats are fairly low-level objects (although very high level compared to languages like C++). There are higher-level objects still.

The terms "higher" and "lower"-level refer to levels of abstraction. For example, the lowest-level form of an integer would be that integer's representation in binary, and a small amount of memory allocated to its identification as an integer. If we had to constantly work with such low levels of abstraction, programming would take forever. An example of a high-level object would be Python's `string` object. It is a collection of `char` objects, which themselves are objects with abstractions still. It's much nicer to work with strings than having to program every 128-bit `char` by yourself. However, low-level operations and storage routines are much faster than abstractions. In fact, the founding principle behind Python itself is higher levels of abstraction, because "programmer time is more important than execution time".

So, what does this have to do with NumPy? NumPy has defined what is probably the most important object in all of Python, the `ndarray` object. This is what has allowed Python to rise to a position of prominence in both scientific computing and data science.

### What is the `ndarray` object?
The object's name is short for "n-dimensional array". The shortest definition would be that it is a container for an *extremely* efficient implementation of array storage and operations. In practical terms, this means that it can store a ton of numbers (usually numbers, anyway) in an organized format and can do efficient (very, very efficient) operations on those numbers. In a way, this fills the gap left behind by Python lists, since we can't do any math on those.

## Tasks
1. Create an `ndarray` object using the [`zeros`](https://docs.scipy.org/doc/numpy/reference/generated/numpy.zeros.html#numpy.zeros) method. It should contain a (3x2) array (that is, 3 rows and 2 columns). Print it out using `print`.
	1. Add the literal value `1` to this array.
	2. Divide the array by `0.5`.
	3. Print it out.
2. Create another (3x2) `ndarray` object using the [`array`](https://docs.scipy.org/doc/numpy/reference/generated/numpy.zeros.html#numpy.array) method to construct the array from lists. Access the documentation to see how. Give it values of your choosing.
	1. Check to see that its dimensions are correct using the `shape` attribute (notice how I say attribute instead of method, because `shape` is not a function. You do not use `()`. 
	2. Multiply this array by the original you generated. Note that they *do not obey matrix multiplication*. Instead, they perform what is known as "element-wise" multiplication. It's the easy way—it simply goes element-by-element and multiplies them together.
	3. Check the type of data your array can store using the `dtype` method. Note that NumPy array elements must all be the same data type.
3. Test the list-indexing syntax on the arrays you've generated.
	1. Start by simply slicing the array with `array_name[:]`. As expected, you should get back the entire array.
	2. Then, try `array_name[:1]`. It should return only a subset of the rows. That's because, in an *n*-dimensional array, the first index corresponds to the first dimension (also referred to as an "axis"). (Note again: is the final bound inclusive or exclusive?)
	3. Try "multi-index slicing", as in `array_name[:2, 2]`.
4. Try some basic aggregation functions.
	1. Create a new, 1-dimensional array using the [`linspace`](https://docs.scipy.org/doc/numpy/reference/generated/numpy.zeros.html#numpy.linspace) command. Look it up.
	2. The `sum` method will do exactly as it suggests. Try it out on your 1D array.
	3. The `sum` method's behavior may seem strange on multi-dimensional arrays. Try it out on one you've previously created. Try supplying the `axis` parameter. Look at the [documentation](https://docs.scipy.org/doc/numpy/reference/generated/numpy.ndarray.sum.html#numpy.ndarray.sum) to see how it works. What is the default?
	4. Sum one of your multidimensional arrays such that each row gets replaced by its sum. Save this result into another array. Use the `shape` attribute to see the new dimensions. 

## References
A good general reference would be NumPy's own [reference page](https://docs.scipy.org/doc/numpy/reference/arrays.ndarray.html) for the `ndarray` object. However, this gets fairly technical with implementation details.

A more user-focused reference can be found [here](https://docs.scipy.org/doc/numpy/reference/generated/numpy.ndarray.html), which is the API (application programmer interface) documentation. This is where almost all of the necessary information can be found on the `ndarray` class (class can be a synonym for object).

There are also many links provided in the exercises themselves.

