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


## SelectionStart and End

The selectionStart property of the HTMLInputElement interface is a number that represents the beginning index of the selected text. When nothing is selected, then returns the position of the text input cursor (caret) inside of the <input> element.

`inputElement.selectionStart`

`inputElement.selectionEnd`


## Tab in textarea

```javascript
const textarea = document.querySelector("textarea");

textarea.addEventListener("keydown", function (e) {
  if (e.key === "Tab") {
    e.preventDefault();

    const start = this.selectionStart;
    const end = this.selectionEnd;

    // Insert tab character
    this.value =
      this.value.substring(0, start) +
      "\t" +
      this.value.substring(end);

    // Move cursor after the tab
    this.selectionStart = this.selectionEnd = start + 1;
  }
});
```

