While I cannot give myself a number rating after completing the first course, I feel that I am definitely right where I need to be. I feel confident in my understanding of all of the material we have learned and I still feel just as, if not, even more excited that I was on day one to learn how to program, and I cannot wait to learn even more. While I do feel that I was successful in this course, one thing I plan to do differently with the next course is spending more time reading over and working with the extra links provided each week. I did my best to spend at least some time with each link each week but that is one aspect that could definitely be improved moving forward. 

Objects are defined as a collection of properties stored in a single value that use keys in order to call each individual property. Using an example from the weresquirrel problem;

```
let day1 = {
  squirrel: false,
  
  // array within an object
  events: ["work", "touched tree", "pizza", "running"]
};
```

we can see that two keys, 'squirrel' and 'events', are used to hold values and are all stored under the object value, 'day1'. The programmer is then able to access the values of squirrel or events by simply calling them using either dot notation (ex: `day1.squirrel`) or bracket notation (day1['squirrel']). Using this example, we see that the key, 'events', holds a list of other values. 

```
// array within an object
  events: ["work", "touched tree", "pizza", "running"]
```

This stored list is a special type of object known as an array. Arrays are similar in that they do store a collection of properties under a single value, however, rather than using keys, arrays instead rely on an ordered index starting at 0. Because arrays do not use keys and instead rely on an index, properties of arrays are only able to be called using bracket notation (ex: `events[0]` would call the value "work"). 

Using the above definitions and examples of an object and an array, we can begin to dive into why the programmer would use one over the other. In the case for the object of `day1`, the programmer needed to be able to call on and easily distinguish different values. Coming up with a name for each property was easy in this case because the programmer knew exactly what they needed, whether or not they turned into a squirrel and what events had occurred that day. In the case of the `events` key, using an array was perfectly acceptable because the programmer only needed a general list. Using an object would have been near impossible because the programmer has no idea what events will occur during the day so coming up with a named key for each event would have proved difficult to say the least. In my previous project, I could have used an object in my adventure game to have created a more interesting combat mechanic when fighting the monster, rather than just automatically having the monster kill you or you kill the monster based on whether you had a sword or not. Instead, I could have implemented a more RPG style of combat and allowed the used to choose from a list of attacks, each having its own attack value, and calling said attack in such a mannor as:
  
```
let monsterHealth = 10;
let attack = { jab: 2, potion: 6, kick: 1 };
  
let input = prompt("How do you attack?")
monsterHealth -= attack[input]

console.log(monsterHealth)
```

This would have allowed the user to not only choose how to attack but would have also allowed there to be varying amounts of damage and a way to keep track of the enemies health. 
