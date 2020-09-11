So far, I feel that the pace of the program is perfect. While I did have some prior knowledge of JavaScript, I had largely forgotten a lot of what I had already learned and a refresher was long overdue. At this pace, I feel that I am not only regaining the information I had lost over time, but I also feel that I am learning a lot of new skills to build on that prior knowledge. I have just enough time to tinker and experiment with new concepts before moving onto the next and I feel accomplished after playing with each new concept. This far into the program, I believe that the current pacing is perfect. 

Functions are an extremely useful tool to organize large programs because they work wonders in terms of limiting repetition and keeping code looking clean. By having a function, the need to repeat a block of code multiple times is completely eliminated. That block of code can instead be written once inside of a function and the function can be called by the programmed multiple times, using different values for the given parameters. By doing this, you not only make your code shorter, but you also make your code much more readable. This will make it much easier to see what you were doing in a given block of code should you ever need to look back at that project for a reference to another project and will make it much easier for others working with you on a project to understand your thought process and what a given block of code is doing. This will also prove itself to be extremely useful in finding errors. Less code to go through means less places to create an error, saving you precious time when building your program. 

Scope is generally defined as the part of the program that a specific binding is visible to. This can generally be broken into 2 main categories, global and local. Global scopes are defined outside of any block of code and outside of any function and are visible to the entirety of the program below the defined function. Say for example you have:

```
console.log(number);

let animal;
let number = Number(prompt("Pick either "1" or "2"));

if (number = 1) {
  animal = "Dog"
} else {
  animal = "Cat"
}

console.log(animal)
```

In this example, both animal and number are visible to and can be used by the entirety of the code written underneath. However, because `console.log(number)` is written before number is defined in the code, it cannot see or use the number binding. The same would be true should we put the animal binding in its place. Think of scope as a zoo with global scope being the zoo in its entirety while local scopes would be each of the smaller, individual animal pens. Local scopes are for those bindings declared within a either a block of code (i.e., and if statement) or within a function, that will only be visible and useable by that block of code or function. For example, let's say we have:
```

let x = prompt("enter a letter");

if (x == "a") {
  let y = "hi";
  } else {
    let y = "bye";
  }

console.log(y);
```

In this case, `console.log(y)` will return an error because y is defined only withing the if statement and therefore, only exists and is useable within that if statement where it is defined. The only way to output y in this scenario through a console.log would be to move that console.log statement under each of the 'let y'
statements;

```
let x = prompt("enter a letter");

if (x == "a") {
  let y = "hi";
  console.log(y);
  } else {
    let y = "bye";
    console.log(y);
  }
```

If we wanted to make y visible within a function but not outside of the function, we could do so by defining y just above the if statement but still withing the brackets of the function:
let x = prompt("enter a letter");

```
function showY() {

let y;

  if (x == "a") {
    y = "hi";
    } else {
      y = "bye";
    }
    
  return y
};

console.log(showY());

console.log(y)
```

By defining y within the function but outside of the brackets of the if statement, y has now become visible and thus useable by the function, so the function is able to return y. However, just like before with the if statement, y does not exist outside of the function. Using console.log to display the function will display the returned value of y however, simply putting y into console.log will return an error as y as a binding is not visible to the console.log. It should be noted that there are some exceptions to this rule. While using const and let will ensure that the binding never escapes its intended scope, using var does pose the possibility of creating problems where sometimes var will actually allow the binding to escape its intended scope due to its hoisting properties, so in most cases, its much safer to use either let or const instead of var to define a binding. 
