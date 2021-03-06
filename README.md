<script>
we can add the script element in two places, in the head section or in the body section.
The best practice is to put the script element at the end of the body section after all existing elements.

Why the best practice is to put the script element at the end of the body section?

There are two reasons for that:

1. The browser parses this file from top to bottom. So, if you put the script element in the head section, you might have a lot of JavaScript code there, so your
browser might get busy parsing and executing that JavaScript code, and it wont be able to render the content of the page. So this will create a bad user experience.
Your user looks at your web page it's white or blank, while your browser is busy parsing and executing your JavaScript code.

2. Almost always the code that we have in between script elements needs to talk to the elements on this web page. For example, we may want to show or hide some elements.
So by adding the code at the end of the body section, we'll be confident that all these elements are rendered by the browser. Now there are exceptions to this rule,
sometimes you're using third part code that has to be placed in the head section But these are exceptions.

console.log('Hello World');

A statement is a piece of code that expresses an action to be carried out. In this case we want to log a message on the console.
All statements in JavaScript should be terminated by a semi colon (;).

'Hello World'

These is a string, a string is a sequence of characters.

//

Two lashes represents a comment.

variable: is a storage location (identified by a memory address) paired with an associated symbolic name, which contains some known or unknown quantity of information
referred to as a value.

To declare a variable:

let name = '';
console.log(name);

Rules:
* Cannot be a reserved keyword (if, else, var...).

* Should be meaningful.

* Cannot start with a number (1name).

* Cannot contain a space or hyphen (-), use camel notation (firstName).

* Are case-sensitive.

    exemple:

    let firstName;
    let FirstName;
    These two variables are different.

Constant: Data values that stay the same every time a program is executed.

What are the kind of values that we can assign to a variable?
In JavaScript we have two caategories of types:

Primitives/ Value Types; String, number, Boolean, undefined and null.

    let name = 'Larissa'; // String Literal
    let age = '18'; // Number Literal
    let isApproved = true; // Boolean literal
    let firstName = undefined;
    let lastName = null; // use null in situations where we want to explicitly clear the value of
    a variable.

Reference Types; Object, Array and function.  
    Object:

        An object in JavaScript and other programming languages is like an object in real life.
        Think of a person, a person has name, age, addres... These are properties of a person. In have the
        same concept in JavaScript.
    ex: let name = 'Larissa';
        let age= 18;
    instead of referecing these two variables we can just reference the person object

        let person = {
            name: 'Larissa',
            age: 18
        };

        console.log(person);

    How to access a property?
    
     We have two ways to do it:
     Dot Notation:
     person.name = 'Leonardo';

     console.log(person.name);

     Bracket Notation:
     person['name'] = 'Yara';

     console.log(person.name);

One thing that separates JavaScript from a lot of programming languages, is that JavaScript is a
dynamic language, and what this mean?

We have two types of programming languages:

 Static Languages:

    In static languages, when we declare a variable the type 
    of the variable is set and it cannot be changed in the future.

 Dynamic Languages:
 In a dynamic language (like JavaScript) the type of a variable can change at run time.

What is an Array?

An array is a special variable, which can hold more than one value at a time.
  ex:
      let selectedColors = ['red', 'blue'];
      selectedColors[2]= 1;
      console.log(selectedColors.length);

length: This property returns a number of items or elements in an array.

What is a Function?

Functions are one of the fundamental building blocks in JavaScript. A function is basically a set of 
statements that performs a task or calculates a value.
ex 1:
    fuction greet() {
        console.log('Hello world');
    }

    greet(); 

In this example we just want to display a message on the console.

 ex 2:
    fuction greet(name, lastNames) {
            console.log('Hello' + name + '' + lastName);
        }

        greet('Larissa', 'Cuquejo'); 

Arithmetic Operators:

We use this form performing calculations. just like the calculations in mathematics.

ex:
    let x = 10;
    let y = 3;

console.log(x + y); 
console.log(x - y); 
console.log(x * y); 
console.log(x / y); 
console.log(x % y); 
console.log(x ** y);

// Increment (++)
console.log(x++);
console.log(x);

// Decrement (--)
console.log(--x);

How to swap a variable?
To swap the value of two variables we need a third variable.

let a = 'red';
let b = 'blue';

let c = a;
a = b;
b = c;

console.log(a);
console.log(b);

// Hour
// If hour is between 6am and 12pm: Good morning!
// If it is between 12pm and 6pm: Good afternoon!
// Otherwise: Good evening!

let hour =20; 

if (hour >= 6 && hour > 12)
  console.log('Good morning');
else if (hour >= 12 && hour > 18)
  console.log('Good afternoon');
else
  console.log('Good evening');

// we wanto to see if this user is a guest, or a moderator or an admin

switch (role) {
    case 'guest':
        console.log('Guest User');
        break;

    case 'moderator':
        console.log(Moderator User);
        break;
    
    default:
        console.log('Unknown User');
}

// We can also do this using if and else

if (role === 'guest' && hour > 12) console.log('Guest');
else if (role === 'moderator') console.log('Moderator'):
else console.log('Unknown User'); 

// let's imagine we want to display Hello world 5 times on the console.

The poor way:

console.log('Hello World')
console.log('Hello World')
console.log('Hello World')
console.log('Hello World')
console.log('Hello World')

There is a better way to achieve the same result, and that's where we use loops. We have various kind
of loops, and all these loops essentially do the same thing. They repeat a action a number of times.
We have For loops, while loops, do...while loops, for... in loops, for...of

for:

for (let x = 10; x <= 100; x=x+10) {
    console.log(x);
}

while:

 let x = 10;
 while (x <= 100) {
     console.log(x);
    x=x+10;
 }

do-while:

 let x = 10;
 do {
     console.log(x);
     x=x+10;
 } while (x <= 100);

 With for, while and do-while loops we can repeat an action a number of times. But we have two more 
 kinds of loops in JavaScript and we use them to iterate over the properties of an object or elements
 in an array 

Infinite loops executes forever. So if you accidentally create one of these loops, you're going to 
crash your browser or your computer. 

Ex 1:

    for (let x = 10; x <= 100;) {
        console.log(x);
    }

Ex 2:

    let x = 10;
    while (x <= 100) {
        console.log(x);
        
    }
Ex 3:

    while (true) {

    }
  
Let's say we have an object with two properties and we want to display all the properties of this
person
 Ex 1:

    const person = {
        name: 'Larissa',
        age: 18
    };
    
    for (let key in person)
    console.log(key, person[key]);

 Ex 2:

    const colors = ['red', 'green', 'blue'];

    for (let index in colors)
      console.log(index, colors[index]);
    
We have a new way to iterate over a raise and that is using the for of loop. it's very similar to the
for in loop but instead of the in keyword we use the of keyword.
Ex:
for (let color of colors)
  console.log(color);

Let's say we want to jump out of a loop. For example, we want to count from 0 to 4 instead of counting
normally from 1 to 5, so we need to use the break keyword:

    let x = 0;
    while (x <= 10) {
        if (x===5) break;

        console.log(x);
        x++;
    }

Now we want to see if x is an even number or not:

   let x = 0;
   while (x <= 10) {
    if (x % 2 === 0) {
        x++;
        continue;
    }

    console.log(x);
    x++;
  }


We want to do a function that takes two numbers and returns the maximum of the two:

    let number = max(1,2);
    console.log(number);

    function max(a,b) {  
        if (a > b) return a;
        return b;
    }
 
Now we will do the same thing but more clean:

    let number = max(1,2);
    console.log(number);

    function max(a,b) {
        return (a > b) ? a : b;
    }