# Package Imports

## Introduction
What people refer to as "Python" is actually the combination of "Pure Python" and innumerable Python extension packages. The extension packages are not necessarily written in Python. Most often, they are written in C++, Fortran, Python, or Cython. C++, Fortran, and Cython have the benefits of often being several orders of magnitude (think 1000x–10000x) faster than Python, depending on the task. This can reduce an operation that might take minutes to a few milliseconds.

The other benefit of using packages is that they allow others to write code for us that can be reused. It doesn't make sense for people to write, say, a linear regression module every time they want to find the slope of a line. This is something that we can steal (borrow) from others using packages.

Packages have values, classes, and functions that you can use in your own programs. Examples would be, respectively, `np.pi`, `np.ndarray`, and `np.sin`.

On a related note, **never, *ever*, use `from package import *`**. This is terrible and kills baby puppies.

## Tasks
1. Import the package `numpy` and assign to it the name `np`. This should be done in one line. `numpy` is arguably the most important package in all of Python. Most scientific packages are in some way based on `numpy`. 
2. Access the variable `pi` from the Python package and assign it to the variable `circle_ratio`.
3. Try setting the value `3.14` to `np.pi`. What happens?
4. Calculate the sine of 90 degrees. Is this right? Calculate the sine of pi/2 radians.
5. Import the `scipy.constants` module as `sc`. There's a list of all of the different constants it contains [here](https://docs.scipy.org/doc/scipy/reference/constants.html). 