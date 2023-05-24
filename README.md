# DOM manipulation cheat sheet for vanilla JS



### Create element
```
const newButton = document.createElement("button");
```


### List of Selectors
```
const firstDiv = document.querySelector('div');
```
```
const navMenu = document.getElementById('main-navigation');
const firstButtonChild = navMenu.querySelector('.button');
```
```
const matches = container.querySelectorAll("div.highlighted > p");
```

```
const cells = table.getElementsByTagName("td");
```
```
element.getElementsByClassName("test");
```
```
const up_names = document.getElementsByName("up");
```


### Removing an element
```
var element = document.querySelector('#some-element');
element.remove();
```



### Inner HTML 
```
const box = document.querySelector('box');
box.innerHTML = '<p>Goodbye</p>'
```

### Remove Child
```
const groceryList = document.getElementById('groceryList');
const iceCream = document.getElementById('iceCream');
groceryList.removeChild(iceCream);
```

### Parent node
```
const firstChild = document.getElementById('first-child');
firstChild.parentNode;
```

### Element.onClick()

```
let element = document.getElementById('addItem');
element.onclick = function() { 
  let newElement = document.createElement('li');
  document.getElementById('list').appendChild(newElement);
};
```



### AppendChild
```
var node1 = document.createElement('li');
document.getElementById('list').appendChild(node1);
```


### Element.style property
```
let blueElement = document.getElementById('colorful-element');
blueElement.style.backgroundColor = 'blue';
```

### AddEventListener & RemoveEventListener()

- This will add and remove the handlerFunctions
- useCapture: an optional Boolean value (true or false) that specifies whether the event should be executed in the capturing or bubbling phase.

```
element.addEventListener("event", eventHandlerFunction);
element.removeEventListener("event", eventHandlerFunction);
target.addEventListener(event, function, useCapture)
```


### Keyboard events
- `keydown` events are fired when the key is first pressed.
- `keyup` events are fired when the key is released.
- `keypress` events are fired when the user presses a key that produces a character value (aka is not a modifier key such as CapsLock).

### Current target

```
$('#button').on('click', event => {
  $(event.currentTarget).css('background-color', 'blue');  
});
```

### Mouse events
click events are fired when the user presses and releases a mouse button on an element.
- `mouseout` events are fired when the mouse leaves an element.
- `mouseover` events are fired when the mouse enters an element’s content.
- `mousedown` events are fired when the user presses a mouse button.
- `mouseup` events are fired when the user releases the mouse button.


