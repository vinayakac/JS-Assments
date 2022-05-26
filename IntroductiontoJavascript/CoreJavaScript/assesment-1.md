 Question: write function to increment the value of variable
 
   var x=2;
   x = plus1(x);
   console.log(x);
function plus1(x) { // Define a function named "plus1" with parameter "x"
return x+1; // Return a value one larger than the value passed in
}

output:

3

////////

Q2: invoke two functions in one expression

 var y=3;
function plus1(x) { // Define a function named "plus1" with parameter "x"
return x+1; // Return a value one larger than the value passed in

}
var square = function(x) { // Functions are values and can be assigned to vars
return x*x; // Compute the function's value
}; // Semicolon marks the end of the assignment.
var a = square(plus1(y))
console.log(a);


output :

16


Q3.When we combine functions with objects

 var a = []; // Create an empty array
a.push(1,2,3); // The push() method adds elements to an array
console.log('pushed array :'+a)
a.reverse(); // Another method: reverse the order of elements
console.log('reversed array :'+a);

output:

pushed array :1,2,3
reversed array :3,2,1


Q4.Define a method to compute distance between points

var points = [ // An array with 2 elements.
{x:0, y:0}, // Each element is an object.
{x:1, y:1}
];
points.dist = function() { // Define a method to compute distance between points
var p1 = this[0]; // First element of array we're invoked on
var p2 = this[1]; // Second element of the "this" object
var a = p2.x-p1.x; // Difference in X coordinates
var b = p2.y-p1.y; // Difference in Y coordinates
return Math.sqrt(a*a + // The Pythagorean theorem
b*b); // Math.sqrt() computes the square root
};
points.dist() // => 1.414: distance between our 2 points
console.log('distance of points :'+ JSON.stringify(points));

output:
distance of points :[{"x":0,"y":0},{"x":1,"y":1}]


Q5: JavaScript statements include conditionals and loops using the syntax

function factorial(n) { // A function to compute factorials
var product = 1; // Start with a product of 1
while(n > 1) { // Repeat statements in {} while expr in () is true
product *= n; // Shortcut for product = product * n;
n--; // Shortcut for n = n - 1
} // End of loop
return product; // Return the product
}
var x =factorial(4) // => 24: 1*4*3*2
console.log('factorial :'+ (x));
output :
24
