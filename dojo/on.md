# Module: dojo/on

## Summary

A function that provides core event listening functionality. With this function
you can provide a target, event type, and listener to be notified of
future matching events that are fired.
## Description

To listen for "click" events on a button node, we can do:

      define(["dojo/on"], function(listen){
        on(button, "click", clickHandler);
        ...

Evented JavaScript objects can also have their own events.

      var obj = new Evented;
      on(obj, "foo", fooHandler);

And then we could publish a "foo" event:

      on.emit(obj, "foo", {key: "value"});

We can use extension events as well. For example, you could listen for a tap gesture:

      define(["dojo/on", "dojo/gesture/tap", function(listen, tap){
        on(button, tap, tapHandler);
        ...

which would trigger fooHandler. Note that for a simple object this is equivalent to calling:

      obj.onfoo({key:"value"});

If you use on.emit on a DOM node, it will use native event dispatching when possible.
## Methods

### emit
Fires an event on the target object.

### once
This function acts the same as on(), but will only call the listener once. The
listener will be called for the first
event that takes place and then listener will automatically be removed.

### parse


### pausable
This function acts the same as on(), but with pausable functionality. The
returned signal object has pause() and resume() functions. Calling the
pause() method will cause the listener to not be called for future events. Calling the
resume() method will cause the listener to again be called for future events.

### selector
Creates a new extension event with event delegation. This is based on
the provided event type (can be extension event) that
only calls the listener when the CSS selector matches the target of the event.

The application must require() an appropriate level of dojo/query to handle the selector.

