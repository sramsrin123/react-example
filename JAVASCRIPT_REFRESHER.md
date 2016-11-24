# JAVASCRIPT REFRESHER

+ Source: https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript

#### Overview
- JavaScript does not have classes. The class functionality is accomplished by
object prototypes.
- The other main difference is that functions are objects, giving functions the
capacity to hold executable code and be passed around like any other object.
- There's no such thing as an integer in JavaScript
- Convert string to number: parseInt("11", 10); // String, Base

#### Variables
- let allows you to declare **block-level** variables.
~~~~//myLetVariable is *not* visible out here

    for( let myLetVariable = 0; myLetVariable < 5; myLetVariable++ ) {
        //myLetVariable is only visible in here
    }

    //myLetVariable is *not* visible out here
~~~~
- const allows you to declare variables whose values are never intended to change. The variable is available from the function block it is declared in.

- var is the most common declarative keyword. An important difference between JavaScript and other languages like Java is that in JavaScript, blocks do not have scope; only functions have scope. So if a variable is defined using var in a compound.  A variable declared with the var keyword is available from the function block it is declared in.
~~~~//myVarVariable *is* visible out here

  for( var myVarVariable = 0; myVarVariable < 5; myVarVariable++ ) {
     //myVarVariable is visible to the whole function
  }

  //myVarVariable *is* visible out here
~~~~

#### Objects
- JavaScript objects can be thought of as simple collections of name-value pairs.
Like associative arrays in PHP
~~~~
var obj = {
  name: "Carrot",
  "for": "Max",
  details: {
    color: "orange",
    size: 12
  }
}
obj.details.color; // orange
~~~~
- Object prototypes
~~~~
function Person(name, age) {
  this.name = name;
  this.age = age;
}

Person.prototype.firstNameCaps = function firstNameCaps() {
  return this.first.toUpperCase()
};

s = new Person("Simon", "Willison");
s.firstNameCaps(); // SIMON
~~~~

#### Functions
- Functions have access to an additional variable inside their body called arguments, which is an array-like object holding all of the values passed to the function
~~~~
function avg(...args) {
  var sum = 0;
  for (let value of args) {
    sum += value;
  }
  return sum / args.length;
}

avg(2, 3, 4, 5); // 3.5
avg.apply(null, [2, 3, 4, 5]); // 3.5
~~~~
- The avg() function takes a comma separated list of arguments — but what if you want to find the average of an array you can use apply

- Anonymous functions: It's extremely powerful, as it lets you put a full function definition anywhere that you would normally put an expression.
~~~~
var a = 1;
var b = 2;

(function() {
  var b = 3;
  a += b;
})();

a; // 4
b; // 2
~~~~
