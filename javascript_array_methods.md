## JavaScript Array Methods

#####1.
Find out if something is indeed an array:

**Array.isArray(yourObj)**

The *Array.isArray()* method returns true if an object is an array, false if it is not.

- Why we need it instead of "typeOf"?
Because typeOf called on an array, will return Object.

#####2.
Find out if all values in array pass the test:

**arr.every(callback[, thisArg])** 

examples:

*[12, 5, 8, 130, 44].every(elem => elem >= 10);* // false

*[12, 54, 18, 130, 44].every(elem => elem >= 10);* // true

#####3.
Filter an array so that you have a new array only with items that passed the test:

**arr.filter(callback[, thisArg])**

example:

*function isBigEnough(value) {*

  *return value >= 10;*
  
*}*

*var filtered = [12, 5, 8, 130, 44].filter(isBigEnough);*

// filtered is [12, 130, 44]