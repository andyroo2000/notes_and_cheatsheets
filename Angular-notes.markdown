# Angular Notes

###### My super-basic personal notes while learning Angular.js

### Services

- To use a service, specify it as an argument in a controller:
for example:
`function EventController($scope) {...`

### Directives

#### Built-in directives

- `ng-change` is just like `ng-click`, except that a function is run every-time the input changes.

#### Custom directives

- it's generally a good practice to write directives as attributes, as in the following example:

```javascript
var app = angular.module("superhero", []);

app.directive("superman", function() {
    return {
      restrict: "A",  // The 'A' restriction is for 'attribute'
      // this restriction is option in this case, as it is the default
      link: function() {
        alert("I'm working stronger");
    }
  };
});
```

- the most common use-case for writing directives is not to specify a restriction and return an object, but to simple return a function as in the following example:

```javascript
app.directive("enter", function() {
  return function(scope, element) {
    element.bind("mouseenter", function() {
      console.log("The mouse is inside the house!");
    });
  };
});
```

- To make your code more reusable, use the **attrs** argument, which can be passed from the html, as in the following example:

```javascript
app.directive("enter", function() {
  return function(scope, element, attrs) {
    element.bind("mouseenter", function() {
      element.addClass(attrs.enter);
    });
  };
});
```

  To set the value of the **attr** in the html, you would do somehting like the following:

```jade
div(enter="headline" leave).
  I'm the affected content.
```
