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


This property does not exist, and the expression evaluates to undefined. This code demonstrates that strings, numbers, and boolean values behave like objects when you try to read the value of a property (or method) from them.

The temporary objects created when you access a property of a string, number, or boolean are known as wrapper objects, and it may occasionally be necessary to distinguish a string value from a String object or a number or boolean value from a Number
or Boolean object.