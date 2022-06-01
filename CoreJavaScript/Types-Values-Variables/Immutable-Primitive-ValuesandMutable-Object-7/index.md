# Immutable Primitive Values and Mutable Object References

* There is a fundamental difference in JavaScript between primitive values (undefined, null, booleans, numbers, and strings) and objects (including arrays and functions).

* Primitives are immutable: there is no way to change (or “mutate”) a primitive value.

* Since strings are like arrays of characters, you might expect to be able to alter the character at any specified index.
In fact, JavaScript does not allow this, and all string methods that appear to return a modified string are, in fact, returning a new string value.

Example :

  <script>

var s = "hello"; // Start with some lowercase text

s.toUpperCase(); // Returns "HELLO", but doesn't alter s

console.log(s)

</script>

o/p :

hello

* Primitives are also compared by value: If two distinct string values are compared, JavaScript treats them as equal if, and only if, they have the same length and if the character at each index is the same.

Objects are different than primitives. First, they are mutable—their values can change:

var o = { x:1 }; // Start with an object

o.x = 2; // Mutate it by changing the value of a property

o.y = 3; // Mutate it again by adding a new property

var a = [1,2,3] // Arrays are also mutable

a[0] = 0; // Change the value of an array element

a[3] = 4; // Add a new array element


* Objects are not compared by value: two objects are not equal even if they have the same properties and values. And two arrays are not equal even if they have the same elements in the same order:


* Objects are not compared by value: two objects are not equal even if they have the same properties and values. And two arrays are not equal even if they have the same elements in the same order:

var o = {x:1}, p = {x:1}; // Two objects with the same properties

o === p // => false: distinct objects are never equal

var a = [], b = []; // Two distinct, empty arrays

a === b // => false: distinct arrays are never equal

* objects are compared by reference: two object values are the same if and only if they refer to the same underlying object.

var a = []; // The variable a refers to an empty array.

var b = a; // Now b refers to the same array.

b[0] = 1; // Mutate the array referred to by variable b.

a[0] // => 1: the change is also visible through variable a.

a === b // => true: a and b refer to the same object, so they are equal.


* As you can see from the code above, assigning an object (or array) to a variable simply assigns the reference: it does not create a new copy of the object.If you want to make a new copy of an object or array, you must explicitly copy the properties of the object
or the elements of the array.

var a = ['a','b','c']; // An array we want to copy

var b = []; // A distinct array we'll copy into

for(var i = 0; i < a.length; i++) { // For each index of a[]

b[i] = a[i]; // Copy an element of a into b

}


* if we want to compare two distinct objects or arrays, we must compare their properties or elements.

function equalArrays(a,b) {

if (a.length != b.length) return false; // Different-size arrays not equal

for(var i = 0; i < a.length; i++) // Loop through all elements

if (a[i] !== b[i]) return false; // If any differ, arrays not equal

return true; // Otherwise they are equal

}

