# Wrapper Objects

The primitive wrapper types make it easier to use primitive values including booleans, numbers, and strings.

Example :

let language = 'JavaScript';

let s = language.substring(4);

console.log(s);  // Script



There are not wrapper objects for the null and undefined values:

var s = "test"; // Start with a string value.

s.len = 4; // Set a property on it.

var t = s.len;

console.log(t)

o/p:

undefined



When you run this code, the value of t is undefined. The second line of code creates a temporary String object, sets its len property to 4, and then discards that object. The third line creates a new String object from the original (unmodified) string value and then tries to read the len property. This property does not exist, and the expression evaluates to undefined.
