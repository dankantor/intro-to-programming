# More Javascript

In the previous lesson on Javascript we learned about variables, functions, if statements and loops. Javascript really shines however when it interacts with HTML and CSS. Today's lesson will show us how to do just that.

### Selecting an Element

In CSS when we want to apply a style to an element, we use a selector such as `#` for an ID and `.` for a Class. Javascript has something similar. If we want to select an element by id we do this

```
var myElement = document.querySelector('#some-id');
```

If we want to select an element by Class we do this&#x20;

```
var myElement = document.querySelector('.some-class');
```

The code above will select one element. If we have multiple elements with the same Class and want to select them all we would do this

```
var myElements = document.querySelectorAll('.some-class');
```

Notice that in the above code we used `querySelectorAll` instead of `querySelector`. That gives us an array of elements that we can then loop over to do things with

```
var myElements = document.querySelectorAll('.some-class');
myElements.forEach(function(myElement) {
  console.log(myElement);
});
```

### Event Listeners

We select elements when we want to do something with them. Many times, we want to listen for when a user clicks on an element so we can then do something after that. Here is how we would listen for a click

```
var myElement = document.querySelector('#some-id');
myElement.addEventListener('click', onClick);

function onClick(e) {
  console.log(e);
}
```

In the above code, we first select our element. Then we add a 'click' listener that will call our `onClick` function when the element is clicked. When our function is called it will pass the event as the function input.&#x20;

There are many events that we can listen to in addition to `click`. We can listen to `submit` events on forms. We can also listen to `play` and `pause` events on video and audio. &#x20;

### Alerts, Confirm and Prompt

There are many times when we want to alert the user of some information or ask the user for some input. We can accomplish this with the `alert` function.&#x20;

```
var myElement = document.querySelector('#some-id');
myElement.addEventListener('click', onClick);

function onClick(e) {
  alert('myElement was clicked');
}
```

If we want to ask the user to confirm something we can use `confirm`

```
var myElement = document.querySelector('#some-id');
myElement.addEventListener('click', onClick);

function onClick(e) {
  var didConfirm = confirm('Did you mean to click myElement?');
  console.log(didConfirm);
}
```

And finally, if we would like to ask the user to type in some text, we can use `prompt`

```
var myElement = document.querySelector('#some-id');
myElement.addEventListener('click', onClick);

function onClick(e) {
  var name = prompt('What is your name?');
  console.log(name);
}
```

### Changing HTML

Many times we want to change the HTML on our page in response to a user action. We can accomplish this using `innerHTML`.&#x20;

```
var myElement = document.querySelector('#some-id');
myElement.addEventListener('click', onClick);

function onClick(e) {
  var name = prompt('What is your name?');
  myElement.innerHTML = name;
}
```

In the above example, once the user tells us their name we change myElement so that it now shows the name they just provided.&#x20;

### Changing Style

Similar to changing the HTML we can also change the style by adding or removing a Class. When we do that, the CSS for the element will change.

```
// CSS
.red {
  color: red;
}

var myElement = document.querySelector('#some-id');
myElement.addEventListener('click', onClick);

function onClick(e) {
  myElement.classList.add('red');
}
```

We can user `classList.add` to add a class, `classList.remove` to remove one and we can check if an element has a class with `classList.contains`. If we want to toggle a class we can use `classList.toggle`.&#x20;

### Saving and Loading

Many times we want to save data so that it persists between sessions. We can do this by using `localStorage`. We can save any data we would like as long as we provide it with a name or `key`. The data we want to save is called the `value`.&#x20;

```
localStorage.setItem('name', 'Bob');
```

If we want to later retrieve our saved data we do this

```
var name = localStorage.getItem('name');
```

We can remove the item as well

```
localStorage.removeItem('name');
```

And if we want to clear all the data we have saved

```
localStorage.clear();
```

## Exercise

Create a page counter that increments by 1 every time a user visits our page. Make sure to show the counter to the user and give them a way to reset the counter.&#x20;

### Extra Credit

When the counter goes above 10 show it in green.&#x20;
