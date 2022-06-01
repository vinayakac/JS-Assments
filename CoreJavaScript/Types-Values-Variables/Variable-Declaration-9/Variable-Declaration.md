# Variable Declaration

Variables are declared with the var keyword, like this:

var i;

var sum;

You can also declare multiple variables with the same var keyword:

var i, sum;

And you can combine variable declaration with variable initialization:

var message = "hello";

var i = 0, j = 0, k = 0;

for loop

for(var i = 0; i < 10; i++) console.log(i);

for(var i = 0, j=10; i < 10; i++,j--) console.log(i*j);

for(var p in o) console.log(p);

## Repeated and Omitted Declarations

It is legal and harmless to declare a variable more than once with the **var** statement. If the repeated declaration has an initializer, it acts as if it were simply an assignment statement.

