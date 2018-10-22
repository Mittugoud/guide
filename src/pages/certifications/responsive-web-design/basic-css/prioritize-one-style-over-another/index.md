---
title: Prioritize One Style Over Another
---
## Prioritize One Style Over Another
In some scenarios you would need to prioritize one style over the other, in order to avoid conflict between the styles.

Most important thing to remember while Prioritizing a Style in CSS is to assign a specific class which you want to apply on an element.

Example: From the below code the body element will automatically get applied or cascaded on h1 (heading 1) to make its color `green`.
```html
<style>
body
{
    background-color: black;
    font-family: monospace;
    color: green;
}
</style>

<h1>Hello World!</h1>
```
What if there is a new style to make 'h1' a different color. Lets say a new style class called "pink-text" is implemented with color value as `pink`.

Then there would be 2 color values conflicting with each other, color `green` from the "body" element and color `pink` from the "pink-text" class.

In order to fix this, the style class needs to be assigned specifically. A specified style class will take precedent over the previous style from body element.

Note: The class attribute is mostly used to point to a class in a style sheet. Hence, style class should always be declared inside the `<style> </style>` element as below.

For example: "pink-text" class should be implemented as below:
```html
<style>
.pink-text
 {
    color: pink;
 }
</style>
```
Note: A class element should always start with a `'.'` (dot or period) in front of the class name.

Now assign the "pink-text" class in the 'h1' element as below:
```html
<h1 class=pink-text> Hello World! </h1>
```

`Which color do you think would get applied to the 'h1' element from the code snippet below?`
```html
<style>
body
{
    background-color: black;
    font-family: Monospace;
    color: green;
}

.pink-text
{
    color: pink;
}
</style>

<h1 class=pink-text>Hello World!</h1>
```
You guessed right! Color `pink` would get applied to 'h1' element, as h1 uses the color from "pink-text" style class which is more specifically assigned style for 'h1' element.
