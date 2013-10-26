# jQuery Notes

create an object and then call the function inside the object from within the `$(document).ready` function like so:

```javascript
var confirmation = {
  init: function() {
  // some event handlers
  }
}
```


```javascript
$(document).ready(function() {
  confirmation.init();
});
```

    