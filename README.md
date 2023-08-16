# important-topics-of-javacript

**Map,Reduce & filter Methods in Array**

**Map**

 The map() method is used for creating a new array from an existing one, applying a function to each one of the elements of the first array.

              Syntax
             var new_array = arr.map(function callback(element, index, array) {
            // Return value for new_array
            }[, thisArg])

**example**

In the following example, each number in an array is doubled.

              const numbers = [1, 2, 3, 4];
              const doubled = numbers.map(item => item * 2);
              console.log(doubled); // [2, 4, 6, 8]

**filter method**

The filter() method takes each element in an array and it applies a conditional statement against it. If this conditional returns true, the element gets pushed to the output array. If the condition returns false, the element does not get pushed to the output array.

Syntax
                  
                  var new_array = arr.filter(function callback(element, index, array) {
                  // Return true or false
                 }[, thisArg])

Examples
                  In the following example, odd numbers are "filtered" out, leaving only even numbers.

                const numbers = [1, 2, 3, 4];
                const evens = numbers.filter(item => item % 2 === 0);
                console.log(evens); // [2, 4]


**Reduce Method**

The reduce() method reduces an array of values down to just one value. To get the output value, it runs a reducer function on each element of the array.

               Syntax
               arr.reduce(callback[, initialValue])



The callback argument is a function that will be called once for every item in the array. This function takes four arguments, but often only the first two are used.

**accumulator** - the returned value of the previous iteration

**currentValue** - the current item in the array

**index** - the index of the current item

**array** - the original array on which reduce was called

The **initial value** argument is optional. If provided, it will be used as the initial accumulator value in the first call to the 

callback function.


                    const numbers = [1, 2, 3, 4];
                    const sum = numbers.reduce(function (result, item) {
                    return result + item;
                    }, 0);
                    console.log(sum); // 10

----------
🔍 **Exploring the JavaScript Call Stack: Understanding Execution and Order** 🔍


Ever wondered how JavaScript pieces together your code? 🤔 Let's delve into the Call Stack and its role in managing functions and their flow! 🎩🎉

🔹 Execution Contexts: Think of the Call Stack as a conductor organizing different parts of your code, including the big picture (global context) and smaller moments (function contexts).

🔹 Last-In-First-Out: Like a stack of plates, the Call Stack follows the rule of "Last-In, First-Out." The latest function invited to the party takes the lead and leaves first.

🔹 Invoking Functions: Calling a function is like inviting a character onto the stage. They bring their context, perform their role, and exit gracefully.

🔹 Nesting Functions: It's like storytelling within storytelling. One function invites others, forming a chain that the Call Stack orchestrates seamlessly.

🔹 Emptying the Stage: As the show progresses, functions take their bows and exit, clearing the Call Stack. When it's empty, the performance concludes.


Let's dive into the example:

🎭 Script's Drama Unfolds 🎭
             function add(a, b) {
             return a + b;
              }

            function average(a, b) {
             return add(a, b) / 2;
              }

            let x = average(10, 20);


1.The script begins with a global context.

2.The call to average(10, 20) adds its context to the stack.

3.Inside average(), add() gets its context.

4. After add() shines, its context exits.

5. average() concludes its scene, and its context departs.

🚀 The Call Stack empties, and the script's curtains close.

--------- 

🚀Power of Higher-Order Functions in JavaScript! 🚀

🔹 What's a Higher-Order Function? It's like a versatile tool in your coding toolbox! A function that takes or returns other functions. It's all about flexibility and reusability!

🔹 Callback Functions in Action: Imagine having a callback function that dances to your tune! 💃🎶 Pass it to a higher-order function, and watch the magic unfold!

       function callbackFunction() {
           console.log('I am a callback function');
       }

       function higherOrderFunction(func) {
         console.log('I am a higher-order function');
          func();
         }

        higherOrderFunction(callbackFunction);

In the above code higherOrderFunction() is a HOF because we are passing a callback function as a parameter to it.

JavaScript's Array methods like map, filter, and reduce are true magicians! ✨ They transform arrays effortlessly, making your code elegant and efficient.

Example:
      const numbers = [1, 2, 3, 4, 5];
      const squared = numbers.map(function(num) {
      return num * num;
      });

      const evens = numbers.filter(function(num) {
       return num % 2 === 0;
       });

     const sum = numbers.reduce(function(acc, num) {
     return acc + num;
     }, 0);

      console.log(squared); // Output: [1, 4, 9, 16, 25]
      console.log(evens);  // Output: [2, 4]
      console.log(sum);   // Output: 15



      Hoisting is a JavaScript behavior where variable and function declarations are moved to the top of their containing scope during the compilation phase, even before the code is executed. This means that you can use variables and functions before they are declared in your code. However, only the declarations are hoisted, not the initializations or assignments.

Here's an example to illustrate hoisting:

```javascript
console.log(myVar); // Outputs: undefined
var myVar = 42;

foo(); // Outputs: "Hello, World!"
function foo() {
    console.log("Hello, World!");
}
```

In this example:
1. The variable `myVar` is hoisted to the top of its scope, but its value is not assigned yet, so it's `undefined` when accessed before the actual assignment.
2. The function `foo()` is also hoisted, so it can be called before its actual declaration.

However, it's important to note that only declarations are hoisted, not initializations or assignments. Let's see another example:

```javascript
console.log(myVar); // Outputs: undefined
var myVar = 42;

bar(); // Throws an error: bar is not a function
var bar = function() {
    console.log("Hello from bar!");
};
```

In this example:
1. The variable `myVar` is hoisted, but again, its value is not assigned yet.
2. The variable `bar` is hoisted as well, but it is initialized with an anonymous function expression. Since only the declaration is hoisted, the assignment of the function to `bar` is not hoisted, resulting in the error.

To avoid unexpected behavior due to hoisting, it's recommended to declare variables at the beginning of their scope and to define functions before using them.

In summary, hoisting is a JavaScript mechanism where variable and function declarations are moved to the top of their scope during compilation, allowing you to use them before their actual declarations in the code. However, only the declarations are hoisted, not the assignments or initializations.







