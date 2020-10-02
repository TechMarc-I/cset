My favorite CSS property so far is the margin property. The margin property creates space around an element and is used to space elements on a webpage apart. This property takes in values for the width and height using any type of measurement unit. I personally love this property because it allows me to change the amount of space on a webpage to my personal preference and it helps in the overall layout of my webpage.


If I were making a website for a restaurant and needed to style the menu options to show that some are spicy or vegetarian or gluten-free with all menu options using the same html elements, I could use class selectors to differentiate between the types of each option. By creating a class, I can be more general and apply the same values to multiple menu items (i.e, all spicy items using one class selector, all vegetarian items using a different class selector, ect.) unlike when using an id selector in which I would only be able to apply the CSS values to that one specified item with that id(i.e, #spicy would only apply to the one item that had the id of 'spicy'). In this case, I would use:
/*styles.css*/
```
.spicy {
  color: red;
}

.vegetarian {
  color: green;
}

.gluten-free {
  color: blue;
}
```
/*index.html*/
```
<ul>
  <li class='spicy'>Spicy Shrimp Pasta Salad</li>
  <li class='vegetarian'>Orecchiette Pasta with Broccoli Sauce</li>
  <li class='gluten-free'>Smoky sausage and butternut lasagne</li>
  <li class='spicy'>Black Bean and Corn Jalapeño Poppers</li>
</ul>
```
Most notably, because a class selector was used rather than and id selector, the class 'spicy' was able to be applied to both Spicy 'Shrimp Pasta Salad' and 'Black Bean and Corn Jalapeño Poppers.' Using a class selector also allowed me to apply different values to each <li> item where as with setting them all with a general li modifier in the CSS file would have left no way to differentiate between each item's type.


In CSS,  cascade, inheritance, and specifity are concepts used to style a webpage. Cascade is the most broad and will apply styles from top to bottom in the order that they are written in the css file/style tag. The cascade concept will overwrite conflicting styles and will display the very last style applied:
```
p {
  color: blue;
  color: red;
  /*text color of 'p' will be 'red'*/
}
```
The concept of inheritance is that an element will 'inherit' or get the same values as its parent element. In this case:
```
body {
  background-color: yellow;
}
```
every element on the page would have a background of yellow. However due to cascading, say we had an h1 element within the body element, that had its background set to blue, the background color of blue in that element would overwrite the background color of yellow from the body element and thus, the background of the h1 element would be blue. Specfity goes a step further by not setting property values to a generic element, but rather to either a specific class or id. The concept of specifity will use the class or id to overwrite any conflicting styles. In this case:
```
/*styles.css*/
p {
  color: green;
}

.purple {
  color: purple;
}
```
```
/*index.html*/
<p>This is green</p>
<p class='purple'>This is purple</p>
```
the style rules for 'p' state that all 'p' elements should have a text color of green which is what is seen in the first 'p' element. However, with the second 'p' element using the class rules for 'purple,' the conflicting style is overwritten and the text color for that specific 'p' element will be displayed as the color purple, as it is considered to be more specific by the browser. In the case of having both an id and a class in the same element, the style rules of the id will take priority as it is considered to be even more specific than a class. 
