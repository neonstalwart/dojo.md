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
## Properties

### _hideAnim


### _hideArgs


### _isHiding


### _isShowing


### _showAnim


### _showArgs


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

