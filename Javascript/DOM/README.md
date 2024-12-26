# DOM

## DocumentFragment

Constructor:
```javascript
let fragment = new DocumentFragment();
let div = document.createElement("div");
fragment.append(div);
```


## FormData

Constructor:

```javascript
const formData = new FormData();

formData.append("username", "Chris");
```

## textContent

Sets or returns the text content of the specified node.

```javascript
element.textContent  # no parethesis
```


## append

Allows you to also append string objects, whereas Node.appendChild() only accepts Node objects.

```javascript
append(param1, param2, /* …, */ paramN)
```


## currentTarget

The element that triggered the event listener

```e.currentTarget```


## Data attributes

data-name: ```el.dataset.name```
