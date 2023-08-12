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







