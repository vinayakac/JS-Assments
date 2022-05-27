# Optional Semicolons:

- JavaScript uses the semicolon (;) to separate statements (see Chapter 5) from each other.

- use semicolons to explicitly mark the ends of statements, even where they are not required.

- Consider the following code. Since the two statements appear on separate lines, the
first semicolon could be omitted:
a = 3;
b = 4;

- Consider the following code:
var a
a
=
3
console.log(a)

- JavaScript interprets this code like this:
var a; a = 3; console.log(a);

- Ex :2

var y = x + f
(a+b).toString()

JavaScript interprets the code like this:
var y = x + f(a+b).toString();


- Ex : 3

x
++
y

It is parsed as x; ++y;, not as x++; y.