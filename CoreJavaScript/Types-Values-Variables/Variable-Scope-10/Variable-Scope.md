# Variable Scope

The scope of a variable is the region of your program source code in which it is defined.

Global : A global variable has global scope; it is defined everywhere in your JavaScript code.


Local : They are local variables and have local scope. Function parameters also count as local variables and are defined only within the body of the function.

var scope = "global"; // Declare a global variable

function checkscope() {

var scope = "local"; // Declare a local variable with the same name

return scope; // Return the local value, not the global one

}

checkscope() // => "local"


Function definitions can be nested. Each function has its own local scope, so it is possible to have several nested layers of local scope. 

For example:

var scope = "global scope"; // A global variable

function checkscope() {

        var scope = "local scope"; // A local variable

        function nested() {

        var scope = "nested scope"; // A nested scope of local variables

        return scope; // Return the value in scope here

        }

        return nested();

}

checkscope() // => "nested scope"



## Function Scope and Hoisting


function scope: variables are visible within the function in which they are defined and within any functions that are nested within that function.

In the following code, the variables i, j, and k are declared in different spots, but all have the same scope—all three are defined throughout the body of the function:

function test(o) {
    
        var i = 0; // i is defined throughout function

        if (typeof o == "object") {

                var j = 0; // j is defined everywhere, not just block

                for(var k=0; k < 10; k++) { // k is defined everywhere, not just loop

                   console.log(k); // print numbers 0 through 9

               }

        console.log(k); // k is still defined: prints 10

        }

        console.log(j); // j is defined, but may not be initialized
}


