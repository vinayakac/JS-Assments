# Numbers

Unlike many languages, JavaScript does not make a distinction between integer values and floating-point values. All numbers in JavaScript are represented as floating-point values.

The JavaScript number format allows you to exactly represent all integers between −9007199254740992 (−253) and 9007199254740992 (253), inclusive.

* When a number appears directly in a JavaScript program, it’s called a numeric literal.



## Integer Literals 

* In a JavaScript program, a base-10 integer is written as a sequence of digits. For example:

0

3

10000000

## Floating-Point Literals

 Floating-point literals can have a decimal point; they use the traditional syntax for real numbers. A real value is represented as the integral part of the number, followed by a decimal point and the fractional part of the number.

 For example:\
3.14\
2345.789\
.333333333333333333\

 Floating-point literals may also be represented using exponential notation: a real number followed by the letter e (or E), followed by an optional plus or minus sign, followed by an integer exponent.

 Example :

 6.02e23 // 6.02 × 1023\
1.4738223E-32 // 1.4738223 × 10−32\

## Arithmetic in JavaScript

JavaScript programs work with numbers using the arithmetic operators that the language provides. These include + for addition, - for subtraction, * for multiplication, / for division, and % for modulo (remainder after division). Full details on these and other operators

In addition to these basic arithmetic operators, JavaScript supports more complex mathematical operations through a set of functions and constants defined as properties of the Math object:

Math.pow(2,53) // => 9007199254740992: 2 to the power 53\
Math.round(.6) // => 1.0: round to the nearest integer\
Math.ceil(.6) // => 1.0: round up to an integer\
Math.floor(.6) // => 0.0: round down to an integer\
Math.abs(-5) // => 5: absolute value\
Math.max(x,y,z) // Return the largest argument\
Math.min(x,y,z) // Return the smallest argument\
Math.random() // Pseudo-random number x where 0 <= x < 1.0\
Math.PI // π: circumference of a circle / diameter\
Math.E // e: The base of the natural logarithm\
Math.sqrt(3) // The square root of 3\
Math.pow(3, 1/3) // The cube root of 3\
Math.sin(0) // Trigonometry: also Math.cos, Math.atan, etc.\
Math.log(10) // Natural logarithm of 10\
Math.log(100)/Math.LN10 // Base 10 logarithm of 100\
Math.log(512)/Math.LN2 // Base 2 logarithm\


Arithmetic in JavaScript does not raise errors in cases of overflow, underflow, or division by zero.

When the result of a numeric operation is larger than the largest repre-
sentable number (overflow), the result is a special infinity value, which JavaScript prints as **Infinity**. Similarly, when a negative value becomes larger than the largest representable negative number, the result is negative infinity, printed as **-Infinity**.

Underflow occurs when the result of a numeric operation is closer to zero than the smallest representable number.


Division by zero is not an error in JavaScript: it simply returns infinity or negative infinity.

Infinity // A read/write variable initialized to Infinity.\
Number.POSITIVE_INFINITY // Same value, read-only.\
1/0 // This is also the same value.\
Number.MAX_VALUE + 1 // This also evaluates to Infinity.\

Number.NEGATIVE_INFINITY // These expressions are negative infinity.\
-Infinity
-1/0
-Number.MAX_VALUE - 1

NaN // A read/write variable initialized to NaN.
Number.NaN // A read-only property holding the same value.
0/0 // Evaluates to NaN.

Number.MIN_VALUE/2 // Underflow: evaluates to 0
-Number.MIN_VALUE/2 // Negative zero
-1/Infinity // Also negative 0
-0

## Binary Floating-Point and Rounding Errors


* when you’re working with real numbers in JavaScript, the representation of the number will often be an approximation of the actual number.

* Binary floating-point representations cannot exactly represent
numbers as simple as 0.1.

var x = .3 - .2; // thirty cents minus 20 cents\
var y = .2 - .1; // twenty cents minus 10 cents\
x == y // => false: the two values are not the same!\
x == .1 // => false: .3-.2 is not equal to .1(Rounding errors)\
y == .1 // => true: .2-.1 is equal to .1\


* Because of rounding error, the difference between the approximations of .3 and .2 is not exactly the same as the difference between the approximations of .2 and .1. It is




## Dates and Times

Core JavaScript includes a Date() constructor for creating objects that represent dates and times.

var then = new Date(2010, 0, 1); // The 1st day of the 1st month of 2010
var later = new Date(2010, 0, 1, // Same day, at 5:10:30pm, local time
17, 10, 30);
var now = new Date(); // The current date and time
var elapsed = now - then; // Date subtraction: interval in milliseconds


later.getFullYear() // => 2010\
later.getMonth() // => 0: zero-based months\
later.getDate() // => 1: one-based days\
later.getDay() // => 5: day of week. 0 is Sunday 5 is Friday.\
later.getHours() // => 17: 5pm, local time\
later.getUTCHours() // hours in UTC time; depends on timezone\


later.toString() // => "Fri Jan 01 2010 17:10:30 GMT-0800 (PST)"\   
later.toUTCString() // => "Sat, 02 Jan 2010 01:10:30 GMT"\
later.toLocaleDateString() // => "01/01/2010"\
later.toLocaleTimeString() // => "05:10:30 PM"\
later.toISOString() // => "2010-01-02T01:10:30.000Z"; ES5 only\