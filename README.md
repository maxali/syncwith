# syncwith
Bind form with object. 

### Installation
  `<script src="syncwith.js"></script>`

### Usage

#### syncwith
1. Add `syncwith` attribute to your `form`. The `value` of the attribute becomes a JSON object
2. Add `modal` attribute to `input` elements. This will sync with the JSON object.

```html
<form syncwith="mydata">
  <input type="text" modal='id' id="id" placeholder="Id number" />
  <input type="text" modal='firsName' id="firstName" placeholder="firstName" />
  <input type="text" modal='lastName' id="lastName" placeholder="lastName" />
</form>
```

#### $.startSync();
Starts watching and binding your form with JSON object.

```javascript
console.log(mydata);
// mydata alwas has the latest values of your form input elements.
{
  "id": "value",
  "firstName": "First name value",
  "lastName": "Last name value"
}
```

[Play with it](http://plnkr.co/edit/BAoYyeDAboRwpAujSJeH)

#### Disclaimer
I use WatchJS library for watching changes in objects
Check it here: https://github.com/melanke/Watch.JS/
