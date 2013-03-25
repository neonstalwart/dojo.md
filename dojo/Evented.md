# Module: dojo/Evented

## Summary

A class that can be used as a mixin or base class,
to add on() and emit() methods to a class
for listening for events and emitting events:


    define(["dojo/Evented"], function(Evented){
    var EventedWidget = dojo.declare([Evented, dijit._Widget], {...});
    widget = new EventedWidget();
    widget.on("open", function(event){
    ... do something with event
    });
    
    widget.emit("open", {name:"some event", ...});
# Constructor

## Methods

### emit


### on


