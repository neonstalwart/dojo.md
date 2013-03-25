# Module: dojo/fx/Toggler

*Constructor*

# Constructor

## Summary

A simple `dojo.Animation` toggler API.
## Description

class constructor for an animation toggler. It accepts a packed
set of arguments about what type of animation to use in each
direction, duration, etc. All available members are mixed into
these animations from the constructor (for example, `node`,
`showDuration`, `hideDuration`).
## Examples

      var t = new dojo/fx/Toggler({
        node: "nodeId",
        showDuration: 500,
        // hideDuration will default to "200"
        showFunc: dojo/fx/wipeIn,
        // hideFunc will default to "fadeOut"
      });
      t.show(100); // delay showing for 100ms
      // ...time passes...
      t.hide();
## Properties

### declaredClass


### hideDuration
Time in milliseconds to run the hide Animation

### node
the node to target for the showing and hiding animations

### showDuration
Time in milliseconds to run the show Animation

## Methods

### hide
Toggle the node to hidden

### hideFunc
The function that returns the `dojo.Animation` to hide the node

### show
Toggle the node to showing

### showFunc
The function that returns the `dojo.Animation` to show the node

