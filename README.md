# important-topics-of-javacript

**Map,Reduce & filter Methods in Array**

**Map**

 The map() method is used for creating a new array from an existing one, applying a function to each one of the elements of the first array.

              Syntax
             var new_array = arr.map(function callback(element, index, array) {
            // Return value for new_array
            }[, thisArg])

example

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


