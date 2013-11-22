# Meteor notes

## Publish and Subscribe

* Replacing autopublish - adding the following code with replace the autopublish functionality

```javascript
if (Meteor.isServer) {
  Meteor.publish('subscription-name', function() {
    return CollectionName.find();
    // no arguments on 'find' will return everything
  }); 
}
```

```javascript
if (Meteor.isClient) {
  Meteor.startup(function() {
    Meteor.subscribe('subscription-name');
  });
}
```


* Controlling what is published

```javascript
if (Meteor.isServer) {
  Meteor.publish('subscription-name', function() {
    return CollectionName.find({completed: false});
    // would return only incomplete items
  }); 
}
```

```javascript
if (Meteor.isServer) {
  Meteor.publish('subscription-name', function() {
    return CollectionName.find({completed: completed}, {fields: {text: 1}});
    // would return only the text field from completed items
  }); 
}
```

## Database

`meteor reset` = wipe database in your Meteor app