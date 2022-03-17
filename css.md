# CSS

CSS contains information on how to style the HTML. This is how an element is positioned and what it looks like (color, size, etc). CSS is typically written in a separate file from the HTML file. It is then linked from the HTML file inside the `head` tag

```
<html>
  <head>
    <link rel="stylesheet" href="style.css"></link>
  </head>
  <body>
  
  </body
</html>
```

### Creating Styles

To style an element you first need to select the element you would like to style and then add the style properties. For example, to style a `div`

```
div {
  color: black;
}
```

In addition to selecting an element by its tag you can also select it by class name or id. To give an element an `id` you create an element with the property `id`&#x20;

```
<div id="some-id">Hello</div>
```

Similarly, to give an element a class you use the `class` property

```
<div class="some-class">Hi</div>
```

It is important to remember - `id` is unique and `class` can be re-used. In other words, don't give the same `id` to more than one element. You can have more than one element sharing the same `class` however.&#x20;

To select an id you use the `#` symbol in front of the id `#some-id`. To select a class you use the `.` symbol `.some-class`.&#x20;

```
#some-id {
  color: black;
}

.some-class {
  color: blue;
}
```

### Color and Size

Some of the most common styles involve color and size. If you want to change the color of text you use `font-color`. If you want to change the color of the entire element you use `background-color`.&#x20;

You can also change the `font-size`, the `width` and the `height` of an element. You can also give an element a `border`.&#x20;

All of these properties have different possible values. Here is an example of how we would use the styles above

```
div {
  font-size: 16px;
  font-color: red;
  background-color: blue;
  width: 200px;
  height: 200px;
  border: 1px solid black; 
}
```

### Layout

As we learned in HTML, elements are either block or inline. CSS gives us even more control over how we can position our elements.&#x20;

#### Absolute position

We can place an element exactly where we want on the page by using absolute positioning.

```
div {
  position: absolute;
  top: 50px;
  right: 50px;
  font-size: 16px;
  font-color: red;
  background-color: blue;
  width: 200px;
  height: 200px;
  border: 1px solid black; 
}
```

The above CSS code will put an element 50px from the top and 50px from the right. We can also set left and bottom. One important thing to remember is that an absolute positioned element is set according to its parent (in the HTML tree). If the parent element is set to `position:absolute` or `position:relative` then the element will be positioned relative to its parent and not the entire page.&#x20;

#### Fixed position

`position:fixed` is always relative to the page. It also stays in the exact same position even when the page is scrolled. This is typically used for top navigation bars, left or right menus and bottom bars.&#x20;

```
div {
  position: fixed;
  top: 50px;
  right: 50px;
  font-size: 16px;
  font-color: red;
  background-color: blue;
  width: 200px;
  height: 200px;
  border: 1px solid black; 
}
```

## Exercise

Using CSS, create a web page that looks like the one below.

![](<.gitbook/assets/Frame 2.png>)

### Extra Credit

Turn the "My Second webpage" text into a top nav bar that stays in position when the page is scrolled.&#x20;
